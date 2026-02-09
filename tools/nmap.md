### Nmap - Network Scanning and Enumeration

## Objective
To discover live hosts, open ports, running services and potential attack vectors using Nmap
Enumeration is always the first real step in any attack

# What is Nmap?
Nmap (Network Mapper) is an open-source tool used to:
    - Discover hosts
    - Identify open ports
    - Detect running services
    - Guess OS and versions
It is one of the most important tools in offensive security

## Basic Syntax
```bash 
nmap [options] target
```
## Core Scan Types
nmap target         Default scan
nmap -p- target     Scan all 65535 ports
nmap -sS target     TCP SYN stealth scan
nmap -sU target     UDP scan
nmap -A target      Aggressive scan(OS, version, scripts)

## Service and Version Detection
```bash 
nmap -sV target
```
Finds what software is running on open ports
## OS Detection
```bash
nmap -O target
```
Attempts to identify the operating system

## Script Scanning (NSE)
```bash
nmap --script vuln target
```
Runs vulnerability detection scripts

## Output Saving
```bash
nmap -oA scan_results target
```
Saves output in all formats

## Sample Enumeration Flow
``` bash 
nmap -p- -sS target
nmap -sV -sC -p <open_ports> target
```
## Security relevance 
Nmap reveals:
    - What services are exposed
    - Which versions may be vulnerable
    - Possible attack paths
Without scanning, exploitation is blind.

## Lessons Learned
- Always scan first
- Small misconfigurations expose systems
- Enumeration beats guessing