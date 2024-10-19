#Listing Processes

hacker@processes~listing-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.2  0.0   1056   640 ?        Ss   09:09   0:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bi
root           7  0.0  0.0   5052  2560 ?        S    09:09   0:00 /run/dojo/bin/sleep 6h
root          68  0.0  0.0   4132  2560 ?        S    09:09   0:00 /challenge/7394-run-25258
root          72  0.0  0.0   2744  1600 ?        S    09:09   0:00 sleep 6h
hacker        73  0.2  0.0   5240  3840 pts/0    Ss   09:09   0:00 /run/dojo/bin/ssh-entrypoint
hacker        90  0.0  0.0   7868  3200 pts/0    R+   09:09   0:00 ps aux
hacker@processes~listing-processes:~$ /challenge/7394-run-25258
Yahaha, you found me! Here is your flag:
pwn.college{oRrOMdb71dJ-GhXguLP8EM7NLi4.dhzM4QDL2IzN0czW}
Now I will sleep for a while (so that you could find me with 'ps').

# Killing Processes

hacker@processes~killing-processes:~$ ps aux | grep /challenge/dont_run
hacker        73  0.0  0.0   4976  3520 ?        Ss   09:50   0:00 /challenge/dont_run
hacker        93  0.0  0.0   4140  2240 pts/0    S+   09:50   0:00 grep --color=auto /challenge/dont_run
hacker@processes~killing-processes:~$ kill 73
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{M28ns9DiBYAHFyMF20nHaxETuMb.dJDN4QDL2IzN0czW}

# Interrupting Processes

hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{cPRRPijaNSTKEC0qprZnWeQfsNI.dNDN4QDL2IzN0czW}

# Suspending Processes

hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          82      65  0 09:56 pts/0    00:00:00 bash /challenge/run
root          84      82  0 09:56 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can
background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          82      65  0 09:56 pts/0    00:00:00 bash /challenge/run
root          89      65  0 09:56 pts/0    00:00:00 bash /challenge/run
root          91      89  0 09:56 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{AdNJMpV4JxpsNzCMU835XALwI6_.dVDN4QDL2IzN0czW}

# Resuming Processes

hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg /challenge/run
/challenge/run
I'm back! Here's your flag:
pwn.college{ovMq6gsiyaC9Hhj_8JQTaSGQQ4L.dZDN4QDL2IzN0czW}

# Backgrounding Processes

hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root          82 S+   bash /challenge/run
root          84 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the
background, and then launch a new version of me! You can background me with
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg /challenge/run
[1]+ /challenge/run &



Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out.
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root          82 S    bash /challenge/run
root          92 S    sleep 6h
root          94 S+   bash /challenge/run
root          96 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{I5Mac-LwyNO7B7Y-aIl6qdJkt1l.ddDN4QDL2IzN0czW}

# Foregrounding Processes

hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the
background, and *then* foreground it without re-suspending it! You can
background me with Ctrl-Z (and resume me in the background with 'bg') or, if
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg /challenge/run
[1]+ /challenge/run &



Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out. After that, resume me into the foreground with 'fg';
I'll wait.
hacker@processes~foregrounding-processes:~$ fg /challenge/run
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{MqxW_0igua7Qs_4gOTCgqxbv0zV.dhDN4QDL2IzN0czW}

# Starting Backgrounded Processes

hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 82



Yay, you started me in the background! Because of that, this text will probably
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{MLsALXOAQdV7nb4QdAgEOh8JMlj.dlDN4QDL2IzN0czW}
[1]+  Done                    /challenge/run

# Process Exit Codes

hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
223
hacker@processes~process-exit-codes:~$ /challenge/submit-code 223
CORRECT! Here is your flag:
pwn.college{gHM1_9UfgUkq9_htR0vGcN75xC1.dljN4UDL2IzN0czW}
