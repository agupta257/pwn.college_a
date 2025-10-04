In this challenge we have to run /challenge/run in an another user account by finding out its password.
## My Solve

**Flag:**pwn.college{0Y4rHCqLDS8Z0PegUDRaV34Sizp.QX3UDN1wCN4kjNzEzW}
```bash
hacker@users~cracking-passwords:~$ cd /
hacker@users~cracking-passwords:/$ john ./challenge/shadow-leak
hacker@users~cracking-passwords:/$ su zardus
Password:aardvark
zardus@users~cracking-passwords:/$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{0Y4rHCqLDS8Z0PegUDRaV34Sizp.QX3UDN1wCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn that using john we can get the password of another user account.

## Refernces
Did not use any references for this challenge.
