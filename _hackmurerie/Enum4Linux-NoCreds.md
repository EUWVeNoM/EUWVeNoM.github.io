---
description: |
  Enum4Linux est un outil permettant d'énumérer des informations à partir de systèmes Windows et Samba, en utilisant un certain nombre de techniques différentes. La commande suivante tentera d'énumérer des informations en l'absence d'informations d'identification.

  Command Reference:

  	Target IP: <IP>

command: |
  enum4linux -a 10.10.10.1
items:
  - No_Creds
attack_types:
  - Enumeration
OS:
  - Linux
  - Approved-tool
references:
  - https://github.com/CiscoCXSecurity/enum4linux
  - https://highon.coffee/blog/enum4linux-cheat-sheet/
---
