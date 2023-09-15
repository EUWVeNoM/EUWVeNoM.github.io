---
description: |
  SharpDump.exe fait partie de la suite d'outils GhostPack et est un portage en C# de Out-Minidump.ps1 de PowerSploit. Il permet d'extraire le processus LSASS ou un processus spécifique à partir de son PID. Ce dump peut ensuite être introduit dans mimikatz pour extraire des informations sensibles. La commande suivante vide simplement le processus LSASS.

command: |
  SharpDump.exe
items:
  - Shell
OS:
  - Windows
  - Approved-tool
attack_types:
  - PrivEsc
  - Enumeration
references:
  - https://github.com/GhostPack/SharpDump
  - https://www.harmj0y.net/blog/redteaming/ghostpack/
---
