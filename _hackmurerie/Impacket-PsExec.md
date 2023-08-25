---
description: |
  Le fichier psexec.py d'Impacket offre des fonctionnalités similaires à celles de psexec. Cela vous donnera un shell interactif sur l'hôte Windows. Il peut également être utilisé pour trouver des parts accessibles en écriture sur la machine cible.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Password: password123
command: |
  python3 psexec.py test.local/john:password123@10.10.10.1
items:
  - Password
  - Username
services:
  - SMB
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
  - Enumeration
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/psexec.py
  - https://www.sans.org/blog/psexec-python-rocks/
---
