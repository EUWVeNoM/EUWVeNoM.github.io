---
description: |
  Smbclient est un outil utilisé pour communiquer avec les serveurs SMB. La commande suivante permet de se connecter à un partage SMB `<C$>` en utilisant des informations d'identification valides.

  Command Reference:

  	Target IP: <IP>

  	Domain: <domain.local>

  	SMB Share: <C$>

  	Username: <user>

  	Password: <passwd>

command: |
  smbclient \\\\<domain.local>\\<C$> -I <IP> -U <user> <passwd>
items:
  - Username
  - Password
services:
  - SMB
OS:
  - Linux
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://www.samba.org/samba/docs/current/man-html/smbclient.1.html
  - https://www.madirish.net/59
---
