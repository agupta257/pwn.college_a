In this challenge we have to access the variables in bash using the env command.
## My Solve

**Flag:**pwn.college{EjXzlTTZilULKoYGgKlcoVTFh1V.QX4UTN0wCN4kjNzEzW}
In this challenge, I wrote the env command and got the list of all the exported variables, in that list I found the flag.
```bash
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=11673958ab72f47b9e897a31a4af8ee453d4851335f1cbd7dd65c0d1f49a606f
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{EjXzlTTZilULKoYGgKlcoVTFh1V.QX4UTN0wCN4kjNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```

## What I Learned
Through this challenge, I was able to learn that the env command prints out every exported variable set in the shell.
## Refernces
Did not use any references for this challenge.

