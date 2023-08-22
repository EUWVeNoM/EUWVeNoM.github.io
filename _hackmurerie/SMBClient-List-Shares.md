---
description: |
  Smbclient est un outil utilisé pour communiquer avec les serveurs SMB. La commande suivante énumère tous les partages disponibles sur le serveur cible à l'aide d'informations d'identification valides.

  Command Reference:

  	Target IP: <IP>

  	Domain: <domain.local>

  	Username: <user>

  	Password: <passwd>

command: |
  smbclient -L \\<domain.local> -I <IP> -U <user> <passwd>
items:
  - Username
  - Password
services:
  - SMB
OS:
  - Linux
attack_types:
  - Enumeration
references:
  - https://www.samba.org/samba/docs/current/man-html/smbclient.1.html
---
