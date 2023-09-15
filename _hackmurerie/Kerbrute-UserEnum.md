---
description: |
  Kerbrute de ropnop effectue une recherche brute et énumère les comptes Active Directory valides par le biais de la préauthentification Kerberos. La commande suivante tente d'énumérer les noms d'utilisateur valides à partir d'une liste de noms d'utilisateur à essayer.

  Command Reference:

  	Domain: test.local

  	Username List: usernames.txt
command: |
  kerbrute userenum -d test.local usernames.txt
items:
  - No_Creds
services:
  - Kerberos
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://github.com/ropnop/kerbrute
---
