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
