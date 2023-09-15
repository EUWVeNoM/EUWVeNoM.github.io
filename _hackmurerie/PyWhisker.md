---
description: |
  pyWhisker est un outil permettant aux utilisateurs de manipuler l'attribut msDS-KeyCredentialLink d'un utilisateur/ordinateur cible afin d'obtenir un contrôle total sur cet objet. Il est basé sur Impacket et sur notre équivalent Python de DSInternals de Michael Grafnetter appelé PyDSInternals. Cet outil, ainsi que les PKINITtools de Dirk-jan, permettent une exploitation primitive complète sur les systèmes basés sur UNIX uniquement.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Password: password123

command: |
  python3 pywhisker.py -d "test.local" -u "john" -p "password123" --target "user2" --action "list" --dc-ip "10.10.10.1"
items:
  - Password
  - Username
services:
  - Kerberos
OS:
  - Linux
  - Approved-tool
attack_types:
  - Exploitation
references:
  - https://github.com/shutdownrepo/pywhisker
---
