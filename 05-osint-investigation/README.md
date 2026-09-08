# OSINT Investigation — Saudi Telecom Company (stc)

**Type:** Hands-on Security Lab

## What this is about
I practiced OSINT (Open-Source Intelligence) — collecting information about a real organization using only public sources, without touching their systems directly. I picked Saudi Telecom Company (stc) as the target since it's a major national provider with a large public footprint.

## Tools
- WHOIS Lookup
- Public document search
- Subdomain discovery tool
- Netcraft

## What I did

### 1. Domain registration lookup
Ran a WHOIS lookup on stc.com.sa — confirmed ownership, found the name servers were managed by Akamai (CDN/DNS), and confirmed DNSSEC was enabled for domain security.

### 2. Searching public documents
Found publicly hosted PDF reports on stc's official website, which gave useful context on how the organization communicates with stakeholders.

### 3. Subdomain discovery
Used a subdomain discovery tool and found 200+ subdomains linked to stc.com.sa — a much fuller picture of their online presence than just the main site.

### 4. Infrastructure lookup with Netcraft
Checked hosting providers, operating systems, and netblocks for various subdomains like my.stc.com.sa and careers.stc.com.sa.

## What I took away from it
It was surprising how much information is sitting in plain sight without any hacking involved — just public tools and patience. It made a strong case for why organizations need to regularly audit their own public footprint, because attackers can gather all of this just as easily.

## Recommendations
- Regularly review and remove unused/outdated subdomains
- Review public documents before publishing to avoid exposing sensitive details
- Continuously monitor public-facing infrastructure using OSINT tools
