In this challenge we have to switch from Window 1 to Window 0 to get the flag.
## My Solve

**Flag:** pwn.college{MM2dBaCKrTXwVReBM1_-z-zk5-a.0FO4IDOxwCN4kjNzEzW}
In this challenge, I first used ls to find the detached session. Then, I reattached into that session and then typed Ctrl+A 0 to switch to Window 0 to get the flag.
```bash
hacker@terminal-multiplexing~switching-windows:~$ screen -r challenge_session
```

## What I Learned
Through this challenge, I was able to learn to switch between different Windows.
## Refernces
Did not use any references for this challenge.
