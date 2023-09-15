---
description: |
  John the Ripper est un outil populaire de craquage de mots de passe qui utilise une variété de techniques pour deviner les mots de passe. Lorsqu'il est utilisé pour casser une clé SSH, John peut tenter de deviner la phrase de passe utilisée pour chiffrer la clé privée, ce qui permet à un attaquant d'obtenir un accès non autorisé au serveur distant.

  Command Reference:
  ```
  Wordlist: /opt/wordlists/rockyou.txt

  Private SSH key in John format: sshkey.john
  ```
command: |
  john --wordlist=/opt/wordlists/rockyou.txt sshkey.john

code: |
  sshng2john.py id_rsa

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
  - https://github.com/openwall/john
  - https://null-byte.wonderhowto.com/how-to/crack-ssh-private-key-passwords-with-john-ripper-0302810/
  - https://github.com/Kyuu-Ji/htb-write-up/blob/master/tenten/write-up-tenten.md
---