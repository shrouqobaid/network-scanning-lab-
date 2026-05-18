# Nmap 7.91 scan initiated Sun May 17 05:00:40 2026 as: nmap -sV -oN basic_scan.txt scanname.nmap.org
Nmap scan report for scanname.nmap.org (50.116.1.184)
Host is up (0.24s latency).
Other addresses for scanname.nmap.org (not scanned): 2600:3c01:e000:3e6::6d4e:7061
rDNS record for 50.116.1.184: ack.nmap.org
Not shown: 996 filtered ports
PORT    STATE SERVICE VERSION
22/tcp  open  ssh     OpenSSH 7.4 (protocol 2.0)
25/tcp  open  smtp    Postfix smtpd
80/tcp  open  http    Apache httpd 2.4.6
443/tcp open  ssl/ssl Apache httpd (SSL-only mode)
Service Info: Host:  ack.nmap.org

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sun May 17 05:02:00 2026 -- 1 IP address (1 host up) scanned in 79.57 seconds
