# cat: not the pet, but the command!

hacker@commands~cat-not-the-pet-but-the-command:~$ cat ~/flag
pwn.college{ko3KR1tcdwULZW1Pffrj1JS0HSk.dFzN1QDL2IzN0czW}

# catting absolute paths

hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{A66hcIsk05DGTxhny_R0SLhqzG2.dlTM5QDL2IzN0czW}

# more catting practice

hacker@commands~more-catting-practice:~$ cat /usr/share/java/flag
pwn.college{A2xevFjleTBJOc1wFznOdczvQIo.dBjM5QDL2IzN0czW}

# grepping for a needle in a haystack

hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{smwoJSoE5bDMRhkFnN67JLgsnTz.ddTM4QDL2IzN0czW}

# listing files

hacker@commands~listing-files:~$ ls /challenge
32163-renamed-run-23570  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/32163-renamed-run-23570
Yahaha, you found me! Here is your flag:
pwn.college{wj7IOdzBOUXvQWKiybgwWH2lwXO.dhjM4QDL2IzN0czW}

# touching files

hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{MWruyuOr0mo5Uesn8nnfy9Cn9ha.dBzM4QDL2IzN0czW}

# removing files

hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{IVjPOD7vj6mcuSNVe9mO4gCk4b6.dZTOwUDL2IzN0czW}

# hidden files

hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv            bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-31061258825371  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat /.flag-31061258825371
pwn.college{wHwanvyOXEKuQZSm_zrlvT_DKZQ.dBTN4QDL2IzN0czW}

# An epic filesystem quest

hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
LEAD  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin   challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat LEAD
Yahaha, you found me!
The next clue is in: /usr/local/lib/python3.8/dist-packages/sympy/solvers/tests/__pycache__

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/$ cd
hacker@commands~an-epic-filesystem-quest:~$ ls /usr/local/lib/python3.8/dist-packages/sympy/solvers/tests/__pycache__
REVELATION-TRAPPED                test_inequalities.cpython-38.pyc  test_recurr.cpython-38.pyc
__init__.cpython-38.pyc           test_numeric.cpython-38.pyc       test_simplex.cpython-38.pyc
test_constantsimp.cpython-38.pyc  test_pde.cpython-38.pyc           test_solvers.cpython-38.pyc
test_decompogen.cpython-38.pyc    test_polysys.cpython-38.pyc       test_solveset.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:~$ cat /usr/local/lib/python3.8/dist-packages/sympy/solvers/tests/__pycache__/REVELATION-TRAPPED
Great sleuthing!
The next clue is in: /opt/busybox/busybox-1.33.2/include/config/feature/modprobe

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:~$ ls /opt/busybox/busybox-1.33.2/include/config/feature/modprobe
TIP-TRAPPED  blacklist.h  small
hacker@commands~an-epic-filesystem-quest:~$ cat /opt/busybox/busybox-1.33.2/include/config/feature/modprobe/TIP-TRAPPED
Congratulations, you found the clue!
The next clue is in: /opt/splitmind/.git/objects/db

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/splitmind/.git/objects/db$ ls
30d24fd7e703e1dd01e2b864811e28e8dfeb55  HINT
hacker@commands~an-epic-filesystem-quest:/opt/splitmind/.git/objects/db$ cat HINT
Yahaha, you found me!
The next clue is in: /usr/share/doc/python3-ppl/html/_sources
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/python3-ppl/html/_sources$ ls
MESSAGE  index.rst.txt
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/python3-ppl/html/_sources$ cat MESSAGE
Congratulations, you found the clue!
The next clue is in: /usr/local/lib/python3.8/dist-packages/pwnlib/adb

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/python3-ppl/html/_sources$ cd
hacker@commands~an-epic-filesystem-quest:~$ ls /usr/local/lib/python3.8/dist-packages/pwnlib/adb
SPOILER-TRAPPED  __init__.py  __pycache__  adb.py  bootimg.py  bootloader.py  protocol.py
hacker@commands~an-epic-filesystem-quest:~$ ls /usr/local/lib/python3.8/dist-packages/pwnlib/adb/SPOILER-TRAPPED
/usr/local/lib/python3.8/dist-packages/pwnlib/adb/SPOILER-TRAPPED
hacker@commands~an-epic-filesystem-quest:~$ cat /usr/local/lib/python3.8/dist-packages/pwnlib/adb/SPOILER-TRAPPED
Yahaha, you found me!
The next clue is in: /usr/share/icons/Adwaita/16x16/ui

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:~$ ls /usr/share/icons/Adwaita/16x16/ui
NOTE                            pan-end-symbolic.symbolic.png    pan-up-symbolic.symbolic.png
pan-down-symbolic.symbolic.png  pan-start-symbolic.symbolic.png
hacker@commands~an-epic-filesystem-quest:~$ cd /usr/share/icons/Adwaita/16x16/ui
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Adwaita/16x16/ui$ cat NOTE
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/Documentation/devicetree/bindings/lpddr2

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Adwaita/16x16/ui$ cd
hacker@commands~an-epic-filesystem-quest:~$ ls /opt/linux/linux-5.4/Documentation/devicetree/bindings/lpddr2
lpddr2-timings.txt  lpddr2.txt
hacker@commands~an-epic-filesystem-quest:~$ ls -a /opt/linux/linux-5.4/Documentation/devicetree/bindings/lpddr2
.  ..  .ALERT  lpddr2-timings.txt  lpddr2.txt
hacker@commands~an-epic-filesystem-quest:~$ cat /opt/linux/linux-5.4/Documentation/devicetree/bindings/lpddr2/.ALERT
Congratulations, you found the clue!
The next clue is in: /opt/busybox/busybox-1.33.2/include/config/feature/crond/special
hacker@commands~an-epic-filesystem-quest:~$ ls /opt/busybox/busybox-1.33.2/include/config/feature/crond/special
CLUE  times.h
hacker@commands~an-epic-filesystem-quest:~$ cat /opt/busybox/busybox-1.33.2/include/config/feature/crond/special/CLUE
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{ozOg_-Efev3V0nbuJbJozex86mR.dljM4QDL2IzN0czW}

# Making directories

hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ ls
bin  hsperfdata_root  pwn  tmp.XvrUsDZh8M
hacker@commands~making-directories:/tmp$ cd pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ ls
college
hacker@commands~making-directories:/tmp/pwn$ ls /tmp/pwn/college
/tmp/pwn/college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{QFiWSnr5Pr55TbnLjYmwzFDjN9_.dFzM4QDL2IzN0czW}

# Finding files

hacker@commands~finding-files:~$ find / -name flag
find: ‘/root’: Permission denied
find: ‘/proc/1/task/1/fd’: Permission denied
find: ‘/proc/1/task/1/fdinfo’: Permission denied
find: ‘/proc/1/task/1/ns’: Permission denied
find: ‘/proc/1/fd’: Permission denied
find: ‘/proc/1/map_files’: Permission denied
find: ‘/proc/1/fdinfo’: Permission denied
find: ‘/proc/1/ns’: Permission denied
find: ‘/proc/7/task/7/fd’: Permission denied
find: ‘/proc/7/task/7/fdinfo’: Permission denied
find: ‘/proc/7/task/7/ns’: Permission denied
find: ‘/proc/7/fd’: Permission denied
find: ‘/proc/7/map_files’: Permission denied
find: ‘/proc/7/fdinfo’: Permission denied
find: ‘/proc/7/ns’: Permission denied
find: ‘/var/log/private’: Permission denied
find: ‘/var/log/apache2’: Permission denied
find: ‘/var/log/mysql’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/php/sessions’: Permission denied
find: ‘/var/lib/mysql-files’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/mysql-keyring’: Permission denied
find: ‘/var/lib/mysql’: Permission denied
find: ‘/tmp/tmp.XvrUsDZh8M’: Permission denied
find: ‘/run/mysqld’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
/usr/local/share/radare2/5.9.5/flag
/opt/linux/linux-5.4/include/config/arch/wants/thp/flag
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
/opt/radare2/libr/flag
/nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag
/nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag
hacker@commands~finding-files:~$ cat /usr/local/lib/python3.8/dist-packages/pwnlib/flag
cat: /usr/local/lib/python3.8/dist-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:~$ cat /usr/local/lib/python3.8/dist-packages/pwnlib/flag
cat: /usr/local/lib/python3.8/dist-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:~$ cat /opt/linux/linux-5.4/include/config/arch/wants/thp/flag
pwn.college{oAGb8oLUClUNjjJjXhgYrnBV0qV.dJzM4QDL2IzN0czW}

# Linking files

hacker@commands~linking-files:~$ cat /lag
cat: /lag: No such file or directory
hacker@commands~linking-files:~$ cat /flag
cat: /flag: Permission denied
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ cat ~/not-the-flag
cat: /home/hacker/not-the-flag: Permission denied
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{sZgZ2NYwLIHKFsCZJ4gT5tAnt-z.dlTM1UDL2IzN0czW}
