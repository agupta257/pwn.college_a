In this challenge we have to delete all the decoy characters among the flag characters.
## My Solve

**Flag:**pwn.college{wu3rMvZkI_W_PhjG0jnDKLi1QrK.0FNxEzNxwCN4kjNzEzW}
In this challenge, I used the tr -d command to delete ^ and % character from the flag.
```bash
hacker@data~deleting-characters:~$ /challenge/run | tr -d ^%
Your character-stuffed flag:
pwn.college{wu3rMvZkI_W_PhjG0jnDKLi1QrK.0FNxEzNxwCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that the tr -d command is used to transalte characters into nothing.

## Refernces
Did not use any references for this challenge.
