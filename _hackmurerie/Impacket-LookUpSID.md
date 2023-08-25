---
description: |
  Le fichier lookupsid.py d'Impacket effectue un bruteforcing des SID Windows pour identifier les utilisateurs/groupes sur la cible distante.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Password: password123

command: |
  python3 lookupsid.py test.local/john:password123@10.10.10.1
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
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/lookupsid.py
  - https://www.puckiestyle.nl/impacket/
---
