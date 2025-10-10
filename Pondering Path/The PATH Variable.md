In this challenge we have to run /challenge/run such that it doesn't delete the flag.
## My Solve

**Flag:*pwn.college{sexfaXG3jnn748WNRjtOoNrkJ4z.QX2cDM1wCN4kjNzEzW}
In this challenge, I used the PATH variable for it to not remove the flag.
```bash
hacker@path~the-path-variable:~$ PATH=''
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{sexfaXG3jnn748WNRjtOoNrkJ4z.QX2cDM1wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that using PATH='' would make the program not look anywhere for the commands.
## Refernces
Did not use any references for this challenge.
