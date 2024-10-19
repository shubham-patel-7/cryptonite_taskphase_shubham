# Changing File Ownership

hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{4L3LSf0LJxJHDV3TDk9DR7CwR4F.dFTM2QDL2IzN0czW}

# Groups and Files

hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{khsn7mnfvP95MjqExcR9cQGAEQV.dFzNyUDL2IzN0czW}

# Fun with Groups Names

hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp719) groups=1000(grp719)
hacker@permissions~fun-with-groups-names:~$ chgrp grp719 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{MkmZUUA9q8sxos1AqxaIhT5OkSu.dJzNyUDL2IzN0czW}

# Changing Permissions

hacker@permissions~changing-permissions:~$ chmod a+r /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{4n4DYRCOYLJ87wuwUxAYkMWqShf.dNzNyUDL2IzN0czW}

# Executable Files

hacker@permissions~executable-files:~$ chmod a+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{4SkNjP32aaBDlX_-Eu1EYxqJW2a.dJTM2QDL2IzN0czW}

# Permission Tweaking Practice

