# OverTheWire Bandit - levels 0 - 15

## Objective
To practice linux enumeration, file handling and basic security concepts by solving progressively difficult challenges on the Bandit wargame.

---

## Platform
- OverTheWire Bandit
-SSH-based CTF

---

## Skills Demonstrated
- File enumeration
- Hidden files
- File type identification
- Searching with find
- Base64 decoding
- Compression extraction
- SSH key authentication

---

## Level Highlights

### Bandit 0 -> 1
**Goal:** Read a file in the home directory.
```bash 
ls
cat readme
```
## Bandit 1 -> 2
**Challenge:**File name with special characters.
```bash
cat ./-
```
### Bandit 2 -> 3
**Challenge:** Filename with spaces.
```bash
cat "Spaces in this filename"
```
## Bandit 3 -> 4
**Challenge:** Hidden file.
```bash 
ls -a
cat .hidden
```
## Bandit 4 -> 5
**Challenge:** Identify readable file
```bash
file ./*
```
## Bandit 5 -> 6
**Challenge:** Find file by size.
```bash 
find . -type f -size 1033c
```
## Bandit 6 -> 7
**Challenge:** Find file by owner/group
```bash
find / -user bandit7 -group bandit 6 2>/dev/null
```
## Bandit 7 -> 8
**Challenge:**Search for a word.
```bash
cat data.txt | grep "millionth"
```
## Bandit 8-> 9
**Challenge:** Find unique line.
```bash 
sort data.txt | uniqu -u
```
## Bandit 9 -> 10
**Challenge:** Extract readable strings.
```bash 
cat data.txt | grep -a '\==' | strings
```
## Bandit 10 -> 11
**Challenge:** Base64 decode.
```bash
base64 -d data.txt
```
## Bandit 11 -> 12
**Challenge:** ROT13
```bash 
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-z'
```
## Bandit 12 -> 13
**Challenge:** Extract compressed file.
```bash
xxd -r data.txt > file
file file
# them tar, gzip, bzip2 repeatedly
```
## Bandit 13 -> 14
**Challenge:** SSH with key
```bash 
ssh -i sshkey.private bandit14@localhost
```
## Bandit 14 -> 15
**Challenge:** Use SSL
``` bash 
echo "password" | nc localhost 30000
```
## Security Relevance
These challenges simulate real-world post-exploitation tasks:
    - Finding credentials
    - Extraction hidden data
    - Handling restricted files
    - Using encryption and keys

## Lessons learned
- enumeration reveals everything
- Linux commands chain together powerfully
- Most "security" failures come from misconfigurations