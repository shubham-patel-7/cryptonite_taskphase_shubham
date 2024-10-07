# Learning from documentation

hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{YpiM7sudMnhuN6ou3qSm-VKF3Yh.dRjM5QDL2IzN0czW}

# Learning complex usage

hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{0ZeAqzDW7dfPArUeUsl4ku8lWPP.dVjM5QDL2IzN0czW}

# Reading manuals

hacker@man~reading-manuals:~$ man challenge

CHALLENGE(1)                  Challenge Commands                 CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --nkxpmb NUM
              print the flag if NUM is 427

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-lu‐
       minarium/>

SEE ALSO
       man(1) bash-builtins(7)

pwn.college                        May 2024                      CHALLENGE(1)
hacker@man~reading-manuals:~$ /challenge/challenge --nkxpmb 427
Correct usage! Your flag: pwn.college{4JZ_2E7nkJxpmbQHEHGadpms9M2.dRTM4QDL2IzN0czW}

# Searching manuals

hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$
hacker@man~searching-manuals:~$ /challenge/challenge --ioak
Initializing...
Correct usage! Your flag: pwn.college{oeyQcgzjWCgf3uwLdT4WKzgZm8A.dVTM4QDL2IzN0czW}

# Searching for manuals

hacker@man~searching-for-manuals:~$ man man
MAN(1)                        Manual pager utils                       MAN(1)

NAME
       man - an interface to the system reference manuals

SYNOPSIS
       man [man options] [[section] page ...] ...
       man -k [apropos options] regexp ...
       man -K [man options] [section] term ...
       man -f [whatis options] page ...
       man -l [man options] file ...
       man -w|-W [man options] page ...

DESCRIPTION
       man  is the system's manual pager.  Each page argument given to man is
       normally the name of a program, utility or function.  The manual  page
       associated  with  each of these arguments is then found and displayed.
       A section, if provided, will direct man to look only in  that  section
       of  the  manual.  The default action is to search in all of the avail‐
       able sections following a pre-defined order  (see  DEFAULTS),  and  to
       show  only  the  first page found, even if page exists in several sec‐
       tions.

       The table below shows the section numbers of the  manual  followed  by
       the types of pages they contain.

       1   Executable programs or shell commands
       2   System calls (functions provided by the kernel)
       3   Library calls (functions within program libraries)
       4   Special files (usually found in /dev)
       5   File formats and conventions, e.g. /etc/passwd
       6   Games
       7   Miscellaneous  (including  macro  packages  and conventions), e.g.
           man(7), groff(7)
       8   System administration commands (usually only for root)
       9   Kernel routines [Non standard]

       A manual page consists of several sections.

       Conventional section names include NAME, SYNOPSIS, CONFIGURATION,  DE‐
hacker@man~searching-for-manuals:~$ man -k challenge
blfmebxaos (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man blfmebxaos

CHALLENGE(1)                  Challenge Commands                 CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --blfmeb NUM
              print the flag if NUM is 517

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-lu‐
       minarium/>

SEE ALSO
       man(1) bash-builtins(7)

pwn.college                        May 2024                      CHALLENGE(1)
hacker@man~searching-for-manuals:~$ /challenge/challenge --blfmeb 517
Correct usage! Your flag: pwn.college{IGAb51Pl79Y8fmAebxFSaosvETy.dZTM4QDL2IzN0czW}

# Helpful programs

hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v]
                                            [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give
                        you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 56
hacker@man~helpful-programs:~$ /challenge/challenge -g 56
Correct usage! Your flag: pwn.college{Q0j56frfjKcWrTeSXOVvWCPHP2m.ddjM4QDL2IzN0czW}

# Help for builtins

hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "AGbQi3U9".
hacker@man~help-for-builtins:~$ challenge --secret AGbQi3U9
Correct! Here is your flag!
pwn.college{AGbQi3U9acLBdCsTOP1RMvEos08.dRTM5QDL2IzN0czW}
