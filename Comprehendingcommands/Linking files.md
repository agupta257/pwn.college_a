In this challenge we have to find the flag using symlink.
## My Solve

**Flag:**pwn.college{8GiXwPst97ey3YItnvxKO5bg8Wd.QX5ETN1wCN4kjNzEzW}
In this challenge, I first removed /home/hacker/not-the-flag using thr rm command. Then I linked /flag and /challenge/catflag using symlink. Then I preintyed the flag
by typing /challenge/catflag.
```bash
hacker@commands~linking-files:~$ rm /home/hacker/not-the-flag
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{8GiXwPst97ey3YItnvxKO5bg8Wd.QX5ETN1wCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn that ln -s command is used to create a symlink between two directories.
## Refernces
Did not use any references for this challenge.
