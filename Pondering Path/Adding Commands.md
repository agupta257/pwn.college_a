In this challenge we have to find the path of the win file that gives the flag when /challenge/run is run.
## My Solve

**Flag:**pwn.college{ItVdTYx9gQvpxrcyb0tQRwngOnp.QX2cjM1wCN4kjNzEzW}
In this challenge, I set the PATH for win and made it exectuable for all using the chmod command. Then I wrote /challenge/run to get the flag.
```bash
hacker@path~adding-commands:~$ PATH=$PATH:/home/hacker
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
/challenge/run: line 4: /home/hacker/win: Permission denied
It looks like that did not work... Did you set PATH correctly?
hacker@path~adding-commands:~$ cat $PATH
cat: '/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/home/hacker:/home/hacker': No such file or directory
hacker@path~adding-commands:~$ chmod +x win
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{ItVdTYx9gQvpxrcyb0tQRwngOnp.QX2cjM1wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn how to add the location of a shell script to its path.

## Refernces
Did not use any references for this challenge.
