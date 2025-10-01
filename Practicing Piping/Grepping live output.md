In this challenge we have to find the flag using | operator and grep command.
## My Solve

**Flag:**pwn.college{EG5rBmOFfyN_oP1XtbWAPZwtgY2.QX5EDO0wCN4kjNzEzW}
In this challenge, I used the | operator to directly send the output of /challenge/run to grep.
```bash
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college
```

## What I Learned
Through this challenge, I was able to learn that the | operator connects standard output from the command to the left to the standard input of the command to the right.
## Refernces
Did not use any references for this challenge.
