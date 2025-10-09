In this challenge we have to check three screen sessions for the flag.
## My Solve

**Flag:**pwn.college{gmpuAFLvfKESVHDAfjIjbEF9-H7.01N4IDOxwCN4kjNzEzW}
In this challenge, I first used ls for the screen to check which sessions are detatched. Then I used screen -r for each one of them to find the one which has the flag.
```bash
hacker@terminal-multiplexing~finding-sessions:~$ screen -ls
hacker@terminal-multiplexing~finding-sessions:~$ screen -r session_e2fc63d3e7b06fdf
hacker@terminal-multiplexing~finding-sessions:~$ screen -r session_c5dc21a101e0c07a
hacker@terminal-multiplexing~finding-sessions:~$ screen -r session_51a8f6d32e5fa28f
```

## What I Learned
Through this challenge, I was able to learn to find the right session to reattach to in cause of multiple sessions running in background.
## Refernces
Did not use any references for this challenge.
