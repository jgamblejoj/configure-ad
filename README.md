<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

<h5>Part 1 (Create our Resources)</h5>
- Create a Resource Group
- Create a Windows 10 Virtual Machine (VM)
- While creating the VM, select the previously created Resource Group
- While creating the VM, allow it to create a new Virtual Network (Vnet) and Subnet
- Create a Linux (Ubuntu) VM
- While create the VM, select the previously created Resource Group and Vnet
- Observe Your Virtual Network within Network Watcher


<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The first step involved creating a Resource Group, Portfolio-Lab, which would be used to contain the two virtual machines. The next step involved creating a Windows 10 Virtual Machine that runs Windows 10, P-VM. Next, a virtual machine that runs Linux (Ubuntu) was created, P-VM2. 
</p>
<img src="https://i.imgur.com/bAjYahN.jpg" height="80%" width="80%" alt="Windows 10 Virtual Machine"/>
<img src="https://i.imgur.com/6gkEFY9.jpg" height="80%" width="80%" alt="Linux (Ubuntu) Virtual Machine"/>
<br />

<p>
Wireshark was installed on the Windows 10 Virtual Machine (P-VM) and run. While first using Wireshark, I noticed that I received no response after attempting to ping the Linux VM. The reason for this was that I did not add the Linux VM to the same virtual network (this is due to the VM being deployed in a different region) as the Windows 10 VM. After recreating the Linux VM with the correct configurations, the ping was replied to by the Linux VM. An exercise was then conducted where the ICMP traffic to P-VM2 (Linux) was blocked by creating a new inbound security rule which denied ICMP traffic from anywhere. After observing the blocked ICMP traffic via Wireshark and the Powershell terminal (P-VM), the default security rules were restored.  
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
