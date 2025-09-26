In this challenge we have to search for the hidden file.
## My Solve

**Flag:**pwn.college{olHbpcaIlHoG5IS9ndq8kuvtcJC.QX5IDO0wCN4kjNzEzW}
In this challenge, I first used cd and ls to find the clues. For the trapped clues i first used ls and then wrote cat and the directory and the clues. For the hidden 
clues, I used ls -a.
```bash
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
HINT  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin   challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat HINT
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/Documentation/devicetree/bindings/board
hacker@commands~an-epic-filesystem-quest:/$ cd /opt/linux/linux-5.4/Documentation/devicetree/bindings/board
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/devicetree/bindings/board$ ls
README  fsl-board.txt
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/devicetree/bindings/board$ cat README
Congratulations, you found the clue!
The next clue is in: /usr/local/lib/python3.8/dist-packages/pyvex/lib

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/devicetree/bindings/board$ ls /usr/local/lib/python3.8/dist-packages/pyvex/lib
SNIPPET-TRAPPED  libpyvex.a  libpyvex.so
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/devicetree/bindings/board$ cat /usr/local/lib/python3.8/dist-packages/pyvex/lib/SNIPPET-TRAPPED
Yahaha, you found me!
The next clue is in: /usr/share/racket/pkgs/compatibility-lib/mzlib/private/compiled

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/devicetree/bindings/board$ cd /usr/share/racket/pkgs/compatibility-lib/mzlib/private/compiled
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/compatibility-lib/mzlib/private/compiled$ ls
DOSSIER                           contract-define_rkt.zo    package-helper_rkt.zo     stxparamkey_rkt.zo
contract-arr-checks_rkt.dep       contract-mutable_rkt.dep  sigmatch_rkt.dep          stxset_rkt.dep
contract-arr-checks_rkt.zo        contract-mutable_rkt.zo   sigmatch_rkt.zo           stxset_rkt.zo
contract-arr-obj-helpers_rkt.dep  contract-object_rkt.dep   sigutil_rkt.dep           unitidmap_rkt.dep
contract-arr-obj-helpers_rkt.zo   contract-object_rkt.zo    sigutil_rkt.zo            unitidmap_rkt.zo
contract-arrow_rkt.dep            contract-struct_rkt.dep   structure-helper_rkt.dep
contract-arrow_rkt.zo             contract-struct_rkt.zo    structure-helper_rkt.zo
contract-define_rkt.dep           package-helper_rkt.dep    stxparamkey_rkt.dep
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/compatibility-lib/mzlib/private/compiled$ cat DOSSIER
Great sleuthing!
The next clue is in: /opt/linux/linux-5.4/drivers/gpu/drm/amd/acp/include
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/compatibility-lib/mzlib/private/compiled$ cd /opt/linux/linux-5.4/drivers/gpu/drm/amd/acp/include
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/amd/acp/include$ ls
TEASER  acp_gfx_if.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/amd/acp/include$ cat TEASER
Tubular find!
The next clue is in: /opt/linux/linux-5.4/drivers/media/platform/ti-vpe

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/amd/acp/include$ ls /opt/linux/linux-5.4/drivers/media/platform/ti-vpe
CLUE-TRAPPED  cal.c       csc.c  sc.c  sc_coeff.h  vpdma.h       vpe.c
Makefile      cal_regs.h  csc.h  sc.h  vpdma.c     vpdma_priv.h  vpe_regs.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/amd/acp/include$ cat /opt/linux/linux-5.4/drivers/media/platform/ti-vpe/CLUE-TRAPPED
Tubular find!
The next clue is in: /usr/local/lib/python3.8/dist-packages/zmq/tests

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/amd/acp/include$ ls -a /usr/local/lib/python3.8/dist-packages/zmq/tests
.  ..  .TIP  __init__.py  __pycache__
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/amd/acp/include$ cat /usr/local/lib/python3.8/dist-packages/zmq/tests/.TIP
Great sleuthing!
The next clue is in: /usr/local/lib/python3.8/dist-packages/future/builtins

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/amd/acp/include$ ls -a /usr/local/lib/python3.8/dist-packages/future/builtins
.   .NOTE        __pycache__  iterators.py  new_min_max.py  newround.py
..  __init__.py  disabled.py  misc.py       newnext.py      newsuper.py
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/amd/acp/include$ cat /usr/local/lib/python3.8/dist-packages/future/builtins/.NOTE
Yahaha, you found me!
The next clue is in: /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/TeX/Math

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/amd/acp/include$ ls -a /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/TeX/Math
.  ..  .WHISPER  BoldItalic  Italic
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/amd/acp/include$ cat /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/TeX/Math/.WHISPER
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{olHbpcaIlHoG5IS9ndq8kuvtcJC.QX5IDO0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn to find the clues without using cd.

## Refernces
Did not use any references for this challenge.
