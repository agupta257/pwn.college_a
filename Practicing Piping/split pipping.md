In this challenge we have to redirect the stderr of /challenge/hack to /challenge/the and stdout of /challenge/hack to /challenge/planet.
## My Solve

**Flag:**pwn.college{o-Yh8eDOKLgVUkOlOh51KvHzsAT.QXxQDM2wCN4kjNzEzW}
```bash
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >( /challenge/planet ) 2> >( /challenge/the )
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{o-Yh8eDOKLgVUkOlOh51KvHzsAT.QXxQDM2wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn to redirect stderr and stdout of /challenge/hack to two different commands.
## Refernces
Did not use any references for this challenge.
