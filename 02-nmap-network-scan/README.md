# Network Scanning using Nmap


## What this is about
I wanted to actually see what's happening on my own home network — how many devices are connected, which ports are open, and whether anything looks like it shouldn't be exposed. Nmap is the standard tool for this, so I used it to scan my network from the inside.

## Tools
- Nmap

## What I did

### 1. Finding the network range
Started by identifying my local network's IP range so I knew what to scan.

### 2. Discovering connected devices
Ran a host discovery scan to see every device currently connected to the network — phones, laptops, smart devices, everything.

### 3. Scanning for open ports
For each device found, I scanned for open ports to see what services were actually running and reachable on the network.

### 4. Reviewing the results
Went through the open ports and running services one by one, thinking about whether each one made sense or looked like unnecessary exposure.

## What I took away from it
It's one thing to know in theory that "every open port is a potential entry point" — it's another to actually scan your own network and see it for real. Most of what came up was expected (routers, printers, personal devices), but going through it made me a lot more aware of what's actually reachable on a network I use every day.
