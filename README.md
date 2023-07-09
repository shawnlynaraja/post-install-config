<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles
Admin Panel -> Agents ->
Roles Supreme Admin
- Configure Departments
Admin Panel -> Agents -> Departments
System Administrators
- Configure Teams
Admin Panel -> Agents -> Teams
Level I Support
Level II Support
- Allow anyone to create tickets
Admin Panel -> Settings -> User Settings
Registration Required: Require registration and login to create tickets
- Configure Agents (workers)
Admin Panel -> Agents -> Add New
Jane
John
- Configure Users (customers)
Agent Panel -> Users -> Add New
Karen
Ken
- Configure SLA
Admin Panel -> Manage -> SLA
Sev-A (1 hour, 24/7)
Sev-B (4 hours, 24/7)
Sev-C (8 hours, business hours)
- Configure Help Topics
Admin Panel -> Manage -> Help Topics
Business Critical Outage
Personal Computer Issues
Equipment Request
Password Reset

<h2>Steps before Configurations</h2>
The first step is to open your Azure Account. 
Copy the Public IP address of the osTicket Virtual Machine. Then open Remote Desktop Connection. 
Paste the osTicket VM Public IP Address into the Remote Desktop Connection.
Enter your osTicket Virtual Machine username and password.

<h2>Browse to your help desk login page: http://localhost/osTicket/scp/login.php & Enter your credentials (This is for the Admin log-in & do admin things.)</h2>
<p>
<img src="https://i.imgur.com/wC2ofg1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h2>Admin Panel vs Agent Panel</h2>
Admin is someone who sets up the ticketing system, set up settings, define roles, and other general administrative duties.
Agent is someone who actually works on the tickets and helping end-users.
if your osTicket Website on the top right hand corner says "Admin Panel" it actually that means that you're operating in the Agent Panel.

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/4982bfa4-a510-4b02-986c-66bda543f085)











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
