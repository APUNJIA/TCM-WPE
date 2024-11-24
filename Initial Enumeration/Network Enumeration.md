First and foremost:

```
ipconfig /all
```

same as ifconfig -a on Linux

You can also look at the arp table of the network by this command:

```
arp -a
```

If you see a 2 or a 255 at the end of the IP address here, its nothing out of the ordinary.

You should also look at the routing table which can be seen by:

```
route /print
```

This command is also important:

```
netstat -ano
```

This basically shows what ports are out there. So that we can possibly exploit them and shit.


