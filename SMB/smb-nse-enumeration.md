# Title
SMB Enumeration using Nmap NSE Scripts

# Objective

The objective of this test was to enumerate SMB services running on the target system using NMAP NSE Scripts in order to identify shares, users, OS information , and security configuration.

#Target Information
Target IP: 192.168.56.101
Operating System: Windows 10
Host name: DESKTOP-89N9SRV

#Tools used
 Nmap 
 Nmap scripting Engine

#Command executed
nmap -A 192.168.56.101
nmap --script smb-enum-shares,smb-enum-users,smb-os-discovery -p445 192.168.56.101

# Open smb ports
139/tcp - NetBios session service 
445/tcp - microsoft directory services 


# SMB enumeration results
- SMB guest access : Disabled
- SMB user enumeration : Blocked
- SMB share : not accessible withou authentication
- SMB OS detection : windows 10 (Build 19041)

# SMB security configuration
 - Authentication level : user
 - smb v1: enabled
 - smb message signing : enable but not required

# security analysis
 Although SMB ports were open , the system did not allow anonymous access. User- level authentication prevented basic enumeration attacks. 
 SMBv1 being enabled and message signing not being required may present theoretical risks, but no direct exploitation was possible in this setup.

 # Conclusion 
  The target system was properly hardened against common SMB enumeraton attacks. No critical vulnerabalites were identified through NSE- based enumeration.
