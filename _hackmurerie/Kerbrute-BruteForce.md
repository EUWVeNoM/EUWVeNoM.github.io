---
description: |
  Kerbrute de ropnop permet de forcer brutalement et d'énumérer les comptes Active Directory valides grâce à la préauthentification Kerberos. La commande suivante tente de forcer des identifiants et des mots de passe valides à partir d'une liste d'informations d'identification (au format `nom d'utilisateur:mot de passe`).

  Command Reference:

  	Domain: test.local

  	Credential List: credentials.txt
command: |
  cat credentials.txt | kerbrute_linux_amd64 -d test.local bruteforce -
items:
  - No_Creds
services:
  - Kerberos
OS:
  - Linux
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://github.com/ropnop/kerbrute
---
