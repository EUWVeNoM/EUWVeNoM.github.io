---
description: |
  PowerView est un module de PowerSploit écrit en PowerShell pour obtenir une connaissance de la situation du réseau sur les domaines Windows. La commande ci-dessous interroge le contrôleur de domaine pour tous les utilisateurs ASREPRoastable.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

command: |
  Get-DomainUser -Domain test.local -DomainController 10.10.10.1 -PreauthNotRequired -Properties SamAccountName

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
