In this challenge we have to get the permissions right eight times in a row and make /flag to make it readable for ourselves.
## My Solve

**Flag:**pwn.college{8fZKEJ_hePZGEDQDwHVqK2g8xPt.QXwEjN0wCN4kjNzEzW}
In this challenge, I followed the instructions to get to the flag.
```bash
hacker@permissions~permission-tweaking-practice:~$ /challenge/run
hacker@permissions~permission-tweaking-practice:~$ chmod g+w /challenge/pwn
hacker@permissions~permission-tweaking-practice:~$ chmod u-r /challenge/pwn
hacker@permissions~permission-tweaking-practice:~$ chmod u+r /challenge/pwn
hacker@permissions~permission-tweaking-practice:~$ chmod ugo-r /challenge/pwn
hacker@permissions~permission-tweaking-practice:~$ chmod o+x /challenge/pwn
hacker@permissions~permission-tweaking-practice:~$ chmod o-x /challenge/pwn
hacker@permissions~permission-tweaking-practice:~$ chmod u+rx /challenge/pwn
hacker@permissions~permission-tweaking-practice:~$ chmod g+r /challenge/pwn
hacker@permissions~permission-tweaking-practice:~$ chmod ugo+r /flag
hacker@permissions~permission-tweaking-practice:~$ cat /flag
pwn.college{8fZKEJ_hePZGEDQDwHVqK2g8xPt.QXwEjN0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn to use the chmod command more efficiently.
## Refernces
Did not use any references for this challenge.
