---
description: |
  Seatbelt.exe fait partie de la suite d'outils GhostPack qui effectue de nombreux "contrôles de sécurité" sur l'hôte Windows et collecte des données système qui pourraient être utiles pour d'éventuelles méthodes d'escalade des privilèges ou de persistance. La commande suivante exécute toutes les vérifications sur le système et stocke la sortie dans un fichier (ATTENTION : collecte beaucoup de données. supprimez `-full` pour moins de sortie).

  Command Reference:

  	Run all checks: -group=all

  	Output File: output.txt

command: |
  Seatbelt.exe -group=all -full > output.txt
items:
  - Shell
OS:
  - Windows
  - Approved-tool
attack_types:
  - PrivEsc
  - Persistence
references:
  - https://github.com/GhostPack/Seatbelt
  - https://www.harmj0y.net/blog/redteaming/ghostpack/
---
