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

*From the Windows VM, we use Powershell to attempt to enable SMBProtocol 1 and 2.* 

### <img width="789" height="106" alt="image" src="https://github.com/user-attachments/assets/d1b89e8f-f579-438e-99cc-753d3d8921d7" />


Step 3: Enable WinRM

Enable WinRM from Powershell 

### <img width="868" height="737" alt="image" src="https://github.com/user-attachments/assets/65cf027c-1ceb-44b5-b8ae-34ed98b4cd61" />


Step 4: Install & Enable openSSH Server (Port 22) 

### <img width="782" height="294" alt="image" src="https://github.com/user-attachments/assets/69d76790-fb61-4713-960d-03da0fa2def6" />

*Verify SSH is Reachable*

### <img width="705" height="91" alt="image" src="https://github.com/user-attachments/assets/4a88ca74-68c5-448e-a1f3-be67ad1fd63d" />


Step 5: Install IIS 

I added IIS to the Windows VM so the machine isn’t just sitting there with a few management ports open. By running a simple web server on ports 80 and 443, the Windows host starts to look more like a real system you’d run into in an enterprise environment. It gives me something meaningful to scan and interact with. Nmap can pull banners, grab headers, detect modules, and actually enumerate a service instead of just reporting closed ports. IIS basically helps round out the attack surface so the lab feels more realistic and useful for practicing basic web service reconnaissance.

### <img width="1120" height="628" alt="image" src="https://github.com/user-attachments/assets/23ba2a6c-f877-452b-8fd1-de636c9d0149" />


Step 6: Disable Firewall

<img width="1116" height="631" alt="image" src="https://github.com/user-attachments/assets/3f154115-49a4-401a-b908-072ef7706c3c" />


Step 7: Prepare for Hash Extraction 

*Verify Windows User is an Admin*

### <img width="506" height="507" alt="image" src="https://github.com/user-attachments/assets/e29d072c-b630-4fb4-b199-89b3f25c356d" />


*Create a folder to export the hives 

### <img width="1130" height="637" alt="image" src="https://github.com/user-attachments/assets/a23f59da-b69b-4013-9a7a-7dabbddbb55e" />

*Export the SAM and SYSTEM Hives and Verify*

<img width="602" height="357" alt="image" src="https://github.com/user-attachments/assets/1cafeec3-032e-4dcd-b7d9-47bc441298e4" />

DONE!
















