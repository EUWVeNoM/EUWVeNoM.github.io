---
description: |
  Le script `krb5-enum-users` de Nmap tente de forcer et d'énumérer les comptes Active Directory valides à travers la préauthentification Kerberos. La commande suivante tentera d'énumérer les noms d'utilisateurs valides à partir d'une liste de noms d'utilisateurs à essayer.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username List: usernames.txt
command: |
  nmap -p 88 --script=krb5-enum-users --script-args krb5-enum-users.realm='test.local',userdb=usernames.txt 10.10.10.1
items:
  - No_Creds
services:
  - Kerberos
  - Enumeration
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://nmap.org/download.html
  - https://nmap.org/nsedoc/scripts/krb5-enum-users.html
---
