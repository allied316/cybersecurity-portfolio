## Gobuster (Directory & DNS Brute forcing)

## What is Gobuster?
Gobuster is a brute-force discovery tool used to find:
- Hidden directories
- Subdomains
- Files on web servers

## Modes
dir     Find directories/files
dns     Discover subdomains
vhost   Virtual host discovery

## Example commands
```bash
# Directory Scan
gobuster dir -u http://10.10.x.x -w /usr/share/wordlists/dirb/common.txt

# Subdomain scan
gobuster dns -d example .com -w subdomains.txt

# File extension search
gobuster dir -u http://10.10.x.x -w  wordlist.txt -x php,html,txt
```

## Why Gobuster Matters
Hidden endpoints often expose:
- Admin panels
- Backup files
- Upload forms
- API routes
