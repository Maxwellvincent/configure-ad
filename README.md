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

<h3>Part 3 Configuring a Firewall</h3>

<p>
To observe how firewall rules impact network communication, you will configure the Network Security Group (NSG) to block and then re-enable ICMP (ping) traffic between the Windows 10 and Ubuntu VMs.

- Initiate a continuous ping:
On the Windows 10 VM, start a non-stop ping to the Ubuntu VM.
This will generate ICMP (ping) traffic, which can be observed in Wireshark and the command prompt.

- Block ICMP traffic in the NSG:
Open Azure Portal and navigate to the Network Security Group (NSG) assigned to the Ubuntu VM.
Modify the Inbound Security Rules to deny ICMP traffic.

- Observe the impact:
Return to the Windows 10 VM and check the ping output—it should now show request timeouts.
Open Wireshark and monitor the ICMP traffic; you should see the absence of ICMP replies.
Re-enable ICMP traffic:

Once observations are complete, stop the ping process on the Windows 10 VM.
</p>
<p>
<img src="https://i.imgur.com/ZTjETwS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/yXo62jx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


<br />
