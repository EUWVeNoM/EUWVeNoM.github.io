---
description: |
  Cette fonction est utile pour deviner les comptes d'utilisateurs/mots de passe par la force brute et pour énumérer les noms d'utilisateurs lorsque ces derniers sont basés sur les noms des utilisateurs. En essayant quelques mots de passe faibles sur un grand nombre de comptes d'utilisateurs, les seuils de verrouillage des comptes d'utilisateurs peuvent être évités.

  Command Reference:
  ```
  Firstname: maurits

  Lastname: maas
  ```
command: |
  ./username-anarchy maurits maas

items:
  - Password
  - Username
  - No_creds
services:
  -
OS:
  - Windows
  - Linux
  - Approved-tool
attack_types:
  - Cracking
  - Enumeration
references:
  - https://github.com/urbanadventurer/username-anarchy
---