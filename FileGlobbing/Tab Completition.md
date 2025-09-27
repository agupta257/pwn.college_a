In this challenge we have to complete the file name using tab and then get the flag.
## My Solve

**Flag:**pwn.college{gBjsYqt-msnGlniyuQ_1jkN5sUb.0FN0EzNxwCN4kjNzEzW}
In this challenge, I first used cd to get into the /challenge directroy and then i wrote cat pwn and pressed tab which completed it to pwncollege and then 
pressed enter to get the flag.
```bash
hacker@globbing~tab-completion:~$ cd /challenge
hacker@globbing~tab-completion:/challenge$ ls
DESCRIPTION.md  pwncollege​
hacker@globbing~tab-completion:/challenge$ cat pwncollege​
pwn.college{gBjsYqt-msnGlniyuQ_1jkN5sUb.0FN0EzNxwCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn that if you hit tab in the shell, it'll try to figure out what you're going to type and automatically complete it. 
## Refernces
Did not use any references for this challenge.
