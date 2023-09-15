---
description: |
  SharpUp.exe fait partie de la suite d'outils GhostPack et est un portage C# de PowerUp qui effectue de nombreux contrôles d'escalade de privilèges. La commande suivante exécute tous les contrôles d'escalade de privilèges et stocke les résultats dans un fichier.

  Command Reference:

  	Output File: output.txt

command: |
  SharpUp.exe > output.txt
items:
  - Shell
OS:
  - Windows
  - Approved-tool
attack_types:
  - PrivEsc
references:
  - https://github.com/GhostPack/SharpUp
  - https://www.harmj0y.net/blog/redteaming/ghostpack/
---
