## Networking fundamentals - Practice Lab Writeup

# Objective
To understand basic network configuration, connectivity and exposed services using common Linux networking commands. This knowledge is essential for enumeration during penetration testing.

# Learning sources
linuxJourney.com - Networking
local linux terminal practice

# Environment
- OS: Kali linux virtual machine
- Network: Wifi


# Commands used and Observations
1.  IP configuration
```bash
ip a
```
**Observation**
Interface: eth0
Ip Address: 10.0.x.x
Network Type: Private LAN

2. Default Gateway
```bash 
ip route
```
**Observation**
default via 10.0.x.x dev eth0

3. Connectivity Test
```bash
ping 8.8.8.8
```
**Result:**
Replies received -> Internet connectivity confirmed

Then:
```bash 
ping google.com
```
This confirmed DNS resolution is working

4. Network Path
```bash
traceroute google.com
```
**Observation**
- Displayed multiple hops between my machine and Google
- Each hop represents a router or network nod

This helps attackers understand network layout and filtering

6. HTTP Request
```bash 
curl http://google.com
```
**Observation**
- Received raw HTML response
- Confirms ability to interact directly with web servers

## Security relevance
Networking is the foundation of all attacks
Attackers use these techniques to:
    - Discover live systems
    - Identify exposed services
    - Choose appropriate exploits 
    - Map internal networks
## Lessons learned
- Every open port is a possible entry point
- Enumeration always comes first
- Understanding traffic flow is critical in attacks