The main motivation of this topic is to think of passwords inside files. We can think of this like SAM files which store hashes on Windows(Active Directory portion in PEH). Passwords can also be stored in registries.

We can start things off with this command:

```
findsr /si password *.txt
```

Basically we are finding the password string in all .txt files

We can also add different file extensions at the end of our command here to broaden our search but it will take more time to search through the entire list.

Use [[Resources]] for all different payloads you can run.
