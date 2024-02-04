![img](https://i.imgur.com/qeoorRI.png)


# Managing Entre ID Identities in Microsoft Azure

You have been tasked to provision users and group accounts within your organization. Within each job role, members within the group must have automatic updates enabled. Next, you'll create a test tenant within your organization and grant that user with limited permission. 

# Objectives

By the end of this lab, you will know how to:
- Create and configure users
- Create groups with assigned and dynamic membership
- Create a tenant
- Manage guest users


# Microsoft Entra Explained

Microsoft Entra ID is a cloud identity and access management solution that seamlessly connects an organization's users, including employees and customers, to their data, apps, and endpoints. Microsoft Entra offers strong authentication and access policies that keep resources protected. The seamlessness of Microsoft Entra comes with its speedy and effortless sign-in experience within your organization's cloud environment. Microsoft Entra's unified identity management keeps all your organization identities central, regardless of your cloud-based or on-premises environment.  

Conditional Access

<b>1.</b> In your Azure Portal, search for <b>Microsoft Entra Id</b>. Once there, on the left-hand side under <b>Manage</b>, select <b>User settings</b> and review any configurations that need to be made. Since we are the Global Admin in this scenario, it's important to consider the rule of least privilege. By default, we are allowing non-admin users to register the application and create security groups. By default, we should set these configurations to no. However, when it comes to the <b> Restricting non-admin users from creating tenant</b>, as the admin, you want to configure this setting to yes. When you go on to create users and groups, as the admin, you'll be able to grant certain users with certain capabilities such as application registration. 

For <b>Guest user access restriction</b> For now, we can give guests limited access to properties and directory objects. 
As an admin, it's important to limit who has access to admin resources such as the <b>Administration center</b> Let's set this setting to <b>Yes</b>

![img](https://i.imgur.com/iZnHNhc.png)

<B>2</B> Under the <b>Manage</b> settings, select <b>Users</b> then click <b>New user</b>. In the <b>Create new user</b> page, you'll be prompted to provide the <b>User principle name</b>, <b>Main nickname</b>, <b>Display name</b>, and <b>Password</b>. You can also choose to have the account enabled and disable it. 

The <b>Properties</b> tab gives you the ability to add a few more distinct details to your users. For this scenario, we are going to use the following information:

| Setting                   | Value
| ------------------------ | -----
| User principal name          | az104-01a-aaduser1
| Display name                   | az104-01a-aaduser1
| Auto-generate password           | de-select
| Initial password         | 	Provide a secure password
| Job title | Cloud Administrator
| Department | IT
| Usage location | 	United States

Next, let's go ahead and assign our user, <b>az104-01a-aaduser1</b> the appropriate permissions a cloud administrate would need. To do this, under <b>Manage</b>, select <b>Assigned roles</b>. Click <b>Add assignments</b> and assign the <b>User administrator</b> role to user, <b>az104-01a-aaduser1</b>. The <b>User Administrator</b> role is able to manage users and group settings, such as password resets. 

Next, open a new browser in private mode and log in as the newly created user. You should notice that when trying to adjust user settings, the permission to do so has been denied. However, you do have the capability to create a new user. 


