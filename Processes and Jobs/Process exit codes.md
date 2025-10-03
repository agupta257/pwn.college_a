In this challenge we have to  retrieve the exit code returned by /challenge/get-code and then run /challenge/submit-code with that error code as an argument.
## My Solve

**Flag:**pwn.college{8ojuVTxawXFlt150mqLjx-mBryt.QX5YDO1wCN4kjNzEzW}
In this challenge, I got the exit code returned by /challenge/get-code by using $? and then I used that code as an argument with /challenge/submit-code to get the flag.
```bash
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
57
hacker@processes~process-exit-codes:~$ /challenge/submit-code 57
CORRECT! Here is your flag:
pwn.college{8ojuVTxawXFlt150mqLjx-mBryt.QX5YDO1wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that $? is used to get the error code of a command.

## Refernces
Did not use any references for this challenge.
