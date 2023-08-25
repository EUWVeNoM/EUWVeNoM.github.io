---
description: |
  Description de l'action et de l'utilité de la commande.

  Command Reference:

    Username: <user_list>

    Password: <passwd>

    Server/IP: <domain.local>

    Service: ssh

command: |
  hydra -L <user_list> -p  <passwd> <domain.local> ssh 

items:
  - Username
  - Password
  - No_creds
services:
  - SSH
  - SMB
  - WMI
OS:
  - Windows
  - Linux
  - Approved-tool
attack_types:
  - Enumeration
  - Exploitation
  - Cracking
references:
  - https://www.freecodecamp.org/news/how-to-use-hydra-pentesting-tutorial/
  - https://www.kali.org/tools/hydra/
---