# The Root

hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{IfrQprOKattDoYnU00lLMkLxTXt.dhzN5QDL2IzN0czW}

# Program and absolute paths

hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{AXsjBb9QTeNvnge2VOlwZ5xx7Cc.dVDN1QDL2IzN0czW}

# POsition thy self

hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /proc/67 directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /proc/67
hacker@paths~position-thy-self:/proc/67$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{4uJJA0f53rkY3Xzi55OWiIdhOOR.dZDN1QDL2IzN0czW}

# Position elsewhere

hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/doc directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /usr/share/doc
hacker@paths~position-elsewhere:/usr/share/doc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{wcLS_by68A367Z2Cuh1iadmnlRD.ddDN1QDL2IzN0czW}

# Position yet somewhere else

hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/include directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd ^C
hacker@paths~position-yet-elsewhere:~$ cd /usr/include
hacker@paths~position-yet-elsewhere:/usr/include$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{wLWCLfjTzsq8qMjJUWU71n8iVz1.dhDN1QDL2IzN0czW}

# implicit relative path, form /

hacker@paths~implicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{QM4b2MboDhuGmbHBbPhTQJzhvWG.dlDN1QDL2IzN0czW}

# explicit relative path, form /

hacker@paths~explicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{oswXG00aDdGlwK3-ooUOUdcXrTl.dBTN1QDL2IzN0czW}

# implicit relative path

hacker@paths~implicit-relative-path:~$ /challenge/run
Incorrect...
You are not currently in the /challenge directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{ocvyd0S6kSOBAz8QGmU-ntHPUxk.dFTN1QDL2IzN0czW}

# home sweet home

hacker@paths~home-sweet-home:~$ /challenge/run ~/s
Writing the file to /home/hacker/s!
... and reading it back to you:
pwn.college{4kPKA5zOy4q0tlaxrCz-zTc97Ak.dNzM4QDL2IzN0czW}
