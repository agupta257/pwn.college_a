In this challenge we have to read the output of the /challenge/run command directly into a variable called PWN.
## My Solve

**Flag:**pwn.college{8aMXK056PDtnd0o6y488PWdWQjP.QX1cDN1wCN4kjNzEzW}
In this challenge, I stored the output of /challenge/run in the variable called PWN and then used the echo command to get the flag.
```bash
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out
and submit it!
hacker@variables~storing-command-output:~$ echo "$PWN"
pwn.college{8aMXK056PDtnd0o6y488PWdWQjP.QX1cDN1wCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn to store command outputs in the form of variables.
## Refernces
Did not use any references for this challenge.
