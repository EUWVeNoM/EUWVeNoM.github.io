---
description: |
  "CrackMapExec (alias CME) est un outil de post-exploitation qui permet d'automatiser l'évaluation de la sécurité des grands réseaux Active Directory." - https://github.com/mpgn/CrackMapExec/wiki. Cette commande énumère les groupes de domaine, les groupes locaux, les utilisateurs, les descriptions d'utilisateurs, les utilisateurs autorisés pour la délégation, les utilisateurs sans mot de passe, Vous pouvez également utiliser la notation CIDR pour cibler une plage d'adresses IP (i.e. <IP>/24).

  Command Reference:

  	Target IP: <IP>

  	Username: <user>

  	Password: <passwd>

command: |
  crackmapexec ldap <IP> -u '<user>' -p '<passwd>' --trusted-for-delegation  --password-not-required --admin-count --users --groups
items:
  - Username
  - Password
services:
  - LDAP
attack_types:
  - Enumeration
OS:
  - Linux
  - Approved-tool
references:
  - https://github.com/mpgn/CrackMapExec
  - https://github.com/mpgn/CrackMapExec/wiki
---
