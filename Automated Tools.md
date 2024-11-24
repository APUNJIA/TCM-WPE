These tools are meant for enumeration.

Executables:
1. winPEAS.exe (.NET4 or greater or no work)
2. Seatbelt.exe(compile)
3. Watson.exe(compile)
4. SharpUp.exe(compile)

PowerShell:
1. Sherlock.ps1
2. PowerUp.ps1
3. jaws-enum.ps1

Other:
1. windows-exploit-suggester.py(local)
2. Exploit Suggester(Metasploit)

WinPEAS - [https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite/tree/master/winPEAS](https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite/tree/master/winPEAS)

Windows PrivEsc Checklist - [https://book.hacktricks.xyz/windows/checklist-windows-privilege-escalation](https://book.hacktricks.xyz/windows/checklist-windows-privilege-escalation)

Sherlock - [https://github.com/rasta-mouse/Sherlock](https://github.com/rasta-mouse/Sherlock)

Watson - [https://github.com/rasta-mouse/Watson](https://github.com/rasta-mouse/Watson)

PowerUp - [https://github.com/PowerShellMafia/PowerSploit/tree/master/Privesc](https://github.com/PowerShellMafia/PowerSploit/tree/master/Privesc)

JAWS - [https://github.com/411Hall/JAWS](https://github.com/411Hall/JAWS)

Windows Exploit Suggester - [https://github.com/AonCyberLabs/Windows-Exploit-Suggester](https://github.com/AonCyberLabs/Windows-Exploit-Suggester)

Metasploit Local Exploit Suggester - [https://blog.rapid7.com/2015/08/11/metasploit-local-exploit-suggester-do-less-get-more/](https://blog.rapid7.com/2015/08/11/metasploit-local-exploit-suggester-do-less-get-more/)

Seatbelt - [https://github.com/GhostPack/Seatbelt](https://github.com/GhostPack/Seatbelt)

SharpUp - [https://github.com/GhostPack/SharpUp](https://github.com/GhostPack/SharpUp)

Windows Exploit Suggester requires xlrd package from python so have that ready.

```
./windows-exploit-suggester.py --update 
pip install xlrd --upgrade
or...
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py: python get-pip.py
(if pip doesnt work)

```
