In this challenge This challenge has a /challenge/files directory with a bunch of files starting with pwncollege. We have to
tab-complete from /challenge/files/p and make our way to the flag!
## My Solve
**Flag:**pwn.college{gnhFWZMxvjvf2-zmRKy1fxuTiMO.0lN0EzNxwCN4kjNzEzW}
In this challenge, I wrote cat pwn and then used tab multiple times to reach to pwncollege-flag and then wrote cat pwncollege-flag and pressend enter to get the flag.
```bash
hacker@globbing~multiple-options-for-tab-completion:~$ cd /challenge/files
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwn
pwn                    pwn-the-planet         pwncollege-flag        pwncollege-flyswatter
pwn-college            pwncollege-family      pwncollege-flamingo    pwncollege-hacking
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwn
pwn                    pwn-the-planet         pwncollege-flag        pwncollege-flyswatter
pwn-college            pwncollege-family      pwncollege-flamingo    pwncollege-hacking
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwncollege-
pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter  pwncollege-hacking
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwncollege-fla
pwncollege-flag      pwncollege-flamingo
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwncollege-flag
pwn.college{gnhFWZMxvjvf2-zmRKy1fxuTiMO.0lN0EzNxwCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that pressing tab will print out all the options that matches the given input.
## Refernces
Did not use any references for this challenge.
