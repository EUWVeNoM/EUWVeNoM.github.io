---
description: |
  Snaffler est un outil utilisé pour énumérer des données sensibles (mots de passe, informations confidentielles, etc.) à partir de partages de fichiers dans Active Directory. Il recherche les fichiers intéressants en se basant sur les extensions de fichiers, les noms de fichiers et le contenu des fichiers qui sont comparés à des expressions rationnelles. Il est également hautement configurable, ce qui vous permet d'ajouter vos propres recherches par expressions rationnelles. La commande suivante énumère toutes les machines du domaine et recherche les partages de fichiers accessibles, en vérifiant les fichiers intéressants susceptibles de contenir des données sensibles.

  Command Reference:

  	Domain: test.local

  	Domain Controller: 10.10.10.1

command: |
  Snaffler.exe -s -o snaffler_output.log -d test.local -c 10.10.10.1
items:
  - Shell
services:
  - SMB
OS:
  - Windows
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://github.com/SnaffCon/Snaffler
---
