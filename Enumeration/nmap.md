### Scanning Command Syntax
```bash
nmap [scan types] [options] {172.16.1.1 specification}
```

### Scanning Types
Switch / Syntax | Example | Description
:---------------: | ------- | :-----------:
-sS | nmap -sS 172.16.1.1 | TCP SYN port scan
-sT | nmap -sT 172.16.1.1 | TCP connect port scan
-sA | nmap -sA 172.17.1.1 | TCP ACK port scan
-sU | nmap -sU 172.16.1.1 | UDP port scan
-sF | nmap -sF 172.16.1.1 | TCP FIN port scan
-sX | nmap -sX 172.17.1.1 | XMAS scan
-sP | nmap -sP 172.16.1.1 | Ping scan
