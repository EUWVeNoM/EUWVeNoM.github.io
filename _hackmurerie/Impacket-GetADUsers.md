---
description: |
  GetADUsers.py d'Impacket tentera de rassembler des données sur les utilisateurs du domaine et leurs adresses électroniques correspondantes.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Password: password123

command: |
  python3 GetADUsers.py -all test.local/john:password123 -dc-ip 10.10.10.1
items:
  - Username
  - Password
services:
  - Kerberos
attack_types:
  - Enumeration
OS:
  - Linux
  - Windows
  - Approved-tool
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/GetADUsers.py
---
