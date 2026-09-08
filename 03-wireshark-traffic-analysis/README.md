# Network Traffic Analysis using Wireshark

**Type:** Coursework Project

## What this is about
I used Wireshark to capture and analyze live network traffic on my machine — the goal was to understand what protocols are actually running in the background, which devices are talking the most, and how much of my traffic is encrypted vs. not.

## Tools
- Wireshark

## What I did

### 1. Setting up the capture
Started a live packet capture on my active network interface and let it run while browsing normally, so the traffic would reflect real, everyday activity — not a staged scenario.

### 2. Collecting traffic
Kept the capture running during regular browsing and background system activity. This generated a solid sample of real traffic: encrypted web requests, DNS lookups, and various transport-layer protocols.

### 3. Looking at protocol distribution
Used Wireshark's Protocol Hierarchy view to see which protocols made up most of the traffic.

**What showed up most:**

| Rank | Protocol | Packets | % of traffic |
|------|----------|---------|---------------|
| 1 | Ethernet | 94,610 | 100.0% |
| 2 | IPv4 | 76,182 | 80.5% |
| 3 | UDP | 74,751 | 79.0% |
| 4 | TLS | 6,723 | 7.1% |

### 4. Finding the most active devices
Checked the IPv4 Endpoints view to see which devices/IPs were generating the most traffic.

| Rank | IP Address | Packets | What it likely is |
|------|-----------|---------|---------------------|
| 1 | 192.168.115.129 | 94,585 | My own device — the busiest by far |
| 2 | 86.51.94.201 | 44,873 | An external server I was communicating with |
| 3 | 74.125.99.41 | 5,732 | Another active external endpoint |

### 5. Comparing HTTP vs HTTPS
Filtered the capture using `http` and `tls` to see how much traffic was actually encrypted.

| Type | Filter | Frames |
|------|--------|--------|
| HTTP | `http` | 64 |
| HTTPS | `tls` | 6,943 |

## What I took away from it
Almost all the traffic was encrypted (HTTPS), which makes sense — most modern websites use HTTPS by default now. It was interesting to actually see that reflected in real data instead of just knowing it in theory. Ethernet and IPv4 were the base of everything, and a lot of the UDP traffic came from QUIC, which is used heavily by services like YouTube and Google.
