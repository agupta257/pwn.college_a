In this challenge we have to read the manual page of challenge and get the flag.
## My Solve

**Flag:**pwn.college{cZJ2McD4F1tl0agKD0_M42IMfYZ.QX0EDO0wCN4kjNzEzW}
In this challenge, I first used the man command to open the manual page of challenge. Then I used the --cctlag argument which was mentioned in the manual page and took the NUM as 241 to get the flag.
```bash
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --cctlag 241
Correct usage! Your flag: pwn.college{cZJ2McD4F1tl0agKD0_M42IMfYZ.QX0EDO0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that the man command opens the manual page of the challenge and I was able to learn about the --cctalg NUM argument.
## Refernces
Did not use any references for this challenge.
