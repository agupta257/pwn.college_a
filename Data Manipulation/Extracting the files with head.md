In this challenge we have to find the flag by piping the first 7 lines of /challenge/pwn to /challenge/college.
## My Solve

**Flag:**pwn.college{EJZBYG9Si76fEu1zuOUBpot44KP.0lNxEzNxwCN4kjNzEzW}
In this challenge, I used the head command to get the first 7 lines of /challenge/pwn and then used | to pipe then to /challenge/college.
```bash
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{EJZBYG9Si76fEu1zuOUBpot44KP.0lNxEzNxwCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that the head command is used to get the early output of a program.

## Refernces
Did not use any references for this challenge.
