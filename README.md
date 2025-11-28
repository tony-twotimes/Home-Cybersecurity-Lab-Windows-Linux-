# Home Cybersecurity Lab (Windows + Linux)

## Objective
The purpose of this lab is to create a safe, isolated Windows environment with multiple user accounts and intentionally exposed services \>
to practice core cybersecurity skills. This includes scanning and enumerating open ports, analyzing Windows services, exploring SMB configurations, \> 
and performing legal password hash extraction and cracking within a controlled two-machine setup.

### Skills Learned

- Building a two-machine cyber lab using VMware
- Configuring a Windows host with exposed services for testing
- Preparing user accounts and settings for future password auditing
- Establishing NAT-based network isolation between VMs
- Setting up a Linux system with essential security tools for scanning

### Tools Used

- VMware Workstation for virtualiztion 
- Windows 10 Home as the target system
- Kali Linux as the attacker system
- Basic Linux terminal utilities
- Powershell

## Steps

Phase 1: Verify Connectivity 

Step 1: ipconfig on command prompt in windows to verify network information

### <img width="955" height="207" alt="image" src="https://github.com/user-attachments/assets/0e037c0f-17ee-43fb-9685-896754c13f7c" />

Step 2: ping the network from the attacker Kali Linux machine
  
### <img width="784" height="286" alt="image" src="https://github.com/user-attachments/assets/d771e831-9bc3-46bd-b0b0-392561f35d9d" />

Phase 2: Make Windows an Interesting Target 

Step 1: Add local users 

*User Creation* 

### <img width="419" height="259" alt="image" src="https://github.com/user-attachments/assets/0fc1281e-3815-4f5b-a882-9a0bbafa4e7e" />


### <img width="456" height="506" alt="image" src="https://github.com/user-attachments/assets/f423ee5e-1a1e-4d91-8d65-90c937032699" />

Step 2: Enable SMB 

Step 3: Enable WinRM

Step 4: Enable SSH 

Step 5: Install IIS 

Step 6: Disable Firewall

Step 7: Prepare for Hash Extraction 






