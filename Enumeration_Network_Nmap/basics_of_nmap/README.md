![image alt](https://github.com/ACH4Q/Penetration-Testing-Path/blob/main/Enumeration_Network_Nmap/Screenshot%20from%202024-12-11%2023-08-47.png?raw=true)

# My Journey in Nmap Host and IP Address Enumeration

This repository documents my learning journey in the **Nmap Enumeration Module**, where I explored advanced techniques for scanning hosts and IP addresses. Through hands-on practice, I discovered various Nmap flags and their powerful capabilities in network scanning.

## Overview
Nmap (Network Mapper) is a versatile tool for network exploration and security auditing. In this module, I focused on the following key areas:
- **Host enumeration**
- **IP address scanning**
- **Advanced flag usage**
![image alt]()
## What I Learned

### Key Nmap Flags
- **`-sn`**: Perform a "ping scan" to identify live hosts without port scanning.
- **`-sT`**: Conduct a TCP connect scan to identify open ports.
- **`-sU`**: Perform a UDP scan to identify open UDP ports.
- **`-F`**: Use the "fast scan" option to scan fewer ports, speeding up the process.
- **`-sV`**: Probe open ports to determine the version of the services running on them.
- **`-O`**: Enable OS detection to identify the operating system of the target host.
- **`-Pn`**: Skip the ping check and assume the host is up for scanning.
- **`-PE`**: Use ICMP Echo Requests to ping the target.

  ![image alt](https://github.com/ACH4Q/Penetration-Testing-Path/blob/main/Enumeration_Network_Nmap/Screenshot%20from%202024-12-11%2023-09-56.png?raw=true)

### Practical Applications
1. **Enumerating live hosts on a network:**
   ```bash
   nmap -sn 192.168.1.0/24
2. **TCP and UDP scanning:**
   ```bash
   nmap -sT -sU -F 192.168.1.1
   ```
      <h3> This combination enabled me to scan both TCP and UDP ports efficiently. Using the -F flag for a fast scan reduced the scanning time by targeting fewer commonly used ports. I learned that TCP scans (-sT) provide a reliable way to detect open ports by completing the three-way handshake, while UDP scans (-sU) focus on less commonly monitored but equally critical services.</h3>
3. **Service and Os detection**
   ```bash
   nmap -sV -O 192.168.1.1
   ```
   <h3> This helped me gather detailed information about the services running on open ports (-sV) and the operating system of the target host (-O). Such insights are invaluable for vulnerability assessments and identifying potential misconfigurations.</h3>
4.**Stelath scanning whit -Pn**
  ```bash
   nmap -Pn 192.168.1.1
  ```
 <h3> This was particularly useful when scanning targets that block ICMP requests or respond inconsistently to ping probes. By skipping the host discovery phase, I could proceed directly to scanning ports, ensuring the process is not halted by unreachable hosts.</h3>
