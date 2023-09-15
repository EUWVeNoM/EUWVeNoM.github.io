---
description: |
  PSCredential est une cmdlet PowerShell utilisée pour créer un objet d'identification. Elle permet de stocker et de récupérer en toute sécurité des noms d'utilisateur et des mots de passe dans des scripts ou des commandes. La cmdlet PSCredential nécessite un nom d'utilisateur et un objet SecureString pour le mot de passe.

  Command Reference:

  	Variable name: $Cred

    Username: htb.local\mmaas

  	Password: $pass = ConvertTo-SecureString 'password123' -AsPlainText -Force

command: |
  $Cred = New-Object System.Management.Automation.PSCredential('htb.local\mmaas', $pass)
items:
  - Shell
services:

OS:
  - Windows
  - Approved-tool
attack_types:
  - General
references:
  - https://learn.microsoft.com/en-us/powershell/scripting/learn/deep-dives/add-credentials-to-powershell-functions?view=powershell-7.3
  - https://pscustomobject.github.io/powershell/howto/PowerShell-Create-Credential-Object/
---
