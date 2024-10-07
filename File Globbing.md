# Matching with *

hacker@globbing~matching-with-:~$ cd /*ge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{AJcuoyaB1V2IbjrTksvSmTq5BQL.dFjM4QDL2IzN0czW}

# Matching with ?

hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{wo7hlp0QD-8oMCePVw6P2oy9w51.dJjM4QDL2IzN0czW}

# Matching with []

hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{A5WQag-vysKgyb6OEEj-SKEh8YT.dNjM4QDL2IzN0czW}

# Matching paths with []

hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{0IpsigIDOa9DffTjKqRbjMpVMSQ.dRjM4QDL2IzN0czW}

# Mixing globs

hacker@globbing~mixing-globs:~$ cd /*ge/*s
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{QflelwJ4fiKmhAeCu1LzLEMEBdy.dVjM4QDL2IzN0czW}

#

hacker@globbing~exclusionary-globbing:~$ cd /*e/*s
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [^pwn]*
You got it! Here is your flag!
pwn.college{cDAZMdCz_Y2BrgUJIfKfF1704kI.dZjM4QDL2IzN0czW}
