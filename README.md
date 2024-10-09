# Post-install-config1

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket -  Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source helpdesk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Microsoft Azure
- Virtual Machine
- osTicket 


<h2>Good Things to Know</h2>

 - Click on specific positions for a better understanding!
 	- [Roles](https://docs.osticket.com/en/latest/Admin/Agents/Roles.html)
	- [Departments](https://docs.osticket.com/en/latest/Admin/Agents/Departments.html)
	- [Teams](https://docs.osticket.com/en/latest/Admin/Agents/Teams.html) 
	- [Agents](https://docs.osticket.com/en/latest/Admin/Agents/Agents.html)
	- [Users](https://docs.osticket.com/en/latest/Agent/Users/User%20Directory.html).
	- [Service Level Agreement(SLA)](https://docs.osticket.com/en/latest/Admin/Manage/SLA%20Plans.html)
	
   

<h2>Installation Steps</h2>

<h3>Step 1: Open osTicket and Log In

- Log in to osTicket using the credentials you made during the installation tutorial </h3>
	- If you need help installing osTicket, please see my tutorial [here](https://github.com/roslyndwilliams/osticket-prereqs)

<p align="center">
<img src="https://i.imgur.com/gAXVBO2.png" height="80%" width="80%" alt="Azure Free Account"/>	


<h3>Step 2: Configure Roles </h3>

- Make sure you are in the Admin panel (check the top-right of the screen to see which panel you are in)
	- If it says "Agent," you are in the Admin panel
- Select the Agent tab > Roles > Add New Role
	- Name: Supreme Admin
	- Select Permissions tab and check every box under the "Tickets," "Tasks," and "Knowledgebase" sections
- Select Add Role
	
<p align="center">
<img src="https://i.imgur.com/9tiOON2.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/CfCzRRk.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>


<h3>Step 3: Configure Departments</h3>

- Ensure you are still in the Admin panel
- Select the Agent tab > Departments > Add New Department 
	- Name: System Administrators
- Select Create Department 


<p align="center">
<img src="https://i.imgur.com/f2uEloL.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/X2dXwjY.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>


<h3>Step 4: Configure Teams
</h3>

- Select the Agent tab > Teams > Add New Team
	- Name: Level II Support 
- Go to the Members tab and select yourself in "Select Agent" dropdown menu
- Select Create Team
	
<p align="center">
<img src="https://i.imgur.com/v6zzN3N.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/4IieS80.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>

<h3>Step 5: Allow Anyone to Create Tickets</h3>

- Select Settings > User Settings
	- Make sure the following box is unchecked: 
		- Registration Required: Require registration and login to create tickets 
		
<p align="center">
<img src="https://i.imgur.com/kcd1jRf.png" height="80%" width="80%" alt="Azure Free Account"/>		


<h3>Step 6: Configure Agents</h3>

- Select the Agent tab > Add New Agents
	- Name: Jane Doe
	- Email : jane.doe(@)osticket.com
	- Username: jane.doe
	- Click Set Password and uncheck the box that says "Send the Agent a Password Reset Email"
		- Set your password to anything you like
		- Uncheck the box that says "Require Password Change at Next Login"
		- Select set
		
<p align="center">
<img src="https://i.imgur.com/fTvI0Ru.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/6OU5KqX.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>

- Select the Access tab 
	- Under Primary Department: 
		- Select the Department dropdown menu > System Administrators
		- Select the Role dropdown menu > Supreme Admin
	- Extended Accesss 
		- Select Department > Support > Add > Supreme Admin
- Select Team tab
	- Select Team dropdown menu > Level II Support
	- Select Add
- Select Create	

	
<p align="center">
<img src="https://i.imgur.com/HPSPHNU.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/hotx1wo.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>

- Create another agent and replace Jane with John.
	- Follow the same steps as above, except make some changes to the Primary Department
		- Select the Department dropdown menu > Support
		- Select the Role dropdown menu > View Only
	- Extended Accesss 
		- Select Department > Support > Save Changes
		
<p align="center">
<img src="https://i.imgur.com/qQ8ckBr.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/KVPsUb4.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>
 
     

<h3>Step 7: Configure Users
</h3>

<p align="center">
<img src="https://i.imgur.com/UUqCK1d.png" height="80%" width="80%" alt="Azure Free Account"/>		
	
- Select the Users tab to create a user
	- Email Address: Karen(@)osticket.com
	- Full Name: Karen Karen
	- Select Add User
	
<p align="center">
<img src="https://i.imgur.com/wpTn12W.png" height="80%" width="80%" alt="Azure Free Account"/>			
	
 - Select the User tab again to create another user
	- Email Address: Ken(@)osticket.com
	- Full Name: Ken Ken
	- Select Add User

<p align="center">
<img src="https://i.imgur.com/EXyy5Gq.png" height="80%" width="80%" alt="Azure Free Account"/>		

<h3>Step 8:  Configure Service Level Agreements (SLA)
</h3>

- We will create three SLAs
- Select the Manage tab > SLA > Add New SLA Plan
	- Name: SEV-A 			
	- Grace Period: 1
	- Schedule dropdown menu: 24/7
	- Select Add Plan
	
<p align="center">
<img src="https://i.imgur.com/fMR4yMR.png" height="80%" width="80%" alt="Azure Free Account"/> <img src="https://i.imgur.com/3tQnihq.png" height="80%" width="80%" alt="Azure Free Services"/>
</p>

	- Name: SEV-B
	- Grace Period: 4
	- Schedule dropdown menu: 24/7
	- Select Add Plan
	
<p align="center">
<img src="https://i.imgur.com/pAbQPEP.png" height="80%" width="80%" alt="Azure Free Account"/>

	- Name: SEV-C 
	- Grace Period: 8
	- Schedule dropdown menu: Monday - Friday 8AM - 5PM with U.S. Holidays
	- Select Add Plan

<p align="center">
<img src="https://i.imgur.com/5cgn0oz.png" height="80%" width="80%" alt="Azure Free Account"/>



<h3>Step 9:   Configure Help Topics
</h3>

- We will create four Help Topics
- Select the Manage tab > Help Topics > Add New Help Topic
	- Business Critical Outage
	- Personal Computer Issues
	- Equipment Request
	- Password Reset
- Select Add Topic for each topic

<p align="center">
<img src="https://i.imgur.com/uFmSyqK.png" height="80%" width="80%" alt="Azure Free Account"/>



Congratulations! You have configured osTicket succesfully! Click [here]() to move on to the final part of this tutorial! 
