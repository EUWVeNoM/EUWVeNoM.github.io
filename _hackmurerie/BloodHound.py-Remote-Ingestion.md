---
description: |
  BloodHound est une application web Javascript d'une seule page, construite sur Linkurious, compilée avec Electron, avec une base de données Neo4j alimentée par un collecteur de données. BloodHound utilise la théorie des graphes pour révéler les relations cachées et souvent involontaires au sein d'un environnement Active Directory. Les attaquants peuvent utiliser BloodHound pour identifier facilement des chemins d'attaque très complexes qui seraient autrement impossibles à identifier rapidement. Les défenseurs peuvent utiliser BloodHound pour identifier et éliminer ces mêmes chemins d'attaque. Les équipes bleues et rouges peuvent utiliser BloodHound pour mieux comprendre les relations de privilèges dans un environnement Active Directory.

  BloodHound.py est un ingestor basé sur Python pour BloodHound, basé sur Impacket. Il vous permet de collecter à distance des données pour BloodHound en interrogeant LDAP.

  Command Reference:

  	Target IP: <IP>

  	Domain: <domain.local>

command: |
  bloodhound.py -d <domain.local> -v --zip -c All -dc <domain.local> -ns <IP>
items:
  - No_Creds
services:
  - LDAP
attack_types:
  - Enumeration
OS:
  - Linux
  - Windows
  - Approved-tool
references:
  - https://github.com/BloodHoundAD/BloodHound
  - https://github.com/fox-it/BloodHound.py
---
