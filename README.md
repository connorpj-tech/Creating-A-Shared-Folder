<h1>Creating a Shared Folder</h1>

<h2>Objective</h2>
This SOP will create a shared folder for users to backup files to the Active Directory Server with the ability to distribute files to users associated with the Active Directory Domain
<h2>Utilities Used</h2>

- <b> Microsoft Azure</b>
- <b> Windows Server 2025</b>
- <b> Group Policy Management</b>
- <b> Windows 11 Pro Edition</b>

<h2>Key Steps</h2>

**1. File and Storage Services**

- <b> While on the home page of Server Manager, on the left hand screen select File and Storage Services**
- <b> Right click and select New Share
- <b> Keep the Share Profile and Location as default.  Name share mydomain.local
- <b> Click next through the wizard and create share

**2. Create a Home Folder**

- <b> In file explorer follow the path This PC> C:> Shares > mydomain.local
- <b> Create a new folder HOME
- <b> Right click on folder and select Properties.  Under the sharing tab select Advanced Sharing
- <b> Checkmark Share Folder and click apply

**3. Secure Folder**

- <b> While in properties select the Security Tab and click on advanced
- <b> Disable inheritance and select Convert Inhertied permissions into explicit permissions
- <b> Remove Users to secure the folder only to authorized users
- <b> Click on Add and Select a Principle
- <b> Type in authorized Users that will be able to use this folder.  Select Check Names and click okay
- <b> Checkmark Modify and click okay.  Check Home properties to verify user is authenticated
- <b> Under the Shared tab click on share to give user Read/Write permissions.  Click on share to give user access  

**4. Change User Settings**

- <b> In the properties tab of the shared folder, go to the shared tab and copy the Network Path
- <b> Open Active Directory Users and Computers and select the User.  Right click and select properties
- <b> Under the Profile tab select Home Folder: Connect
- <b> Assign a letter to the drive and paste the file path of the folder.  Click apply and okay to save settings

**5. Login as User**

- <b> Login as the authorized user to a Windows 11 Pro workstation associated with the Active Directory Domain Server
- <b> Open File Explorer and click on This PC.  Under Network Sharing open new shared folder
- <b> Right click to create a new text document to make sure user is authenticated.  Verify the text document appears on the Domain Controller's home folder as well
- <b> 
