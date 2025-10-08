In this challenge we have to make /challenge/run executable and then get the flag.
## My Solve

**Flag:**pwn.college{A0JWPI5cuJ5ptZz08GqCelNbrSF.QXyEjN0wCN4kjNzEzW}
In this challenge, I used the chmod command to make /challenge/flag executable for everyone.
```bash
hacker@permissions~executable-files:~$ chmod ugo+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{A0JWPI5cuJ5ptZz08GqCelNbrSF.QXyEjN0wCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn to change the file permissions to make the directory executable using chmod command.

## Refernces
Did not use any references for this challenge.
