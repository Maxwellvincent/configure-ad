<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell
- Wireshark

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)
- Linux(Ubuntu)

<h2>High-Level Deployment and Configuration Steps</h2>

- Creating Virtual Machines in Azure
- Observing ICMP Traffic Using Wireshark
- Configuring a Firewall (Network Security Group)
- Monitoring Network Traffic in Wireshark

<h2>Deployment and Configuration Steps</h2>


<p>
Before deploying Active Directory, we must create two virtual machines:
1️⃣ Windows Server 2022 VM – This will act as the domain controller.
2️⃣ Windows 10 VM – This will serve as a client machine for testing.

📌 Instructions:

- Log in to the Azure Portal.
- Create a Resource Group to organize related resources.
- Deploy a Windows Server 2022 VM with at least 2 vCPUs and 4GB RAM.
- Deploy a Windows 10 VM in the same Virtual Network (VNet) as the Server.
- Configure RDP access for both machines.
</p>
<br />
<p>
<img src="https://i.imgur.com/nlOvyNX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h3>Step 2</h3>

<p>
To ensure proper communication between the machines, we need to adjust network settings.

📌 Instructions:

- Assign Static Private IP Addresses to both VMs.
- Disable Windows Defender Firewall on both machines (optional but may prevent connectivity issues).
- Verify connectivity by using ping commands between VMs.
</p>
<br />
<p>
<img src="https://i.imgur.com/ya3fmei.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h3>Step 3</h3>

<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<p>
<img src="https://i.imgur.com/ZTjETwS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h3>Step 4</h3>

<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<p>
<img src="https://i.imgur.com/yXo62jx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
