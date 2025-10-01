In this challenge we have to use grep -v to filter out all the lines containing "DECOY" and reveal the real flag.
## My Solve

**Flag:**pwn.college{QitYpM3ofoZ0JvqYgnTAI3vott3.0FOxEzNxwCN4kjNzEzW}
In this challenge, I used the | operator and the grep -v command to filter out all the decoy flags and get the real flag.
```bash
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{QitYpM3ofoZ0JvqYgnTAI3vott3.0FOxEzNxwCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn that the grep -v command shows lines that do not match the given pattern.
## Refernces
Did not use any references for this challenge.
