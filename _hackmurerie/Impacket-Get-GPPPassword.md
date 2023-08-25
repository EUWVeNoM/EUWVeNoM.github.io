---
description: |
  Script Python pour extraire et décrydéchiffrer automatiquement les mots de passe des préférences de stratégie de groupe (GPP) en utilisant des flux pour découper des fichiers au lieu de monter des partages.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Password: password123

command: |
  python3 Get-GPPPassword.py 'TEST.local/john:password123@DC01.TEST.local' -dc-ip 10.10.10.1
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
  - Exploitation
  - Enumeration
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/Get-GPPPassword.py
  - https://podalirius.net/en/articles/exploiting-windows-group-policy-preferences/
---
