---
description: |
  PSCredential est une cmdlet PowerShell utilisée pour créer un objet d'identification. Il est utilisé pour stocker et récupérer en toute sécurité des noms d'utilisateur et des mots de passe dans des scripts ou des commandes. La méthode GetNetworkCredential permet de récupérer le mot de passe.

  Command Reference:

  	Variable name: $cred

    Method: GetNetworkCredential

command: |
  $cred.GetNetworkCredential().Password

code: |
  $pass = ConvertTo-SecureString 'password123' -AsPlainText -Force

  $Cred = New-Object System.Management.Automation.PSCredential('htb.local\mmaas', $pass)

items:
  - Shell
services:
  - 
OS:
  - Windows
  - Approved-tool
attack_types:
  - Cracking
references:
  - https://jatinpurohit.wordpress.com/2020/04/08/decrypt-pscredential-object-password-and-its-applications/
---
