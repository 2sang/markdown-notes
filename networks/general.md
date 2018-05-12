How to check if a port is open for remote system - [Link](https://serverfault.com/questions/188429/how-to-check-if-a-port-is-open-for-remote-systemubuntu)
```bash
#Use nmap.
[user@lappie ~]$ nmap host

Starting Nmap 5.21 ( http://nmap.org ) at 2010-10-07 11:25 CEST
Nmap scan report for host (ip.adr.tld)
Host is up (0.0052s latency).
rDNS record for ip.adr.tld : host.domain.tld
Not shown: 995 closed ports
PORT     STATE SERVICE
22/tcp   open  ssh
80/tcp   open  http
111/tcp  open  rpcbind
3000/tcp open  ppp
5666/tcp open  nrpe

Nmap done: 1 IP address (1 host up) scanned in 0.18 seconds
```

