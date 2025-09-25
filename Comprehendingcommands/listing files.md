In this challenge we have to find the renamed directory of /challenge/run using the ls comannd.
## My Solve
**Flag:**pwn.college{YMMpoVLLhCA3DBkbLnVZZSHvB5T.QX4IDO0wCN4kjNzEzW}
In this challenge, I used the ls command to find the renamed directory of /challenge/run and then wrote the renamed version to get the flag.
```bash
hacker@commands~listing-files:~$ ls /challenge
7561-renamed-run-14886  DESCRIPTION.md
hacker@commands~listing-files:~$
hacker@commands~listing-files:~$ /challenge/7561-renamed-run-14886
Yahaha, you found me! Here is your flag:
pwn.college{YMMpoVLLhCA3DBkbLnVZZSHvB5T.QX4IDO0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that the ls command lists the contents of a directory.

## Refernces
Did not use any references for this challenge.
