Basically WSL allows you to run Linux on top of Windows.

If we have a potential wsl escalation, we should have wsl.exe and bash.exe in the windows machine. 

To find where bash.exe is:

```
where /R c:\windows bash.exe
```

Run the same thing for wsl.exe

You can then run the wsl.exe by pasting the location and then putting a command in the end like whoami.

If you look at the cheat sheet, you can find that you can run a python reverse shell if the above instruction gives you a root or something similar.

You can then just run the bash.exe file by just putting the location of the file in the command line and a shell will spawn.

But dont let this fool you, you are in Linux not in Windows and you need to escalate privileges in Windows not Linux.

Since we are in a non tty shell, we need to escape this, so for that, we can run:

```
python -c "import pty;pty.spawn('/bin/bash')"
```

Then you need to escape this tty shell for that you can look up tty escape cheat sheet and then follow the guide by net sec i suppose.

Spawning a TTY Shell - [https://netsec.ws/?p=337](https://netsec.ws/?p=337)

Impacket Toolkit - [https://github.com/SecureAuthCorp/impacket](https://github.com/SecureAuthCorp/impacket)

HTB Box to Practice: SecNotes