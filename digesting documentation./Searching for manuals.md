In this challenge we have to search for the right man page and then get the flag.
## My Solve

**Flag:**pwn.college{w4eDAn4cBcB8EL55uXdgMtmzai_.QX2EDO0wCN4kjNzEzW}
In this challenge, I first used man man and then in it I found the command man -k printfile to search for a particular keyword. Then i worte man -k challenge to find out the correct manual. Using that manual, I was
able to find the --wenccu NUM argument which helped me to print the flag.
```bash
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k challenge
wenccudgtm (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man wenccudgtm
hacker@man~searching-for-manuals:~$ /challenge/challenge --wenccu 448
Correct usage! Your flag: pwn.college{w4eDAn4cBcB8EL55uXdgMtmzai_.QX2EDO0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that the man man command teaches us the advanced usage of the man command.

## Refernces
Did not use any references for this challenge.
