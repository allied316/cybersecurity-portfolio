#linux basics
**Day 1**
## commands learned
- ls
- cd
- pwd
- cp
- mv
- rm
- nano
- touch
- file
- grep
- cut
- paste
- find
- help
- mkdir

## Notes
linux is the foundation of offensive security. Understanding file systems, permissions and
processes is critical

## practice
- Navigate directories
- Created and deleted files


    **Day 2**
## commands learned
- join and split
- cat
- less
- history
- copy
- move
- uniq
- rm
- head
- tail
- man
- whatis
- allias
- wn and nc
- tr
- pipe and tee
- env
- expand and unexpand

## Notes
Linux definitely has a lot of commands. Each with a purpose and useful in its own way. 

## practice
- Chained two commands together such that the stdout of one command become the stdin of another
- joint files together and then split them
- identified the word count of different files
- Used man and what if to identify how certain commands are used

**Day 3**
## commands learned
- chmod
- chown
- passwd
- chgrp
- sudo
- su

## Notes
su just like sudo can be used to gain superuser privileges.
It is recommended to actually gain superuser privileges temporarily instead of logging in as root.
This is because operating continously as the root user increases the risk of making a critical system-altering mistake.

## practice
- Did bandit level 0 and level 1
    - this was about using ssh to get into a user account 
    - and navigating through the files to obtain a password from a file called passwords.txt