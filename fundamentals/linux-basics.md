# Linux Fundamentals — Week 1

## Objective
To understand basic Linux navigation, file management, and system concepts
used in penetration testing and security operations.

Linux is the primary operating system used in offensive security tools such as
Kali Linux, Parrot OS, and attack frameworks.

---

## Environment
- OS: Kali Linux (VM)
- Terminal: Bash
- Practice Platforms: OverTheWire (Bandit)

---

## Core Commands Learned

| Command | Purpose |
|--------|---------|
| ls     | List files and directories |
| cd     | Change directory |
| pwd    | Show current path |
| mkdir  | Create directory |
| touch  | Create file |
| cp     | Copy files |
| mv     | Move/rename files |
| rm     | Delete files |
| cat    | Display file contents |
| less   | View large files |
| find   | Search for files |
| man    | Read manual pages |

---

## Permissions Basics
Linux uses **read (r)**, **write (w)**, and **execute (x)** permissions.

Example:
```bash
ls -l

```
# Output:
-rw-r--r-- 1 user user file.txt

- Owner: rw-
- Group: r--
- Others: r--

# changing permissions
```bash 
chmod 755 script.sh

```
## Practical Exercises
1. Directory Navigation
2. File creation and Deletion
3. Bandit Practice
    completed Bandit levels 0-5
    used:
        cat
        ls -a
        cd
        file
        find


## Security Relevance
Attackers and defenders rely on Linux for
    - Log analysis
    - Script execution
    - Privilege escalation
    - Network scanning

## Lessons Learned
The terminal is faster than GUI once practiced
Permissions are critical for security
Most hacking tools rely on linux command-line usage.