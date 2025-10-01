In this challenge we have to redirect the PWN file to /challenge/run and have the PWN file contain the value COLLEGE.
## My Solve

**Flag:**pwn.college{IYjbF9UReBByQ4qKkYNV8gyC8x7.QXwcTN0wCN4kjNzEzW}
In this challenge, I used the echo command and > character to have the PWN file contain the value COLLEGE and the I redirected PWN file to /challenge/run using < character.
```bash
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{IYjbF9UReBByQ4qKkYNV8gyC8x7.QXwcTN0wCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn that the < character is used to redirect input to programs.
## Refernces
Did not use any references for this challenge.
