---
description: |
  Smbclient est un outil utilisé pour communiquer avec les serveurs SMB. La commande suivante permet de lister tous les partages disponibles sur le serveur cible en utilisant une connexion anonyme.

  Command Reference:

  	Target IP: <IP>

  	Domain: <domain.local>

command: |
  smbclient -L \\<domain.local> -I <IP> -N
items:
  - No_Creds
services:
  - SMB
OS:
  - Linux
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://www.samba.org/samba/docs/current/man-html/smbclient.1.html
---
