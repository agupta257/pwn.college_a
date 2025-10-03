In this challenge we have to interrupt /challenge/run.
## My Solve

**Flag:**pwn.college{MNK1gtta7B0tWu50y1cblNA55js.QXzQDO0wCN4kjNzEzW}
In this challenge, I first wrote /challenge/run and then used Ctrl-C to interrupt it.
```bash
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{MNK1gtta7B0tWu50y1cblNA55js.QXzQDO0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that Ctrl-C sends an interrupt to whatever application is waiting on input from the terminal and this causes the application to cleanly exit.

## Refernces
Did not use any references for this challenge.
