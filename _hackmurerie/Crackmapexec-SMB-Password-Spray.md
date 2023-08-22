---
description: |
  "CrackMapExec (alias CME) est un outil de post-exploitation qui permet d'automatiser l'évaluation de la sécurité des grands réseaux Active Directory." - https://github.com/mpgn/CrackMapExec/wiki. Cette commande permet de pulvériser les mots de passe via SMB sur le contrôleur de domaine.

  Command Reference:

  	Domain Controller IP: <IP>

  	Username List: <dict>

  	Password: <passwd>

command: |
  crackmapexec smb <IP> -u <dict> -p <passwd>
items:
  - Username
services:
  - SMB
attack_types:
  - Exploitation
OS:
  - Linux
  - Approved-tool
references:
  - https://github.com/mpgn/CrackMapExec
  - https://github.com/mpgn/CrackMapExec/wiki
---
