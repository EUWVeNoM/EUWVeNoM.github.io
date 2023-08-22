---
description: |
  "CrackMapExec (alias CME) est un outil de post-exploitation qui permet d'automatiser l'évaluation de la sécurité des grands réseaux Active Directory." - https://github.com/mpgn/CrackMapExec/wiki. Cette commande exécute une commande powershell sur la machine cible si l'utilisateur dispose des privilèges d'administrateur. L'utilisation de "-x" permet d'exécuter la commande à partir de cmd.

  Command Reference:

  	Target IP: <IP>

  	Username: <user>

  	Password: <passwd>

command: |
  crackmapexec smb <IP> -u '<user>' -p '<passwd>' -X '$Host'
items:
  - Username
  - Password
services:
  - SMB
attack_types:
  - Exploitation
OS:
  - Linux
references:
  - https://github.com/mpgn/CrackMapExec
  - https://github.com/mpgn/CrackMapExec/wiki
---
