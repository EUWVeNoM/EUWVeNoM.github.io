---
description: |
  "CrackMapExec (alias CME) est un outil de post-exploitation qui permet d'automatiser l'évaluation de la sécurité des grands réseaux Active Directory." - https://github.com/mpgn/CrackMapExec/wiki. Cette commande énumère les groupes de domaine, les groupes locaux, les utilisateurs connectés, les identifiants relatifs (RID), les sessions, les utilisateurs de domaine, les partages/permissions SMB et obtient la politique de mot de passe du domaine. Vous pouvez également utiliser la notation CIDR pour cibler une plage d'adresses IP (par exemple <IP>/24).

  Command Reference:

  	Target IP: <IP>

  	Username: <user>

  	Password: <passwd>

command: |
  crackmapexec smb <IP> -u '<user>' -p '<passwd>' --groups --local-groups --loggedon-users --rid-brute --sessions --users --shares --pass-pol
items:
  - Username
  - Password
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
