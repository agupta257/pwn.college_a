In this challenge we have to use = and - to do more radical permission changes and get the flag.
## My Solve

**Flag:**pwn.college{Y5zCo6sAcKiOhe_VRLQh_xKJUa5.QXzETO0wCN4kjNzEzW}
In this challenge, I followed the commands to get the flag.
```bash
hacker@permissions~permissions-setting-practice:~$ /challenge/run
hacker@permissions~permissions-setting-practice:~$ chmod u=x,g=rwx,o=rx /challenge/pwn
hacker@permissions~permissions-setting-practice:~$ chmod u=wx,g=-,o=- /challenge/pwn
hacker@permissions~permissions-setting-practice:~$ chmod u=-,g=rwx,o=r /challenge/pwn
hacker@permissions~permissions-setting-practice:~$ chmod u=wx,o=w /challenge/pwn
hacker@permissions~permissions-setting-practice:~$ chmod u=rx,g=wx,o=r /challenge/pwn
hacker@permissions~permissions-setting-practice:~$ chmod u=rwx,g=-,o=rw /challenge/pwn
hacker@permissions~permissions-setting-practice:~$ chmod u=x,o=w /challenge/pwn
hacker@permissions~permissions-setting-practice:~$ chmod u=x,g=rx,o=r /challenge/pwn
hacker@permissions~permissions-setting-practice:~$ chmod u=r /flag
hacker@permissions~permissions-setting-practice:~$ cat /flag
pwn.college{Y5zCo6sAcKiOhe_VRLQh_xKJUa5.QXzETO0wCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn that using = with chmod can set the permissions altogether, overwriting the old ones.
## Refernces
Did not use any references for this challenge.
