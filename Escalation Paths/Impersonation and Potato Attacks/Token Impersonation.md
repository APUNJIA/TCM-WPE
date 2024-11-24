What are tokens?

They are temporary keys that allow you access to a system/network without having to provide credentials each time you access a file. Think cookies for computers

There are two types of tokens:

1. Delegate tokens: Created for logging into a machine or using Remote Desktop(most often)
2. Impersonate: 'non-interactive' such as attaching a network drive or a domain logon script

Resources: https://www.offensive-security.com/metasploit-unleashed/fun-incognito

Why this is bad?

You can use tokens to pop a shell and load incognito. Then you can impersonate our domain user(using incognito). Then you can attempt to dump hashes as non-Domain Admin(using mimikatz from PEH course).

Imagine if you can do that if a Domain Admin token was available?

You can impersonate as the domain admin.

Payload all the things from [[Resources]]