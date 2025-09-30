In this challenge we have to append the flag to /challenge/run.
## My Solve

**Flag:**pwn.college{saUfZs6ppBe1BBm4bf1Cva9dFza.QX3ATO0wCN4kjNzEzW}
In this challenge, I used the >> character to append the flag to /challenge/run and then used the cat command to get the flag.
```bash
hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
hacker@piping~appending-output:~$ cat  /home/hacker/the-flag
 |
\|/ This is the first half:
 v
pwn.college{saUfZs6ppBe1BBm4bf1Cva9dFza.QX3ATO0wCN4kjNzEzW}
                              ^
     that is the second half /|\
                              |
```

## What I Learned
Through this challenge, I was able to learn that you can redirect input in append mode using >> character.
## Refernces
Did not use any references for this challenge.

