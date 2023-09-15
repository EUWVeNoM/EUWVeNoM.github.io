---
description: |
  Ldapsearch est un outil basé sur Linux qui ouvre une connexion à un serveur LDAP, s'y attache et effectue une recherche en utilisant les paramètres spécifiés. La commande suivante tentera de trouver des informations sensibles (telles que des creds divulgués) en interrogeant tous les objets LDAP, ce qui revient à déverser toutes les données auxquelles un utilisateur anonyme peut avoir accès.

  Command Reference:

  	Domain: test.local

command: |
  ldapsearch -LLL -x -H ldap://test.local -b'' -s base '(objectclass=\*)'
items:
  - No_Creds
services:
  - LDAP
OS:
  - Linux
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://linux.die.net/man/1/ldapsearch
---
