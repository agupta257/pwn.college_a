In this challenge we have to run /challenge/run such that it runs the win command.
## My Solve

**Flag:**pwn.college{sU1Iw30-OnhUtZd5FQg7annQI5S.QX1cjM1wCN4kjNzEzW}
In this challenge, I used the PATH variable to use /challenge/more_commands/ directory as the path so that /challenge/run runs the win command.
```bash
hacker@path~setting-path:~$ PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{sU1Iw30-OnhUtZd5FQg7annQI5S.QX1cjM1wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that using PATH variable would help us define the path for a command to run.
## Refernces
Did not use any references for this challenge.
