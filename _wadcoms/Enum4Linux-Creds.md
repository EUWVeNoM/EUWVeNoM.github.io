---
description: |
  Enum4Linux est un outil permettant d'énumérer des informations à partir de systèmes Windows et Samba, en utilisant un certain nombre de techniques différentes. La commande suivante tente d'énumérer des informations à partir d'identifiants de connexion valides.

  Command Reference:

  	Target IP: <IP>

  	Username: <user>

  	Password: <passwd>

command: |
  enum4linux -u <user> -p <passwd> -a <IP>
items:
  - Username
  - Password
attack_types:
  - Enumeration
OS:
  - Linux
references:
  - https://github.com/CiscoCXSecurity/enum4linux
  - https://highon.coffee/blog/enum4linux-cheat-sheet/
---
