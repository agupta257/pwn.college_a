In this challenge we have to find the option that will give you the flag by reading the challenge man page.
## My Solve

**Flag:**pwn.college{8p3UwD9AV379dSzFKANBdUTh4nT.QX1EDO0wCN4kjNzEzW}
In this challenge, I first opened the manual of challenge and the used / to search for the word 'flag' the I used n to go to the next search. Doing this, I found the --qq argument which would print the flag.
```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --qq
Initializing...
Correct usage! Your flag: pwn.college{8p3UwD9AV379dSzFKANBdUTh4nT.QX1EDO0wCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn how to search for a particular word in the manual.
## Refernces
Did not use any references for this challenge.
