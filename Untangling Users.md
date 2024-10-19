# Becoming root with su

hacker@users~becoming-root-with-su:~$ su
Password:
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{sVJ1SGR1rAYPQvSoPS4kTkb73Bz.dVTN0UDL2IzN0czW}

# Other users with su

hacker@users~other-users-with-su:~$ su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{wl9I0lUWciUkVwu5-cCT4g3dx3y.dZTN0UDL2IzN0czW}

# Cracking passwords

hacker@users~cracking-passwords:~$ cat /challenge/shadow-leak
root:*:19873:0:99999:7:::
daemon:*:19873:0:99999:7:::
bin:*:19873:0:99999:7:::
sys:*:19873:0:99999:7:::
sync:*:19873:0:99999:7:::
games:*:19873:0:99999:7:::
man:*:19873:0:99999:7:::
lp:*:19873:0:99999:7:::
mail:*:19873:0:99999:7:::
news:*:19873:0:99999:7:::
uucp:*:19873:0:99999:7:::
proxy:*:19873:0:99999:7:::
www-data:*:19873:0:99999:7:::
backup:*:19873:0:99999:7:::
list:*:19873:0:99999:7:::
irc:*:19873:0:99999:7:::
gnats:*:19873:0:99999:7:::
nobody:*:19873:0:99999:7:::
_apt:*:19873:0:99999:7:::
hacker::20000:0:99999:7:::
zardus:$6$f/D7pLa9MAC8yIq/$KfigyBVxYe7tROOp.m0c0Sg7snPQSJCQz8TlF1U9xrZ.q7GWnMJFxOFMhbOUmTYMfuoQOszekSl0Ekw5Khs66.:20015:0:99999:7:::
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Created directory: /home/hacker/.john
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04933g/s 287.2p/s 287.2c/s 287.2C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password:
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{MJAqQcyn47LkgXxkPs7fYGPzIRP.ddTN0UDL2IzN0czW}

# Using sudo

hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{kwlDtnLNsw0SSyEahbBSZa12bKa.dhTN0UDL2IzN0czW}
