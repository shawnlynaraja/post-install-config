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


<pre>



  
  
</pre>


<h2>Configure Users (customers)
Agent Panel -> Users -> Add Karen & Ken
</h2>


<p>Users can now create an account and log-in to create a ticket or check a ticket’s status. 
  
  As always with osTicket, users or ticket creators are associated with their email address as the unique identifier of each user. 
  
  The User Directory, located on the Agent Panel, allows agents to search tickets by user as well as create Organizations to associate the user to. 
  
  Agents can be configured as internal Account Managers for tickets created by users of an Organization.

  Users are the ticket owners of the tickets in the help desk. When a ticket is created in the help desk, 
  
  the user is associated with their email address in the User Directory of the help desk. Users can be added or deleted from the User Directory of the help desk at any time.

</p>

<h2> We are now going to the Agent Panel now. Click Users & Add New Users
</h2>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/c6b5f14a-7b5f-4110-a89b-c6655046a720)

<pre>

  
</pre>

<p>Enter its customer's credentials and click Add User</p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/aba40330-d9c8-4808-b3d6-4693203e4bc7)

<pre>

  
</pre>

<p>Do also the same thing for the Customer Ken.</p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/c7b6fc77-246b-40b1-b412-4f67ca2e0ed1)


<pre>

  
</pre>

<h2>
  Configure SLA
  
Admin Panel -> Manage -> SLA
  
Sev-A (1 hour, 24/7)

Sev-B (4 hours, 24/7)

Sev-C (8 hours, business hours)

</h2>

<p>The purpose of the SLA Plan is to provide a length of time in which the help desk Administrator expects tickets to be closed.
  
The way osTicket defines them, is putting them in a time limit

SLA in osTicket is in a time limit, meaning, for how long the ticket is going to be open.</p>

<pre>
  
</pre>

<p>To create 3 SLAs, We are going back to the Admin Panel, Click Manage and click SLA</p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/35176ddf-c2a9-499a-bad1-fd893f875647)

<p> - Click "Add new SLA plan"
  
  - Name it SEV-A, 
  
  - Choose 24/7 for Schedule. 24/7 means if there is an issue with the customer's computer on the weekened, it doesn't matter if it's on the weekend.

  - Grace Period: Amount, in hours, before tickets with this SLA will become overdue if not closed in allotted time.

  - For example, if it happens on Sunday night 10:00 PM, the ticket needs to be resolved by Sunday night 11:00 PM.

  - Click Add Plan

  </p>

  ![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/4c2029d8-0021-480d-bd8d-df2d46196a07)


<pre>
  
</pre>

<h2>For SEV-B</h2>

<p> It will be scheduled for 24/7 and grace period: 4 Hours

- For example, on Saturday morning 2:00 AM, It will need to be resolved by Saturday morning 6:00 AM because of our grace period: 4 hours.

- Click Add Plan
</p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/cc23b6e0-fe21-461d-becc-f7af350b7ff0)

<pre>

  
</pre>

<h2>For SEV-C</h2>

<p>It will be scheduled during business hours (Mon-Fri 8AM-5PM)
  
  - Grace Period: 8 Hours 
  
  - Basically, if something happens on Friday at 3:00 PM, We have 2 more hours before business closes. So another 6 hours starting on Monday at 8:00 AM.
  
  - Click Add Plan
  
  </p>

  ![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/9db019ea-60dd-4025-a1d9-d95d30a22380)

<pre>


  
</pre>

We now have SLAs to create and assigned tickets.

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/f0c3bc72-c8a9-4099-86c3-12d64852e9b5)

<pre>


  
</pre>


  <h2>Configure Help Topics
Admin Panel -> Manage -> Help Topics
Business Critical Outage
Personal Computer Issues
Equipment Request
Password Reset
</h2>

<p>Help Topics will help streamline your end-user’s help desk experience to ensure proper assignment and prompt response to the ticket. 
  
  Create as many Help Topics as needed and can even nest Help Topics within each other for further breakdown (For example, Human Resources and Human Resources/Payroll.)

Help Topics will determine what Department the ticket is routed to which will determine which Agents have access to the ticket. The Help Topic also can determine other configurations of the ticket, such as the ticket’s SLA (or Service Level Agreement) and priority of a ticket, i.e. Emergency to Low.

There are two places where the Help Topic must be selected on New Tickets; the client portal and new tickets created internally by staff. When Users select the Help Topic, they are not aware of the configurations in place for that Help Topic</p>


<h2>Go to the Admin Panel -> Manage -> Help Topics</h2>

<p>Cllick add new Help Topic</p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/8b7746ad-af40-4821-8d15-3a94b72e9aad)

<pre>
  
</pre>

<p>Create 4 new help topics: 1) Business Critical Outage, 2) Personal Computer Issues, 3) Equipment Request, 4) Password Reset</p>

![image](https://github.com/shawnlynaraja/post-install-config/assets/138860791/98fe8f63-454a-4c7c-a572-a3bd3cc18ed7)




