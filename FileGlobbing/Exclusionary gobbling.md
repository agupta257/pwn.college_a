In this challenge we have to run /challenge/run with all files that don't start with p, w, or n.
## My Solve

**Flag:**pwn.college{oVfvHNxBNXpA0GCnzV2CYuhz55G.QX2IDO0wCN4kjNzEzW}
In this challenge, I used the ! character inside the [] character at the start to not include the files that start with p,w or n.
```bash
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{oVfvHNxBNXpA0GCnzV2CYuhz55G.QX2IDO0wCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn If the first character in the brackets is a ! or ^, the glob inverts, and the
bracket instance matches characters that aren't listed.
## Refernces
Did not use any references for this challenge.
