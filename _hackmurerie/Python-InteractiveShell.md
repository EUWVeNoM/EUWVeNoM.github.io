---
description: |
  Commande Python pour créer un shell interactif à partir d'un simple shell. Le module pty vous permet de créer un psuedo-terminal qui peut tromper des commandes comme su en leur faisant croire qu'elles sont exécutées dans un vrai terminal.

  Command Reference:

    Variant of shell you will get: /bin/bash or /bin/sh

command: |
  python3 -c 'import pty;pty.spawn("/bin/bash")'

code: |
  python3 -c 'import pty;pty.spawn("/bin/bash")'

  ctrl + z

  stty raw -echo; fg 

items:
  - Shell
services:
  - 
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Persistence
  - General
references:
  - https://blog.ropnop.com/upgrading-simple-shells-to-fully-interactive-ttys/
---