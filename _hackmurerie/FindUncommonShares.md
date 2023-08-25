---
description: |
  Le script FindUncommonShares.py est un équivalent Python de Invoke-ShareFinder.ps1 de PowerView permettant de trouver rapidement des parts peu communes dans de vastes domaines Windows.

  Command Reference:

    Domain: <domain.local>

  	Target IP: <IP>

  	Username: <user>

  	Password: <passwd>

command: |
  python3 FindUncommonShares.py -u '<user>' -d '<domain.local>' -p '<passwd>' --dc-ip <IP>
items:
  - Password
  - Username
  - Hash
services:
  - SMB
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://github.com/p0dalirius/FindUncommonShares
---
