<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory Deployed in the Cloud (Azure)</h1>
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

- Step 1: First, I used 'Remote Desktop Connection to access my Windows 2022 server VM/Domain controller. Once inside, I went to the application 'Windows Defender Firewall with Advanced Security' then clicked on 'Inbound Rules' and enabled both 'Core Nerworking Diagnostis - ICMP Echo Request (ICMPv4-In)' rules
- Step 2: Next, I clicked on 'add roles and features' in server manager and when on the screen I selected 'Active Directory Domain Services' and installed it. After the features dowloaded it took me back to sever manager and once there I clicked on the caution sign and flag in the top write and clicked 'Promote this server to a domain comtroller'
- Step 3: Then, in the Deployment Configuration I clicked 'Add a new forest' and named my domain. Once installed and set up, the VM automatically restarted. After the restart I logged back in and navigated to 'Active Directory Users and Computers' and created two organizational groups under my domain for employees and admins. In both of the organizational units I created users for those units. In the 'admins' OU I added the users to the 'Domain Admins' Security group by going to 'Properties', 'member of' and adding the to the security group there. 
- Step 4: Finally, through the Azure portal, I changed the Windows 10 VM's DNS server to that of the Domain controller. After that I logged into the Windows 10 VM and went to 'about' in settings and clicked on 'Rename this PC (Advanced)'. Next I clicked on "change" by 'change this pc's domain' then cicked on 'domain' and entered the name of my domain. After the VM restarted I logged back in as one of the admin accounts I created and went back to 'system' in settings and clicked on 'Remote Desktop' then cliked 'Select Users that can remotely access this PC' then clicked 'Add' and typed "Domain users" so that all users of the domain controller could log in to the VM.
- Step 5: This step wasn't neccessary for the setup but what I did here was log back into the Domain Controller as an admin. Next, I opened Powershell ISE as an admin, opened a new script then copy and pasted a script in there that would create 1000 new domain users. 

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
