---
description: |
  "CrackMapExec (alias CME) est un outil de post-exploitation qui permet d'automatiser l'évaluation de la sécurité des grands réseaux Active Directory." - https://github.com/mpgn/CrackMapExec/wiki. Cette commande permet d'énumérer les hôtes SMB utilisant un accès anonyme.

  Command Reference:

  	Target IP: <IP>

command: |
  crackmapexec smb <IP> -u 'a' -p ''
items:
  - No_Creds
services:
  - SMB
attack_types:
  - Enumeration
OS:
  - Linux
  - Approved-tool
references:
  - https://github.com/mpgn/CrackMapExec
  - https://github.com/mpgn/CrackMapExec/wiki
---
