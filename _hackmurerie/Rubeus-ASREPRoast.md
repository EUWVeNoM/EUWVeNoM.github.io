---
description: |
  Le module `asreproast` de Rubeus va tenter de récolter les réponses AS_REP non préauth pour une liste donnée de noms d'utilisateurs. Ces réponses seront chiffrées avec le mot de passe de l'utilisateur, qui peut ensuite être déchiffré hors ligne. La commande suivante est exécutée sur une machine Windows dans le domaine de la victime.

  Command Reference:

  	Output File: hashes.txt

command: |
  Rubeus.exe asreproast /format:hashcat /outfile:hashes.txt
items:
  - Shell
services:
  - Kerberos
OS:
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
  - PrivEsc
references:
  - https://github.com/GhostPack/Rubeus
  - https://github.com/GhostPack/Rubeus#asreproast
---
