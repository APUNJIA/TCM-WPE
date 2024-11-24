Resources for Potato Attack: 

Rotten Potato - [https://foxglovesecurity.com/2016/09/26/rotten-potato-privilege-escalation-from-service-accounts-to-system/](https://foxglovesecurity.com/2016/09/26/rotten-potato-privilege-escalation-from-service-accounts-to-system/)

Juicy Potato - [https://github.com/ohpe/juicy-potato](https://github.com/ohpe/juicy-potato)

How this works on a high level:

1. Trick the "NT AUTHORITY\SYSTEM" account into authenticating via NTLM to a TCP endpoint we control
2. MITM this authentication attempt(NTLM relay) to locally negotiate a security token for the "NT AUTHORITY\SYSTEM" account. This is done through a series of Windows API calls
3. Impersonate the token we have just negotiated. This can only be done if the attackers' current account has the privilege to impersonate security tokens. This is usually true for most service accounts and not true for most user-level accounts.

HTB Machine: Jeeves

Quick note for this machine: This machine uses alternate data streams to store data. In order to access hidden data, you can run this command:

```
DIR /R
```

Then you can access the data in the root.txt file by this command:

```
more < location_of_the_file
```

