# HTB: Fawn

File Transfer Protocol

1. On peut utiliser ftp pour telecharger des documents
2. si nmap montre anonymous: login: anonymous; pw: <Enter>

- find version: ```nmap -sV -sC -v 10.129.148.247```
- get flag: ```ftp 10.129.148.247; get flag.txt```

[HTB: Fawn Walkthrough](https://www.youtube.com/watch?v=kSvvGV-_7n8)

