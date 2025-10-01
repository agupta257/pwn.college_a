In this challenge we have to redirect the output of /challenge/run to myflag and the errors to instructions.
## My Solve

**Flag:** pwn.college{AkvtQYs_nWZ_dEyTlOvRS2_Twq_.QX3YTN0wCN4kjNzEzW}
In this challenge, I used > character to redirect the output and errors using > character.
```bash
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{AkvtQYs_nWZ_dEyTlOvRS2_Twq_.QX3YTN0wCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn that using 2 before > character would redirect the errors to thjat file.
## Refernces
Did not use any references for this challenge.
