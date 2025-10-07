In this challenge we have to change the group ownership of /flag to hacker and read the flag.
## My Solve

**Flag:**pwn.college{weE4LvgoEbU8_tNZyq5huX6DBjb.QXxcjM1wCN4kjNzEzW}
In this challenge, I used the chgrp command to change the group ownership of /flag and then used cat command to get the flag.
```bash
hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{weE4LvgoEbU8_tNZyq5huX6DBjb.QXxcjM1wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that chgrp is used to change the group ownership of a file/directory.

## Refernces
Did not use any references for this challenge.
