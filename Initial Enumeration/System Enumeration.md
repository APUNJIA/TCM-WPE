Remember from the PEH course that you can run the following NMAP scan on a machine using the following command if you know its IP address:

```bash
nmap -A -T4 -p- <IP>
```

Then you can exploit the ports that you find and doing initial enumeration to get low level access on the machine. Then you can do the next steps to enumerate to gain privilege.

 The first step to find information about the system is to run the command:

```
systeminfo
```

We can also look how well patched the system is by using a command called:

```
wmic qfe
```

wmi stands for windows management instrumentation and c here is for command line. qfe stands for quick fix engineering.

It basically returns information about the system that it is running on.

We can also look at what drives are connected to the system by running:

```
wmic logicaldisk get caption,description,providername
```



