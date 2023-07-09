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

<h2>Configure Roles
Admin Panel -> Agents -> Roles
Supreme Admin
</h2>

<p>In this objective, We want to give a certain people the supreme admin role, so they can do anything they want; create tickets, delete tickets, etc.</p>
<p>First, go to or click the Admin Panel, click Agents in the subheadline, click roles.</p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/f1cbd59a-7e76-4d67-b135-6f4479b79176)

<p> Add New role </p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/1e75bb49-a0ad-4173-a654-349b0369603d)

<p>In the definitions, Name it "Supreme Admin" & in the Permissions, grant the Supreme Admin every Ticket permissions, Task permissions & Knowledgebase permission, Click Save Changes. </p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/200c4f96-92b6-43a4-91d4-3330265cdd92)

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/a4266b34-b972-4cec-9b99-ce78ff2a72ac)

<pre> 




  
</pre>

<h2>Configure Departments
Admin Panel -> Agents -> Departments
System Administrators
</h2>

<p>In this configuration, We will create departments.
  For example, depending on the department that the ticket gets associated with, like a ticket comes through for a networking issue. 
  It's going to be assigned into the Networking Department. And the Networking Department has a specific SLA for instance.  </p>
<pre>

  
</pre>

<p>To create a Department, go in the Admin Panel, click Agents in the subheadline, and go to Departments section </p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/8bfcee96-a716-4dfa-8ec4-8a629719a9f8)

<p>You will see that there are 2 Departments; Maintance & Support. But click "Add New Departments"</p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/18b4bd06-92cd-4ab9-a2cd-ed1de8fd1181)

<p>Fill out: Choose Top Level Departments, Name it System Administrators, Click Active, 
  Type: Public, SLA will be on Default for now, Choose All for Ticket assignment, then click "Create Department" </p>

  ![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/e56c0c7e-6224-4189-9b33-9b46a5f103bb)

<p>Congratulations, you have created a new department: System Administrators but it doesn't have any agents yet.</p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/c19711df-acaa-40b0-8b1b-95a285b280d8)

<pre>





  
  
</pre>




<h2>Configure Teams
Admin Panel -> Agents -> Teams
Level I Support
Level II Support
</h2> 

<p>Teams allow you to pull Agents from different Departments and organize them to handle a specific issue or user via a Help Topic or Ticket Filter.

Having Agents from different Departments assigned to a Team will supersede the parameters of the Agents’ Department rules. For example, you can create a Help Topic associated with a particular product you produce, and assign it to a Team of specialist Agents from different Departments.

To create a Team in your Admin Panel, locate the Agents tab, and click on Teams. Then click Add New Team on the right, and fill out the appropriate information. Then you will be able to add Agents to the team by clicking on their name from your list of Agents and checking the corresponding box next to the Team name you wish to add them at the bottom of the page.

A Team can have an appointed leader who can receive Alerts & Notices separate from other team members. In order to set a Team Leader you can choose an Agent from the Team Lead dropdown when creating a Team or Editing an existing Team.

Basically, you can create an A-Team from different departments into it.
</p>

<pre>

  
</pre>

<p>To make a Team, go to the Admin Panel, click Agents in the subheadline, click teams & click create Add New Team </p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/ee9baefb-f936-4260-ba0a-6ab134849cb8)

<pre>
  
</pre>

<p>Name it -> Level ll Support, and you can also add yourself in the Team Members, and click Create Team.</p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/d54857df-8250-4913-9fed-ef97b20f4195)

<pre>

  
</pre>

<h2>Allow anyone to create tickets
Admin Panel -> Settings -> User Settings
Registration Required: Require registration and login to create tickets
</h2>


<p>Go to the Admin Panel, click settings, & click users
  
Check the box: Require registration and login to create tickets. But if you want people to create tickets anonymously, then don't check the box.
Click Save.

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/fe9c7cee-c714-4c30-a3b0-5ac43bf66ef2)


</p>

<pre>



  
</pre>


<h2>Configure Agents (workers)
Admin Panel -> Agents -> Add New Agent Workers: Jane & John (Actual Help Desk Professionals)
</h2>

<p>Agents are given access to the help desk with the intent to respond and resolve the tickets. 
  When adding an Agent to the help desk, they will need to be assigned to a Primary Department and given a Primary Role for the Tickets/Tasks routed to that department. 
  Agents can be given Extended Access to additional departments of the help desk as well as assigned different Roles to those departments; 
  this can be configured in the Access tab of the Agent’s Profile.

</p>

<p>To create Agents, go to the Admin Panel, click agents & click create new agents</p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/a973d165-4dc1-488c-bdb8-76f6c5465cca)

<pre>
  
</pre>

<p>Create Jane user log-in & click "set password." You can also make Jane to create new passwords everytime the next time she log-in.
  
  Since your the Admin, you can modify Jane's access & permissions.

  You can also make her as an Administrator if you want to.

  </p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/40aefcda-0c3a-4611-997b-16eb8a329755)

<pre>
  
</pre>

<p>On the Access section, Assign Jane to the System Administrators Department & Assign her as the Supreme Admin. 
  You can also give Jane an extended access to different departments if you want to.</p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/5e7734e8-9206-4495-adf9-0f7d225c39bf)

<pre>
  
</pre>

<p>
Make sure she has all permissions
</p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/64aec0e2-53b8-40da-a602-e7ca337ea59c)


<pre>
  
</pre>

<p>Assign Jane to the Level ll Support Team & click "Create"</p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/359c61ba-c9bf-44b1-96a8-1e536bf488bf)

<pre>


  
</pre>

<p>You have succesfully created Jane as an agent.</p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/e754dc6f-8a6a-4890-a7f6-6490f7043e70)

<pre>
  
</pre>

<p>Create another Agent: John Doe</p>
  
<p>Go to Admin Panels, click Agents, Add new Agents.

Create a username for John Doe, and click "Set password" to create a password.

Uncheck the Box: Send the agent a password to reset email.

Enter a Password.

Also Uncheck the Box: Require Password change at next login.

And click set.

On the Access Section, Assign John Doe to the Support Department, Assign him to the Support Extended Access, & click "View only" as his role.

Click Create.</p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/d49d4868-0876-464f-9328-e98cd64a291b)






