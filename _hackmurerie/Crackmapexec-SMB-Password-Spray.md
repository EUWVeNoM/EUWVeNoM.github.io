---
description: |
  "CrackMapExec (a.k.a CME) is a post-exploitation tool that helps automate assessing the security of large Active Directory networks." - https://github.com/byt3bl33d3r/CrackMapExec/wiki. This command will perform password/user spraying over SMB against the domain controller.

  Command Reference:

  	Domain Controller IP: 10.10.10.1

  	Username List: users.txt

  	Password: password123 /password.txt

command: |
  crackmapexec smb 10.10.10.1 -u users.txt -p password123
items:
  - Username
  - Password
services:
  - SMB
attack_types:
  - Exploitation
  - Enumeration
OS:
  - Linux
references:
  - https://github.com/byt3bl33d3r/CrackMapExec
  - https://github.com/byt3bl33d3r/CrackMapExec/wiki
---
