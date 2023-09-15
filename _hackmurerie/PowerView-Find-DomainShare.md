---
description: |
  PowerView est un module de PowerSploit écrit en PowerShell pour obtenir une connaissance de la situation du réseau sur les domaines Windows. La commande ci-dessous interroge le contrôleur de domaine pour obtenir une liste des partages disponibles auxquels l'utilisateur actuel a accès.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

command: |
  Find-DomainShare -CheckShareAccess -Domain test.local -DomainController 10.10.10.1
items:
  - Shell
OS:
  - Windows
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://github.com/PowerShellMafia/PowerSploit/tree/master/Recon
  - https://www.attackdebris.com/?p=470
---
