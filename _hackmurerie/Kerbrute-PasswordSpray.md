---
description: |
  Kerbrute de ropnop effectue une recherche brute et énumère les comptes Active Directory valides par le biais de la préauthentification Kerberos. La commande suivante effectue une pulvérisation de mot de passe contre une liste d'utilisateurs fournis avec un mot de passe.

  Command Reference:

  	Domain: test.local

  	Username List: domain_users.txt

  	Password: password123
command: |
  kerbrute passwordspray -d test.local domain_users.txt password123
items:
  - Username
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
