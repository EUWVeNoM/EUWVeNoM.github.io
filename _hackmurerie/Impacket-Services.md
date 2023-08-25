---
description: |
  Le fichier services.py d'Impacket communique avec les services Windows en utilisant l'interface MSRPC. Il peut effectuer de nombreuses actions différentes sur n'importe quel service.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Password: password123

  	Action: list

command: |
  python3 services.py test.local/john:password123@10.10.10.1 list
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
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/services.py
  - https://www.hackingarticles.in/impacket-guide-smb-msrpc/
---
