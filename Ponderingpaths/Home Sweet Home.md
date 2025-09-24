In this challenge /challenge/run will write a copy of the flag to any file which we specify as an argument on the commandline.
## My Solve

**Flag:**pwn.college{Ekn4a8TI2IeQOtMbkN-NQ-PMPrU.QXzMDO0wCN4kjNzEzW}
In this challenge, I executed /challenge/run and then wrote an argument in the home directory.
```bash
hacker@paths~home-sweet-home:~$ /challenge/run
You must provide an argument to /challenge/run when you invoke it!
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{Ekn4a8TI2IeQOtMbkN-NQ-PMPrU.QXzMDO0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that /challenge/run will write a copy of the flag to the file in the home directory as an argument on the commandline.

## Refernces
Did not use any references for this challenge.
