---
description: |
  linPEAS.sh est un script qui recherche tous les chemins possibles pour élever les privilèges sur les hôtes Linux. La commande ci-dessous exécute toutes les vérifications de priv esc et stocke les résultats dans un fichier.

  Command Reference:

  	Run all checks: cmd

  	Output File: <file>

command: | 
  linpeas.sh > <file>
items:
  - Shell
OS:
  - Linux
attack_types:
  - PrivEsc
references:
  - https://github.com/carlospolop/PEASS-ng/tree/master/linPEAS
  - https://book.hacktricks.xyz/windows/windows-local-privilege-escalation
---
