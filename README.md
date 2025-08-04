-----------Nmap Scan Summary-------------

I just scanned my Local network using TCP SYN-ACK scan and found local open ports and their service using nmap(network mapper) tool. And in this task i have analysed open ports and its potential risk for further details there will be reference nmapoutput2.txt file  
---

10.61.114.61 — No open ports (All closed)  
10.61.114.78 — Port 53 open, dnsmasq 2.51 (⚠️ outdated)  
10.61.114.119 — No open ports (All closed)  
10.61.114.147 — Port 53 open, dnsmasq 2.90  
10.61.114.185 — Port 7070 open, ssl/realserver? (🔍 investigate)  
10.61.114.198 — No open ports (All closed)  
10.61.114.182 — No open ports (All closed)

---

--------Summary

- 4 hosts have all TCP ports closed (silent or firewalled).
- 2 hosts run **dnsmasq on port 53**; one uses an outdated version (2.51).
- 1 host exposes **port 7070** with an unclear service (possibly streaming or admin panel).

--------Recommendations

- **Upgrade dnsmasq (2.51)** to a secure version.
- **Restrict DNS and 7070 access** to internal, trusted IPs.
- Monitor and investigate **7070/tcp** service for risk or misuse.
