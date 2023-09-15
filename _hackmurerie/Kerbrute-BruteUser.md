---
description: |
  Kerbrute de ropnop permet de forcer brutalement et d'énumérer les comptes Active Directory valides grâce à la préauthentification Kerberos. La commande suivante permet de forcer brutalement un compte à partir d'une liste de mots de passe fournis avec un nom d'utilisateur.

  Command Reference:

  	Domain: test.local

  	Password List: passwords.txt

  	Username: john
command: |
  kerbrute bruteuser -d test.local passwords.txt john
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
