---
description: |
  SMBMap est un outil utilisé pour énumérer les lecteurs partagés SMB, y compris la liste des permissions des lecteurs partagés, le contenu des partages, la fonctionnalité de téléchargement, l'énumération des noms de fichiers et l'exécution de commandes à distance. La commande suivante permet d'énumérer une liste d'hôtes SMB pour les partages SMB accessibles, qu'il s'agisse de lecteurs locaux ou mappés, à l'aide d'informations d'identification valides.

  Command Reference:

  	Domain: <domain.local>

  	SMB Hosts: <smb-hosts.txt>

  	Username: <user>

  	Password: <passwd>

command: |
  python3 smbmap.py --host-file <smb-hosts.txt> -u <user> -p '<passwd>' -d <domain.local> -L
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
