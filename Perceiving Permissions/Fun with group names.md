In this challenge we have to find the name of the random group that the user is in and get the flag.
## My Solve

**Flag:**pwn.college{c2FVif16JdgIKOSfE7kP3VpLdSK.QXycjM1wCN4kjNzEzW}
In this challenge, I used id to find the name of the group, then I used the chgrp command to change the group and then I used cat command to get the flag.
```bash
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp9094) groups=1000(grp9094)
hacker@permissions~fun-with-groups-names:~$ chgrp grp9094 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{c2FVif16JdgIKOSfE7kP3VpLdSK.QXycjM1wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that id is used to check the group which we are a part of.
## Refernces
Did not use any references for this challenge.
