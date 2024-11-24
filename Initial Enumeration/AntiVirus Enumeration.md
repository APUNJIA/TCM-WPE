You can find out about windows defender using this command:

```
sc query windefend
```

Lets say we dont know whats going on if there's some other AV in the machine. In that case, we can run this command for ex:

```
sc queryx type= service
```

If you want to look at firewall settings:

```
netsh advfirewall firewall dump
```

```
firewall show state
```

```
netsh firewall show config
```