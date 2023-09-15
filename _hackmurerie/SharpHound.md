---
description: |
  SharpHound.exe est le collecteur de données officiel de BloodHound. Il est écrit en C# et utilise les fonctions de l'API Windows et les fonctions de l'espace de noms LDAP pour collecter des données à partir des contrôleurs de domaine et des systèmes Windows reliés à un domaine. Ces données peuvent ensuite être introduites dans BloodHound afin d'énumérer les voies potentielles d'escalade des privilèges. La commande suivante exécute toutes les méthodes de collecte et stocke les résultats dans un fichier zip qui peut être placé directement dans l'interface graphique de BloodHound.

  Command Reference:

  	Output File: output.zip

command: |
  SharpHound.exe --CollectionMethod All --ZipFileName output.zip
items:
  - Shell
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
