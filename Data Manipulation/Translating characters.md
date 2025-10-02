In this challenge we have to print the flag but have to swap the casing of all characters.
## My Solve

**Flag:**pwn.college{IuLIqgKFOjcA-ubByjDpsn6fIMY.01MxEzNxwCN4kjNzEzW}
In this challenge, I used the tr command to swap the cases of all the alphabets.
```bash
hacker@data~translating-characters:~$ /challenge/run | tr 'ABCDEFGHIJKLMNOPQRSTUVWXYZ abcdefghijklmnopqrstuvwxyz' 'abcde
fghijklmnopqrstuvwxyz ABCDEFGHIJKLMNOPQRSTUVWXYZ'
yOUR CASE-SWAPPED FLAG:
pwn.college{IuLIqgKFOjcA-ubByjDpsn6fIMY.01MxEzNxwCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn that the tr command is used to translate the character provided in its first argument to the character provided in its second argument.

## Refernces
Did not use any references for this challenge.
