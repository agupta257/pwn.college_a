In this challenge we have to redirect the output of /challenge/hack to /challenge/planet and /challenge/the simultaneously.
## My Solve

**Flag:**pwn.college{IN1gcN6oJl_TkThMotR7cdcpKxc.QXwgDN1wCN4kjNzEzW}.
```bash
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >( /challenge/the ) | /challenge/planet
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{IN1gcN6oJl_TkThMotR7cdcpKxc.QXwgDN1wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn to use multiple commands.
## Refernces
Did not use any references for this challenge.
