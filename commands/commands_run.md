# Commands run

All commands were run from a Kali Linux 2026.1 VM (VirtualBox).

## Part 1: Passive phase (target: example.com only)

### Domain registration
```
whois example.com
whois 104.20.23.154
```

### DNS
```
dig example.com A
dig example.com AAAA
dig example.com MX
dig example.com NS
dig example.com TXT
nslookup example.com
nslookup -type=AAAA example.com
nslookup -type=MX example.com
nslookup -type=NS example.com
nslookup -type=TXT example.com
nslookup -type=A example.com
```

### Emails and subdomains
```
theHarvester -d example.com -b duckduckgo
theHarvester -d example.com -b all
```

### Web technology
```
whatweb example.com
whatweb https://example.com
```

## Part 2: Active phase (target: 192.168.18.41 only, instructor-approved lab machine)

Scope: this single address. No other host was assessed. No logins, password guessing or exploitation.

```
ping -c 3 192.168.18.41
nmap -sV 192.168.18.41 -oN nmap_sV.txt
sudo nmap -O 192.168.18.41
whatweb http://192.168.18.41
```

Still to add: `nmap -sn 192.168.18.41` (host discovery).
