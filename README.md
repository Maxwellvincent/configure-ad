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

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1: Deploy and Configure the Domain Controller (DC-1)
- Step 2: Deploy and Configure the Client Machine
- Step 3: Install and Configure Active Directory   
- Step 4: Join a Clinet to the Domain

<h2>Deployment and Configuration Steps</h2>

<h3>Part 1: Setting up Active Directory</h3>
<p>
The Domain Controller (DC-1) is created in Azure, and Active Directory Domain Services (AD DS) is installed.
</p>
<p>
<img src="https://i.imgur.com/Hclpbce.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/1de93Bm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

<h3>Part 2: Configuring Remote Desktop for Domain Users</h3>
<p>
Remote Desktop is enabled for non-administrative users on Client-1. Domain users are granted RDP access, allowing them to log in remotely.
</p>
<p>
<img src="https://i.imgur.com/F18ebhQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/KQCwlJl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/tnHL5Bx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

<<h3>Part 3: Automate User Creation with PowerShell</h3>
<p>
A PowerShell script is executed on DC-1 to create multiple Active Directory user accounts. 
</p>
<p>
<img src="https://i.imgur.com/g2SoPyh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
