# THE PATH VARIABLE

hacker@path~the-path-variable:~$ PATH=" "
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: command not found
The flag is still there! I might as well give it to you!
pwn.college{8VQgatB0LWF5bWGISw-Qx7pGpB7.dZzNwUDL2IzN0czW}

# Setting PATH

hacker@path~setting-path:~$ PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{oH7btmstm6Wcd4QENw4R_2nWnv6.dVzNyUDL2IzN0czW}

# Adding commands

hacker@path~adding-commands:~$ which cat
/run/workspace/bin/cat
hacker@path~adding-commands:~$ ls -l win
-rw-r--r-- 1 hacker hacker 11 Oct 19 13:23 win
hacker@path~adding-commands:~$ chmod ugo+x win
hacker@path~adding-commands:~$ nano win
hacker@path~adding-commands:~$ export PATH=/home/hacker:$PATH
hacker@path~adding-commands:~$ echo $PATH
/home/hacker:/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin/
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
/home/hacker/win: line 1: /run/workspace/bin/cat: No such file or directory
pwn.college{MDlfmstBA5b8xam2Si5L4w8K2M5.dZzNyUDL2IzN0czW}

# Hijacking commands

hacker@path~hijacking-commands:~$ echo $PATH
/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
hacker@path~hijacking-commands:~$ export PATH=/home/hacker/:$PATH
hacker@path~hijacking-commands:~$ touch rm
hacker@path~hijacking-commands:~$ nano rm
hacker@path~hijacking-commands:~$ cat /flag
cat: /flag: Permission denied
hacker@path~hijacking-commands:~$ export PATH=/home/hacker/:$PATH
hacker@path~hijacking-commands:~$ chmod +x rm
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
Found 'rm' command at /home/hacker//rm. Executing!
pwn.college{gNECSmCrg9zPPEDUcmtHkI5JiSY.ddzNyUDL2IzN0czW}
