### Scanning Command Syntax
```bash
nmap [scan types] [options] {172.16.1.1 specification}
```

### Scanning Types
Switch / Syntax | Example | Description
:---------------: | :-------: | :-----------:
-sS | ```nmap -sS 172.16.1.1``` | TCP SYN port scan
-sT | ```nmap -sT 172.16.1.1``` | TCP connect port scan
-sA | ```nmap -sA 172.17.1.1``` | TCP ACK port scan
-sU | ```nmap -sU 172.16.1.1``` | UDP port scan
-sF | ```nmap -sF 172.16.1.1``` | TCP FIN port scan
-sX | ```nmap -sX 172.17.1.1``` | XMAS scan
-sP | ```nmap -sP 172.16.1.1``` | Ping scan

### Port Specification Options
Syntax | Example | Description 
:------: | :-------: | :----------:
-p | ```nmap -p 23 172.16.1.1``` | Port scanning specific port
-p | ```nmap -p 23-100 172.17.1.1``` | port scanning, port range
-p | ```nmap -pU:110,T:23-25,443 172.16.1.1``` | U-UDP, T-TCP scan
-p- | ```nmap -p- 172.16.1.1``` | Port scan for all ports
-f | ```nmap -f 172.16.1.1``` | More speed
-r | ```nmap -r 172.16.1.1``` | Sequential port scan

### Host Discovery
Switch / Syntax | Example | Description
:---------------: | :-------: | :-----------:
-sL | ```nmap -sL 172.16.1.1-5``` | List without scanning 
-sn | ```nmap -sn 172.16.1.1/8``` | Disable port scanning
-Pn | ```nmap -Pn 172.16.1.1-8```| Port scanning only no host discovery
-PS | ```nmap 172.16.1.185 -PS22-25,80``` | TCP SYN discovery
-PA | ```nmap 172.16.1.185 -PA-22-25,80``` | TCP ACK discovery
-PU | ```nmap 172.16.1-8 -PU53``` | UDP port discovery
-PR | ```nmap 172.16.1.1-8 -PR``` | ARP discovery within local network
-n | ```nmap 172.16.1.1 -n``` | No DNS resolution
