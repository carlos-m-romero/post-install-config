<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
Hey there! This is a guide on how to configure osTicket, an open-source help desk ticketing system, after the installation process.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- [osTicket Documentation](https://docs.osticket.com/en/latest/index.html)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)


<h2>Post-Install Configuration Objectives</h2>
Create and Configure Roles
Create and Configure Departments & Teams
Create and Configure Agents (workers) & Users (clients)
Configure SLA (Service Level Agreements)
Configure Help Desk Topics
<h2>Configuration Steps</h2>
<h3>&#9312; Prerequisites and Installation</h3>
This demonstration assumes a virtual machine is established with the prerequisite files installed for working osTicket. </br>
Credentials and configurations that will be used in this demonstration can be found in "Prerequisites and Installation". </br>

<hr>
<h3>&#9313; Admin Panel - Roles, Departments, Teams, & Agents</h3>
On the web browser (Microsoft Edge), go to the Help Desk Login Page and sign in to your osTicket Help Desk credentials (this example uses username ostuser / ostuser@email.com).
Help Desk Login Page -- http://localhost/osTicket/scp/login.php

![4](https://github.com/carlos-m-romero/post-install-config/assets/148396073/43e5812c-1c98-4990-bf37-f12977d85a4f)
![5](https://github.com/carlos-m-romero/post-install-config/assets/148396073/63f2b604-6a24-43b8-afbb-f1e743392c03)

Currently, at the Agent Panel, click on "Admin Panel" at the top-right of the page.

![6](https://github.com/carlos-m-romero/post-install-config/assets/148396073/71d7a032-9a07-499f-b671-0452f09884c5)


Click on the "Agents" tab > "Roles" > "Add New Role".

![7](https://github.com/carlos-m-romero/post-install-config/assets/148396073/404a968d-4552-40a1-bce0-9cf3bacd62cf)



"Roles are the permissions granted to Agents per Department that they have access to."

In the Definition tab, type any Role name of your choice (this example uses Supreme Admin).
This role will be given all permissions.
Then, click on the Permissions tab.


![8](https://github.com/carlos-m-romero/post-install-config/assets/148396073/487fe89f-bbf1-4576-8981-4940148e9e14)


In the Permissions tab, under the Tickets category, checkmark ALL boxes.
Go through both Tasks and Knowledgebase categories and checkmark ALL boxes as well.
Once done, click "Add Role".

![9](https://github.com/carlos-m-romero/post-install-config/assets/148396073/08933841-298d-4866-b013-822ddec03932)


Now we've created a Supreme Admin role with all permissions granted. Next, we'll create a Department.

Currently, in the Agents tab, click on the "Departments" category.
Click "Add New Department".

![10](https://github.com/carlos-m-romero/post-install-config/assets/148396073/45bf89a6-b089-4ca4-a511-f56c30944c26)


Create a Department name of your choice (this example uses System Administrators).
Skip everything else for now and click "Create Dept".

![11](https://github.com/carlos-m-romero/post-install-config/assets/148396073/bc7e6ce9-674a-469c-bc3a-2524de22d4ec)


Next, we'll move on to creating a Team. <br>
"Teams allow you to pull Agents from different Departments and organize them to handle a specific issue or user via a Help Topic or Ticket Filter."

Currently, in the Agents tab, click on the "Teams" category.

Click "Add New Team".

![12](https://github.com/carlos-m-romero/post-install-config/assets/148396073/0ae78b49-1a51-4cf1-8bbd-6d6a6bf4302f)



Create a Team name of your choice (this example uses Level II Support).
Click "Create Team".


![13](https://github.com/carlos-m-romero/post-install-config/assets/148396073/75edc430-7e7d-4660-b078-6cb45bd6984b)


Currently, in the Agents tab, click "Agents" category.

![14](https://github.com/carlos-m-romero/post-install-config/assets/148396073/aafc4350-f590-4e56-8a62-e098bfb8dd60)


Create the required credentials for this user that are in bold:
First Name (this example uses Jane).
Last Name (this example uses Doe).
Email Address (this example uses jane.doe@osTicket.com).
Username (this example uses jane.doe).
Click "Set Password" and a windows prompt will appear:
Uncheck "Send the agent a password reset email".
Create a password for this user.
Uncheck "Require password change at next login".
Click "Set".


![15](https://github.com/carlos-m-romero/post-install-config/assets/148396073/e3895776-a8f8-4245-bcd4-514b064c2567)


Click on the "Access" tab:
Assign this user the Department that we created (this example uses System Administrators).
Assign this user the Role that we created (this example uses Supreme Admin).
Under Extended Access, assign this user the "Support" department with the "Supreme Admin" role.
Click "Save Changes".


![16](https://github.com/carlos-m-romero/post-install-config/assets/148396073/00e1b3a2-09ff-4049-a9f3-ae37d80ae4ca)


Click on the "Teams" tab:
Assign this user the Team that we created (this example uses Level II Support).
Once done, click "Create".


![17](https://github.com/carlos-m-romero/post-install-config/assets/148396073/ce870cc9-7fa6-4bc2-b062-3e7ef92531f0)


Create another Agent following the steps, however assign it to a different Role and Department.</br>
This example creates Agent "John Doe" | Department: "Level I Support" | Role: "View only | Extended Access: Support".


![18](https://github.com/carlos-m-romero/post-install-config/assets/148396073/221d06e2-abfc-4e20-8cc4-f5a61cc639da)


<hr>
<h3>&#9314; Agent Panel - Creating Users</h3>
Click on "Agent Panel" on the top-right of the page.

![19](https://github.com/carlos-m-romero/post-install-config/assets/148396073/faf82e96-f908-4bf6-8bff-9322edd95cd8)


Click on the "Users" tab.
Click on "Add User".
Create an Email Address and Full Name for this user (this example uses karen@osticket.com / Karen Karen).
Click "Add User".

![20](https://github.com/carlos-m-romero/post-install-config/assets/148396073/a0c19bd1-be61-414c-85f5-70164ab6cbb2)
![21](https://github.com/carlos-m-romero/post-install-config/assets/148396073/7a151a8d-429b-4aab-a455-e04561eb4e5b)


Create another user of your choice (this example uses ken@osticket.com / Ken Ken)

![22](https://github.com/carlos-m-romero/post-install-config/assets/148396073/b8cf4052-965c-490a-8045-0c70007d0894)


<hr>
<h3>&#9315; Admin Panel - Configuring SLA</h3>
"SLA Plans or Service Level Agreements, are unlimited in osTicket. The purpose of the SLA Plan is to provide a length of time in which the help desk Administrator expects tickets to be closed."

Return to the "Admin Panel".
Navigate to "Manage" tab > "SLA".
Click "Add New SLA Plan".


![23](https://github.com/carlos-m-romero/post-install-config/assets/148396073/99776d59-058a-4a55-ad69-0287554e07fe)


Create the following plans:
SEV-A

Grace Period: 1 hour (Amount, in hours, before tickets with this SLA will become overdue if not closed in allotted time.)
Schedule: 24/7 (Accounted for all days of the week, even on non-business days)
SEV-B

Grace Period: 4 hours
Schedule: 24/7
SEV-C

Grace Period: 8 hours
Schedule: Monday - Friday 8am - 5pm with U.S. Holidays
Click "Add Plan" for each.

![24](https://github.com/carlos-m-romero/post-install-config/assets/148396073/e66e36c8-648a-4feb-9e62-f1055b907309)

![25](https://github.com/carlos-m-romero/post-install-config/assets/148396073/b8911971-8159-47bf-b5cc-5fc25f49696b)



<hr>
<h3>&#9316; Configure Help Topics</h3>
Help Topics will help streamline your end-user’s help desk experience to ensure proper assignment and prompt response to the ticket.

Currently in the Admin Panel, navigate to "Manage" tab > "Help Topics".
Click "Add New Help Topic".


![26](https://github.com/carlos-m-romero/post-install-config/assets/148396073/6b638f60-6256-47a0-9039-80efa2416a1e)


Create Help Topics with the following names:
Business Critical Outage
Personal Computer Issues
Equipment Request
Password Reset
"Internal Notes" can be written down for personal use, but not necessary.
After that, click "Add Topic".

![28](https://github.com/carlos-m-romero/post-install-config/assets/148396073/9e17a313-b573-41de-b79f-b3913cb76d9d)
![27](https://github.com/carlos-m-romero/post-install-config/assets/148396073/3fa5e689-22ed-495d-a289-88d8ba7bfb7a)




<hr>
<h1><p align=center>All Done</p></h1

<h2><p align=center>Next Demonstration:<br><a href="https://github.com/JasonDelahoussaye/ticket-lifecycle">Ticket Lifecycle Examples</a></p></h2>
