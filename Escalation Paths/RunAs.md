RunAs command allows us to run a command as somebody else.

HTB Box to Practice: Access

Note: You should be looking for a **cmdkey /list** This is a command which will be looking for stored credentials on a machine.

Note for getting low level user on this machine: you can read mdb files using mdb-sql and pst files as readpst on the linux command line.

The command that you will run is:

```powershell
C:\Windows\System32\runas.exe /user:ACCESS\Administrator /savecred "C:\Windows\System32\cmd.exe /c TYPE C:\Users\Administrator\Desktop\root.txt > C:\Users\security\root.txt"
```

So... you're running runas.exe and you're using user: ACCESS\Administrator and with this, you want to run savecred. Savecred is basically saying hey, save this credential for me. Then we're running command prompt, /c means copy then you're going to copy the root.txt file from the admistrator user to the low level user.