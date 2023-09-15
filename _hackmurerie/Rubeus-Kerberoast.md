---
description: |
  Le module `kerberoast` de Rubeus va tenter de récupérer les noms de service (Service Principal Names) qui sont associés à des comptes d'utilisateurs normaux. Il renvoie un ticket crypté avec le mot de passe du compte utilisateur, qui peut ensuite être forcé hors ligne. La commande suivante est exécutée sur une machine Windows du domaine victime.

  Command Reference:

  	Output File: hashes.txt

command: |
  Rubeus.exe kerberoast /outfile:hashes.txt
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
  - https://github.com/GhostPack/Rubeus#kerberoast
---
