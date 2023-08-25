---
description: |
  Le fichier rpcdump.py d'Impacket énumère les points d'extrémité des appels de procédure à distance (RPC).

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Password: password123

command: |
  python3 rpcdump.py test.local/john:password123@10.10.10.1
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
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/rpcdump.py
  - https://www.hackingarticles.in/impacket-guide-smb-msrpc/
---
