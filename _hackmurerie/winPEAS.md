---
description: |
  winpeas.exe est un script qui recherche tous les chemins possibles pour élever les privilèges sur les hôtes Windows. La commande ci-dessous exécute toutes les vérifications de priv esc et stocke les résultats dans un fichier.

  Command Reference:

  	Run all checks: cmd

  	Output File: <file>

command: |
  winpeas.exe cmd > <file>
items:
  - Shell
OS:
  - Windows
  - New-tool
attack_types:
  - PrivEsc
references:
  - https://github.com/carlospolop/PEASS-ng/tree/master/winPEAS
  - https://book.hacktricks.xyz/windows/windows-local-privilege-escalation
---
