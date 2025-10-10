In this challenge we have to find the path of the win file in which the flag is stored.
## My Solve

**Flag:**pwn.college{0JI07eErVyF2IJqhcOUmBlThmrK.01NzEzNxwCN4kjNzEzW}
In this challenge, I used the which command to find the path of the win file. Then is used cd for that file and wrote cat flag to get the flag.
```bash
hacker@path~finding-commands:~$ which win
/challenge/paths/15251/win
hacker@path~finding-commands:~$ cd /challenge/paths/15251
hacker@path~finding-commands:/challenge/paths/15251$ cat flag
pwn.college{0JI07eErVyF2IJqhcOUmBlThmrK.01NzEzNxwCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that the which command helps to find the path in which a file is stored.
## Refernces
Did not use any references for this challenge.
