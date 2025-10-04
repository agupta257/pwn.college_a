In this challenge we have to get the flag in the root.
## My Solve

**Flag:**pwn.college{spCfvC5GYtxHfZNsh7tZjKp8Slh.QX1UDN1wCN4kjNzEzW}
In this challenge, I used su to go to the root, I entered the password hack-the-planet and used the cat command to get flag.
```bash
hacker@users~becoming-root-with-su:~$ su
Password:hack-the-planet
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{spCfvC5GYtxHfZNsh7tZjKp8Slh.QX1UDN1wCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn that su is used to become the root.

## Refernces
Did not use any references for this challenge.
