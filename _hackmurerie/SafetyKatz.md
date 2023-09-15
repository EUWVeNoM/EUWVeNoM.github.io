---
description: |
  SafetyKatz.exe fait partie de la suite d'outils GhostPack et est une combinaison de SharpDump et de Mimikatz. La commande suivante videra le processus LSASS et lancera Mimikatz pour extraire les informations d'identification du processus vider.

command: |
  SafetyKatz.exe
items:
  - Shell
OS:
  - Windows
  - Approved-tool
attack_types:
  - PrivEsc
  - Enumeration
references:
  - https://github.com/GhostPack/SafetyKatz
  - https://www.harmj0y.net/blog/redteaming/ghostpack/
---
