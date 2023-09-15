---
description: |
  SharpWMI.exe fait partie de la suite d'outils GhostPack qui fournit des fonctionnalités WMI, telles que des requêtes WMI locales/à distance, la création de processus WMI à distance et l'exécution à distance de VBS arbitraires par le biais d'événements WMI. La commande suivante permet de dresser la liste de tous les processus en cours d'exécution sur le système local.

  Command Reference:

  	Get all processes: "select * from win32_process"

command: |
  SharpWMI.exe action=query query="select * from win32_process"
items:
  - Shell
services:
  - WMI
OS:
  - Windows
  - Approved-tool
attack_types:
  - Persistence
references:
  - https://github.com/GhostPack/SharpWMI
  - https://www.harmj0y.net/blog/redteaming/ghostpack/
---
