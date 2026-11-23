# External Attack Surface Discovery and Reconnaissance (Capstone)

Cybersecurity capstone project. We acted as a junior penetration-testing team and started with reconnaissance.

- **Passive recon target:** example.com
- **Active recon target:** 192.168.18.41, a Metasploitable2 lab machine set up by the instructor
- **Status:** passive and active phases complete

## What is in this repository

| Folder | Contents |
|---|---|
| `report/`   | `report/` | The reconnaissance report (PDF, passive and active phases) and the attack surface diagram |
| `evidence/` | Screenshots of every command and result. File names match the appendix labels (A-1, A-2, ...) in the report |
| `commands/` | A list of every command we ran |

## Scope

All results in this repository come from example.com (passive phase) and the single approved address 192.168.18.41 (active phase). Hostnames and IPs that appeared in third-party search results were treated as unverified data and were not contacted.

## Tools used

whois, dig, nslookup, theHarvester, whatweb, and (for the active phase) Nmap.

## Key findings 

- example.com is an IANA-reserved domain with no registrant details exposed.
- DNS and web traffic are served through Cloudflare. ARIN confirms 104.20.23.154 belongs to Cloudflare, Inc.
- The domain publishes a null MX record and an SPF `-all` policy, so it is set up to send and receive no email.
- Three registry locks and DNSSEC are enabled.
- theHarvester returned nothing from one source and many unverified hostnames from all sources. These are treated as likely noise until checked.
- No vulnerabilities were identified.
- Active phase (192.168.18.41): 23 of the 1,000 most common TCP ports were open, including Telnet, the r-services, FTP, VNC, MySQL and PostgreSQL. Services were very old (Linux 2.6.x, Apache 2.2.8, PHP 5.2.4). Nothing was exploited and no logins were attempted.
## Notes

- Findings are labelled as confirmed facts or assumptions in the report.
- AI assistance: [state here how AI was used, if your course requires a disclosure.]

## Team

TANIMOLA AYOMIDE ERIC
