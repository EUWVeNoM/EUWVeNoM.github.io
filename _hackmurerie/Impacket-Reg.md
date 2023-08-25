---
description: |
  reg.py d'Impacket est un outil de manipulation du registre à distance, qui offre des fonctionnalités similaires à reg.exe sous Windows.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Password: password123

command: |
  python3 reg.py test.local/john:password123@10.10.10.1 query -keyName HKLM\\SOFTWARE\\Policies\\Microsoft\\Windows -s
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
  - Persistence
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/reg.py
  - https://www.hackingarticles.in/impacket-guide-smb-msrpc/
---
