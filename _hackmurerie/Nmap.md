---
description: |
  Nmap est un scanner de ports libre créé par Fyodor et distribué par Insecure.org. Il est conçu pour détecter les ports ouverts, identifier les services hébergés et obtenir des informations sur le système d'exploitation d'un ordinateur distant. Ce logiciel est devenu une référence pour les administrateurs réseaux car l'audit des résultats de Nmap fournit des indications sur la sécurité d'un réseau. Il est disponible sous Windows, Mac OS X, Linux, BSD et Solaris.

  Le code source de Nmap est disponible sous la licence GNU GPL jusqu'à la version 7.90. Il est désormais distribuée sous la Nmap Public Source License (NPSL), qui est basée sur la GPLv2 mais ajoute des restrictions qui la rendent non-libre4.  

  Command Reference:

  	Target IP: <IP>

command: |
  nmap -p- -sC -sV -sS <IP>
items:
  - No_Creds
services:
attack_types:
  - Enumeration
OS:
  - Linux
  - Windows
  - Approved-tool
references:
  - https://nmap.org/man/fr/index.html
  - https://hackertarget.com/nmap-cheatsheet-a-quick-reference-guide/
---
