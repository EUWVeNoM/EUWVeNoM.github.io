---
description: |
  Smbclient est un outil utilisé pour communiquer avec les serveurs SMB. La commande suivante énumère tous les partages disponibles sur l'ip cible en utilisant le hash de l'utilisateur <user> sur le domaine de <domain.local>.

  Command Reference:

  	Target IP: <IP>

  	Domain: <domain.local>

  	Username: <user>

  	Hash: <hash>

command: |
  smbclient -L \\<IP> -U <domain.local>/<user> --pw-nt-hash <hash>
items:
  - Username
  - Hash
services:
  - SMB
OS:
  - Linux
attack_types:
  - Enumeration
references:
  - https://www.samba.org/samba/docs/current/man-html/smbclient.1.html
---
