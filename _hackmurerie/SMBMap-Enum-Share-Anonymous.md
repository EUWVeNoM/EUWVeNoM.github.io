---
description: |
  SMBMap est un outil utilisé pour énumérer les lecteurs partagés SMB, y compris la liste des autorisations des lecteurs partagés, le contenu des partages, la fonctionnalité de téléchargement, l'énumération des noms de fichiers et l'exécution de commandes à distance. La commande suivante permet d'énumérer une liste d'hôtes SMB pour les partages SMB accessibles, qu'il s'agisse de lecteurs locaux ou mappés, sans informations d'identification (session nulle).

  Command Reference:

  	Domain: <domain.local>

  	SMB Hosts: <smb-hosts.txt>

command: |
  python3 smbmap.py --host-file <smb-hosts.txt> -d <domain.local> -L
items:
  - No_Creds
services:
  - SMB
OS:
  - Linux
  - Windows
attack_types:
  - Enumeration
references:
  - https://github.com/ShawnDEvans/smbmap
  - https://www.nopsec.com/blog/smbmap-wield-it-like-the-creator/
---
