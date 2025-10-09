In this challenge we have to detach the screen, run /challenge/run and then reattach it.
## My Solve

**Flag:** pwn.college{ksnrStwD4COIHyEDNQx565FtWqK.0lN4IDOxwCN4kjNzEzW}
In this challenge, I first launched the screen, then I detached it using Ctrl+A after that I pressed d. Then I wrote /challenge/run and reattached it by typing screen -r. Doing this, I got the flag.
```bash
hacker@terminal-multiplexing~detaching-and-attaching:~$ /challenge/run
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen -r
```

## What I Learned
Through this challenge, I was able to learn to detach and reattach the screen and that any command typed after detaching it, runs in the background.
## Refernces
Did not use any references for this challenge.
