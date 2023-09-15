---
description: |
  SMBMap est un outil utilisé pour énumérer les lecteurs partagés SMB, y compris la liste des autorisations des lecteurs partagés, le contenu des partages, la fonctionnalité de téléchargement, l'énumération des noms de fichiers et l'exécution de commandes à distance. La commande suivante permet d'énumérer une liste d'hôtes SMB à la recherche de fichiers et de noms de fichiers contenant le mot-clé `password`.

  Command Reference:

  	Domain: <domain.local>

  	SMB Hosts: <smb-hosts.txt>

  	Username: <user>

  	Password: <passwd>

command: |
  python3 smbmap.py --host-file <smb-hosts.txt> -u <user> -p '<passwd>' -d <domain.local> -F password
items:
  - Username
  - Password
services:
  - SMB
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://github.com/ShawnDEvans/smbmap
  - https://www.nopsec.com/blog/smbmap-wield-it-like-the-creator/
---
