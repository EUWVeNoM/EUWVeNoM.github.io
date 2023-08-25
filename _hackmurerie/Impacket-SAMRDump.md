---
description: |
  Le fichier samrdump.py d'Impacket communique avec l'interface SAMR (Security Account Manager Remote) pour dresser la liste des comptes d'utilisateurs du système, des partages de ressources disponibles et d'autres informations sensibles.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Password: password123

command: |
  python3 samrdump.py test.local/john:password123@10.10.10.1
items:
  - Password
  - Username
services:
  - RPC
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/samrdump.py
  - https://www.hackingarticles.in/impacket-guide-smb-msrpc/
---
