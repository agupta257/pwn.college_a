In this challenge we have to change the owner of /flag to hacker and then get the flag.
## My Solve

**Flag:**pwn.college{kea8JT23xxOBgRi6zFhEV3OXnOs.QXxEjN0wCN4kjNzEzW}
In this challenge, I first changed the owner of /flag to hacker using the chown command and then I used the cat command to get the flag.
```bash
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{kea8JT23xxOBgRi6zFhEV3OXnOs.QXxEjN0wCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn that chown is used to changed the owner of a file/directory.

## Refernces
Did not use any references for this challenge.
