In this challenge we have to find the flag using grep and | operator by redirecting file descriptor 2 to file descriptor 1.
## My Solve

**Flag:**pwn.college{4qSB0FuH0-31RaHxJDr-oUZa29x.QX1ATO0wCN4kjNzEzW}
In this challenge, I used the >& operator to redirect file descriptor 2 to file descriptor 1 and then got the flag using grep command and pipe operator.
```bash
hacker@piping~grepping-errors:~$ /challenge/run 2>& 1 | grep pwn.college
```

## What I Learned
Through this challenge, I was able to learn that the >& operator redirects a file descriptor to another file descriptor.
## Refernces
Did not use any references for this challenge.
