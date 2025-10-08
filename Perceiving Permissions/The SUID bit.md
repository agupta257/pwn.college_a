In this challenge we have to add the SUID bit to the /challenge/getroot program in order to spawn a root shell for us and then get the flag.
## My Solve

**Flag:**pwn.college{gr-uzxI2-PJQIjeYaFiPrh0F4YP.QXzEjN0wCN4kjNzEzW}
In this challenge, I followed the commands to get the flag.
```bash
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root!
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{gr-uzxI2-PJQIjeYaFiPrh0F4YP.QXzEjN0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn to set a files's SUID bit by using chmod.

## Refernces
Did not use any references for this challenge.
