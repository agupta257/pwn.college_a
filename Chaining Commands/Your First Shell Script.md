In this challenge we have to run /challenge/pwn and then /challenge/college, in a shell script called x.sh, then run it with bash.
## My Solve

**Flag:**pwn.college{s0sBmQWqBCjyCF_Xnhi8YzbgYvZ.QXxcDO0wCN4kjNzEzW}
In this challenge, I followed the commands to get the flag.
```bash
hacker@chaining~your-first-shell-script:~$ echo "/challenge/pwn" > x.sh
hacker@chaining~your-first-shell-script:~$ echo "/challenge/college" >> x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{s0sBmQWqBCjyCF_Xnhi8YzbgYvZ.QXxcDO0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that we can create a shell script by suffixing the name with sh and we can execute them passing it as an argument to a new instance of our shell.
## Refernces
Did not use any references for this challenge.
