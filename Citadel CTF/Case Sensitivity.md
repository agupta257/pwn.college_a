You step into a constricted floor where every movement and operation is limited. Commands are few, space is tight, and options are restricted.
A guardian looms over the floor, its body shifting like liquid metal, enforcing these constraints. It watches your every move, daring you to make do with what you have and uncover the passcode to
the next floor despite the restrictions.

## What I did
When I setup the nc connection, I got
```bash
Ha, I bet you can't find what "FLAG" is in this shitty python interpreter.
What could you possibly even do here?

>>>
```
After multiple tries, I got three hints which where flag, print and environ.
flag -
```bash
>>> flag
flag

ERROR:
Traceback (most recent call last):
  File "/chall", line 23, in <module>
    exec('from os import *; ' + clean(user_input))
                                ^^^^^^^^^^^^^^^^^
  File "/chall", line 15, in clean
    raise ValueError(f"NUH UH, {word} is not allowed!{although}")
ValueError: NUH UH, flag is not allowed!(although flag is very close)
```

print - 
```bash
>>> print
print

ERROR:
Traceback (most recent call last):
  File "/chall", line 23, in <module>
    exec('from os import *; ' + clean(user_input))
                                ^^^^^^^^^^^^^^^^^
  File "/chall", line 15, in clean
    raise ValueError(f"NUH UH, {word} is not allowed!{although}")
ValueError: NUH UH, print is not allowed! (although print is very close)
```

environ -
```bash
>>> environ
environ

ERROR:
Traceback (most recent call last):
  File "/chall", line 23, in <module>
    exec('from os import *; ' + clean(user_input))
                                ^^^^^^^^^^^^^^^^^
  File "/chall", line 15, in clean
    raise ValueError(f"NUH UH, {word} is not allowed!{although}")
ValueError: NUH UH, environ is not allowed! (although environ is very close)
```

After this, I gave AI this prompt and it gave me the script which is as follows:
```bash
>>> exec("PRINT(ENVIRON".lower() + "['FLAG'])")
exec("PRINT(ENVIRON".lower() + "['FLAG'])")
```

Using this script, I got the flag which is as follows
citadel{d34th_d035_n07_fr33_y0u_fr0m_7h3_gu17ar15t}
