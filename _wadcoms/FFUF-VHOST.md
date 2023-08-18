---
description: |
  FFUF, ou "Fuzz Faster you Fool" est un outil de fuzzing web open source, destiné à découvrir des éléments et du contenu au sein d'applications web, ou de serveurs web. Qu'entendons-nous par là ? Souvent, lorsque vous visitez un site web, le propriétaire du site vous présente le contenu qu'il souhaite vous offrir, qui peut être hébergé sur une page telle que index.php. Dans le cadre de la sécurité, les problèmes d'un site web qui doivent être corrigés existent souvent en dehors de cette page. Par exemple, le propriétaire du site web peut avoir du contenu hébergé sur admin.php, que vous voulez tous deux connaître et tester. FFUF est un outil qui permet de découvrir ces éléments, à votre intention.

  Command Reference:

    Domain: <domain.local>

    Dictionnaire: <dict>

command: |
  - ffuf -w <dict> -u http://<domain.local>/ -H "Host: FUZZ.<domain.local>"
items:
  - No_Creds
services:
  - HTTP
attack_types:
  - Enumeration
OS:
  - Linux
references:
  - https://github.com/ffuf/ffuf
  - https://cheatsheet.haax.fr/web-pentest/tools/ffuf/
---
