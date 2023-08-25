---
description: |
  La commande atexec.py d'Impacket utilise le service de planification des tâches sur l'hôte Windows distant pour exécuter la commande donnée. Il créera une tâche Windows avec un nom aléatoire, déclenchera la tâche, puis la supprimera. La commande suivante exécute `whoami` sur l'hôte Windows distant.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Password: password123

  	Command Executed: whoami
command: |
  python3 atexec.py test.local/john:password123@10.10.10.1 whoami
items:
  - Password
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
