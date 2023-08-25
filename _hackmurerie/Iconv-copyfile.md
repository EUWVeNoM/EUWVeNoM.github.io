---
description: |
  Iconv est un programme en ligne de commande utilisé pour convertir du texte d'un encodage de caractères à un autre. Il peut être utilisé pour convertir des fichiers texte d'un encodage à un autre, ou pour effectuer des conversions de jeux de caractères lors du déplacement de texte entre différents systèmes d'exploitation ou applications. Il est utile pour copier des fichiers de Linux vers Windows, car il peut encoder des fichiers powershell et les exécuter sur la machine Windows.

  Command Reference:

    Copy file from Linux to Windows

    File to copy: powershell.ps1
        
    encoding: UTF-16LE

    Windows command: powershell <base64> -enc

command: |
  cat powershel.ps1 |iconv -t UTF-16LE |base64 -w 0

items:
  - Shell
services:
OS:
  - Windows
  - Approved-tool
attack_types:
  - General
references:
  - https://www.gnu.org/savannah-checkouts/gnu/libiconv/documentation/libiconv-1.17/iconv.1.html#SEC7
---