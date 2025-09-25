In this challenge we have to move a file in a directory.
## My Solve

**Flag:**pwn.college{0lkWUdw3QHb8_z-Aj28lQ16AzfJ.0VOxEzNxwCN4kjNzEzW}
In this challenge, I used the mv command to move /flag file into /tmp/hack-the-planet and the wrote /challenge/check to get the flag.
```bash
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{0lkWUdw3QHb8_z-Aj28lQ16AzfJ.0VOxEzNxwCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn that the mv command moves files around.

## Refernces
Did not use any references for this challenge.
