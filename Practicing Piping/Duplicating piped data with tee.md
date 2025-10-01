In this challenge we have to pipe a secret value from /challenge/pwn to /challenge/college.
## My Solve

**Flag:**pwn.college{sEOqEDEHgoaABgjEZ72i16b6erG.QXxITO0wCN4kjNzEzW}
In this challenge, I used the pipe operator first and then wrote cat pwn to get the secret code and then again used the pipe operator to get the flag.
```bash
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee pwn | /challenge/college
hacker@piping~duplicating-piped-data-with-tee:~$ cat pwn
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "sEOqEDEH"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret sEOqEDEH | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{sEOqEDEHgoaABgjEZ72i16b6erG.QXxITO0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that the tee operator we can make multiple copies of the piped in data.
## Refernces
Did not use any references for this challenge.
