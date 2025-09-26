In this challenge we have to search for the hidden file.
## My Solve

**Flag:**pwn.college{AbxVhpo7F0zsYWueXiZQla86JoR.QXwUDO0wCN4kjNzEzW}
In this challenge, I used the ls -a command to find the hidden file. The flag was hidden as a dot-prepended file. Then I used cd to find the flag.
```bash
hacker@commands~hidden-files:~$ ls -a /
.   .dockerenv           bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-5966866810710  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:~$ /.flag-5966866810710
bash: /.flag-5966866810710: Permission denied
hacker@commands~hidden-files:~$ cat /.flag-5966866810710
pwn.college{AbxVhpo7F0zsYWueXiZQla86JoR.QXwUDO0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that the ls -a command will search for the hidden file.

## Refernces
Did not use any references for this challenge.
