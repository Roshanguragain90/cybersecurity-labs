
# TCP 3-way handshake -pracitcal lab

## Objective 
To observe and understand the TCP 3-Way handshake using live network traffic.

## Lab Setup
 - Attacker Machine: Kali LInux
 - Target Machine: Windows 10
 - Network TYpe: Host-only
 - Ip Range: 192.168.56.0/24

## Tools Used
 - nmap 
 - tcpdump

## Commands Used
 """ bash
sudo tcpdump -i eth1 tcp
nmap -p 445 192.168.56.101



## Observation
 - SYN packet sent form kali to windows
 - SYN-ACK received from windows
 - ACK sent from kali
 - TCP connection successfully established on port 445(SMB)


## Conclusion
 TCP uses 3-way handshake(SYN,SYN_ACK,ACK) to established a reliable and connection-oriented communication.


## Evidence 
 ![TCP Handshake Capture ] (screenshot/tcp-handshake-tcpdump.png)
