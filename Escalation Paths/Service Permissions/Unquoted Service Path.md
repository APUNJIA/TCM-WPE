THM Paid: SteelMountain

So if you have a service executable for which path is not enclosed in quotation marks and contains a space, we have a problem here

So basically if you go to regedit and go to this location you will see all the unquoted service paths:

```
Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\service\unquotedsvc
```

Basically what the issue here is since the path is not quoted, windows will try to go through it this way instead of going directly to the service path that the file is saved in:

C:\Program.exe -> C:\Program File.exe -> C:\Program File\Unquoted.exe and so on 

So, we can get malicious with it because of this, we can make a file called C:\Program Files\Unquoted Path Service\Common.exe and that will run before the actual application.

