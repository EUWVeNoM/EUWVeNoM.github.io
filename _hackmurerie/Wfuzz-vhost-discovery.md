---
description: |
  Wfuzz a été créé pour faciliter la tâche dans les évaluations d'applications web et repose sur un concept simple : il remplace toute référence au mot-clé FUZZ par la valeur d'une charge utile don

  Command Reference:

    -u for target site: http://flight.htb/

    -w for wordlist: https

    Placeholder for vhosts (-H): FUZZ.flight.htb


command: |
  wfuzz -c -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-20000.txt -u "http://flight.htb/" -H "Host: FUZZ.flight.htb" --hl 154


items:
  - No_creds
services:
  - Web
OS:
  - Windows
  - Linux
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://github.com/xmendez/wfuzz
  - https://wfuzz.readthedocs.io/en/latest/
---