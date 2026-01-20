#Enumeration -Nmap service & Version detection 

## Objective 
To identify open ports, running services and service versions on windows target machine using Nmap service detection.

## Lab setup

Attacker machine: Kali Linux
Target Machine : Windows 10
Network SEtup : Virtual Box ,Host Only Network
Tools: Nmap 


## Command Used:

nmap -sV 192.168.56.101 
nmap -sV 192.168.56.101 -oN nap_sV.txt



## Results 
The scan identified the following open ports and services:

1.port 139 - open -netbios -ssn microsoft windows netbios
 -used for NetBios over TCP
 - old windows networking
 - works with SMB

2.port 445 (SMB)
 -open -microsoft -ds microsoft windows(7-10) 
 - smb is running
 - file sharing service
 - common attack surface

3. port 3389
 - open ms-WBT server microsoft terminal service 
 - RDP enabled 
 - remote desktop service possible 

4. OS information 
 - service info: OS: windows 
 - Host name: DESKTOP - 89N95RV

## Analysis 
SMB port is open it means file sharing service is enable and it makes an attack surface though open port doesn't mean system is vulnerable

RDP is enable which allows remote access and can be risky if passwords and credential are weak.


## evidence 
Screenshots of the Nmap scan and output are stored in the screenshot directory

