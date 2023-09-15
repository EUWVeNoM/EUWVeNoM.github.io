---
description: |
  SharpHound.exe est le collecteur de données officiel de BloodHound. Il est écrit en C# et utilise les fonctions de l'API Windows et les fonctions de l'espace de noms LDAP pour collecter des données à partir des contrôleurs de domaine et des systèmes Windows reliés à un domaine. Ces données peuvent ensuite être introduites dans BloodHound afin d'énumérer les voies potentielles d'escalade des privilèges. La commande suivante exécute toutes les méthodes de collecte et utilisera les informations d'identification LDAP fournies lors de l'exécution des méthodes de collecte LDAP, et stocke le résultat dans un fichier zip qui peut être directement placé dans l'interface graphique de BloodHound.

  Command Reference:

  	LDAP Username: john

  	LDAP Password: password123

  	Output File: output.zip

command: |
  SharpHound.exe --CollectionMethod All --LdapUsername john --LdapPassword password123 --ZipFileName output.zip
items:
  - Shell
  - Username
  - Password
services:
  - LDAP
OS:
  - Windows
  - Approved-tool
attack_types:
  - PrivEsc
  - Enumeration
references:
  - https://github.com/BloodHoundAD/SharpHound3
  - https://bloodhound.readthedocs.io/en/latest/data-collection/sharphound.html
---
