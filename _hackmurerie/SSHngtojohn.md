---
description: |
  sshng2john est un outil utilisé pour convertir les clés privées SSH au format OpenSSH dans un format qui peut être craqué à l'aide d'outils de craquage de mots de passe tels que John the Ripper. Cela peut finalement permettre de craquer le mot de passe de la clé privée.

  Command Reference:

    Private SSH key: id_rsa

command: |
  sshng2john.py id_rsa

code: |
  john --wordlist=/opt/wordlists/rockyou.txt sshkey.john

items:
  - SSH_key
services:
  - SSH
OS:
  - Windows
  - Linux
  - Approved-tool
attack_types:
  - Cracking
references:
  - https://github.com/truongkma/ctf-tools/blob/master/John/run/sshng2john.py
  - https://github.com/Kyuu-Ji/htb-write-up/blob/master/tenten/write-up-tenten.md
---