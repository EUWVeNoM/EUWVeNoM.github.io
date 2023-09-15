---
description: |
  La commande PowerShell ConvertTo-SecureString permet de convertir un texte en clair en une forme cryptée pouvant être utilisée pour un stockage ou une transmission sécurisés. Elle prend une chaîne de texte en clair et la convertit en un objet chaîne sécurisé qui peut être enregistré dans un fichier ou utilisé en mémoire à des fins d'authentification ou de cryptage.

  Command Reference:

  	Variable name: $pass

  	Password: password123

command: |
  $pass = ConvertTo-SecureString 'password123' -AsPlainText -Force
items:
  - Shell
services:

OS:
  - Windows
  - Approved-tool
attack_types:
  - General
references:
  - https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.security/convertto-securestring?view=powershell-7.3
  - https://www.pdq.com/blog/secure-password-with-powershell-encrypting-credentials-part-1/
---
