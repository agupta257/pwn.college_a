In this challenge we have to change the permissions of the /flag file to read it.
## My Solve

**Flag:**pwn.college{cwbf0rQ2bXkaYOtG76Cgjp6ZlF3.QXzcjM1wCN4kjNzEzW}
In this challenge, I used the chmod command to change the permissions of the flag to allow everyone to read the flag.
```bash
hacker@permissions~changing-permissions:~$ chmod ugo+r *
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{cwbf0rQ2bXkaYOtG76Cgjp6ZlF3.QXzcjM1wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that the chmod command is used to change the permissions of a file.

## Refernces
Did not use any references for this challenge.
