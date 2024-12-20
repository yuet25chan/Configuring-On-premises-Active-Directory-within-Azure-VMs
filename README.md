# Configuring-On-premises-Active-Directory-within-Azure-VMs
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1
- Step 2
- Step 3
- Step 4

<h2>Deployment and Configuration Steps</h2>

<p>

![image](https://github.com/user-attachments/assets/26b356e5-761a-4aa8-a847-10e72e7a5564)

![image](https://github.com/user-attachments/assets/cbb2d37e-cfd8-4243-b4b2-b39c355d26b4)

![image](https://github.com/user-attachments/assets/ee544e03-7b19-48e4-9bde-cfcb02c37876)

![image](https://github.com/user-attachments/assets/8761d483-31d4-41e2-92a5-c72e1869c59a)



</p>
<p>
  
Click on the client-1's Network Settings. Then click on Network Interface/IP Configuration. Then click on DNS Server. 

![image](https://github.com/user-attachments/assets/61e6f200-3be4-49ee-abc6-80b60ccaecc1)

Click on DNS Server. Select Custom and enter dc-1's private IP address. 

![image](https://github.com/user-attachments/assets/49ae430d-3ef5-4e42-8255-5980f43ddba7)



</p>
<br />

<p>

After VM is created, set Client-1’s DNS settings to DC-1’s Private IP address
From the Azure Portal, restart Client-1
Login to Client-1
Attempt to ping DC-1's private IP address

<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<h2> Install Active Directory </h2>

<p>

![image](https://github.com/user-attachments/assets/1dfcaff6-3de9-403c-9a5c-b858c52938dc)

</p>
<p>
Login to DC-1 and install Active Directory Domain Services. 

Login to DC-1 and select Server Manager from the Start Menu. 

</p>

<p>

![image](https://github.com/user-attachments/assets/f062f352-af7d-4f3d-b1c3-80ee4b18e3b2)

</p>

<p>
Click on "Add Roles and Features".

</p>

<p>


![image](https://github.com/user-attachments/assets/b22bd92f-778c-47ae-abfd-55cf54b8f65c)
 
</p>

<p>
On the Select Installation Type Tab, select Role-based or feature-based installation and click "Next".   

</p>

<p>

![image](https://github.com/user-attachments/assets/487d5bd5-6ee0-4a7a-b498-e00b74479548)

</p>

<p>

Select DC-1 as the server under the Server Selection tab and click "Next".

</p>

<p>

![image](https://github.com/user-attachments/assets/54cac71a-6895-40cd-bafa-2fbacfa4edfe)


</p>

<p>

Select "Active Domain Services" under the "Server Role" tab and click "Next". 

</p>

<p>

![image](https://github.com/user-attachments/assets/c2dfbd8a-b549-44bf-8607-6228db7e8f50)


</p>

<p>
Click on "Add features". 

</p>

<p>

![image](https://github.com/user-attachments/assets/6e6b212d-5a1c-4450-a607-0e186e42abd1)


</p>

<p>
Click "Next". 

</p>

<p>
  
![image](https://github.com/user-attachments/assets/4c2bd1b9-3b34-4cc5-a287-965101408f0d)

</p>

<p>
Click "Next".
  
</p>


<p>
  
![image](https://github.com/user-attachments/assets/1c163325-31c7-458c-8b15-5538a357dfd1)

</p>

<p>
Check the box, click "Next" and then click "Install". 
</p>
<br />

<p>

![image](https://github.com/user-attachments/assets/c0d96718-edd2-4b1a-a1a0-29aa217b75af)

</p>

<P>

Once the Active Directory has been installed, we can promote DC-1 as a domain controller. To promote it as a domain controller, we need to click on the flag on the upper right and click "Promote this server to a domain controller". 

</P>


<p>

![image](https://github.com/user-attachments/assets/c1ca72c2-c209-4f84-8e34-ca4459a0312c)

</p>

<p>

Select "Set as a Forest", enter the domain name, and click "Next". 


</p>

![image](https://github.com/user-attachments/assets/62f8688e-d209-43d3-911f-fd700adbd81c)


<p>

<P>

Enter the password. 

</p>

<p>
  
![image](https://github.com/user-attachments/assets/6a146019-5715-4cdb-bbb4-465a6aac0f10)


</p>

<p>

Leave the box unchecked and click "Next". 

</P>

<p>

![image](https://github.com/user-attachments/assets/b075c1f9-3757-41f1-ae08-19b53dad12e6)

</p>

<p>
Click "Next". 
</p>

<p>

![image](https://github.com/user-attachments/assets/78beabde-edeb-4148-b25a-a33a806b0193)


</p>

<p>

Click "Next". 

</p>

<p>

![image](https://github.com/user-attachments/assets/989c8794-55bc-48c3-8e3b-773e95af306d)


</p>

<p>

Click "Next". 

</p>

<p>

![image](https://github.com/user-attachments/assets/c8ad599a-7d06-4e0b-b838-0e869bb11bf7)

</p>

<p>

Click "Install".

</p>

<p>

After the active directory has been installed, log out to restart and then log back into DC-1 as user:mydomain.com\labuser. 

</p>

![image](https://github.com/user-attachments/assets/a6020289-3610-44dd-9deb-f93323418aeb)


</p>

<p>

Once logged in, Click on the Start menu. Click "Windows Administrative Tools" and open "Active Directory Users and Computers". 

</p>

<p>

![image](https://github.com/user-attachments/assets/91fce6f8-44e6-4624-a222-a5cc02ca05b3)

![image](https://github.com/user-attachments/assets/e37c6b9a-c9cf-45b5-ac31-3f812c67f9e8)

![image](https://github.com/user-attachments/assets/ffc20837-d7e5-4995-accd-8b4a38e97db4)

![image](https://github.com/user-attachments/assets/3314776c-730f-4e43-80c8-cc713de944e3)

</p>

<p>

In Active Directory Users and Computers (ADUC), create an Organizational Unit (OU) called “_EMPLOYEES”

</p>

<p>

![image](https://github.com/user-attachments/assets/3201662f-1cce-4fd9-9f33-8f8e8f057c66)


![image](https://github.com/user-attachments/assets/ddd87feb-d39a-4e9b-b4af-89553cf8cad5)
</P>

<p>
  
Create a new OU named “_ADMINS”.

</p>

![image](https://github.com/user-attachments/assets/df9433e7-3e1e-4e56-b8c0-e703d2a38876)

![image](https://github.com/user-attachments/assets/d7cbd056-f216-4e73-a1b9-5af347d054d8)

![image](https://github.com/user-attachments/assets/c40bef18-4190-4f5a-b3e7-dfeae2088289)

![image](https://github.com/user-attachments/assets/17af0896-bc22-41c0-b0a6-58ac2e02c580)


</P>

<p>

Right-click the "_ADMINS" folder, then click "New" and then click "Users." Create a new employee named “Jane Doe” (same password) with the username “jane_admin” and enter the password. Click "Finish." 

</P>

<p>

![image](https://github.com/user-attachments/assets/66bc5653-db8f-4b3a-9982-b304f0568419)

![image](https://github.com/user-attachments/assets/85e87008-a021-4627-a799-ff30a8e29ca0)

![image](https://github.com/user-attachments/assets/ddd77647-1d70-44a1-bc54-f81df08e32d2)

![image](https://github.com/user-attachments/assets/af6f317e-f0a8-40a6-b3d9-55920a13e7a6)

</p>

<p>

In the "_ADMINS" folder, right-click Jane Doe. Select "Properties" and click on the "Member of" tab. Add Jane Doe as "Domain Admin" and click "Apply". Log out / close the connection to DC-1 and log back in as “mydomain.com\jane_admin”. Use jane_admin as your admin account from now on


</p>

<p>
  
![image](https://github.com/user-attachments/assets/b5ac0423-884e-4f7b-8466-313273fed4ae)

![image](https://github.com/user-attachments/assets/6381e569-300d-4514-9fef-533c0a48e65b)


</p>

<p>

Login to Client-1 as the original local admin (labuser). Once logged in, right-click the "Start" Menu, then click "Settings" and then click "Rename this PC (Advanced)". Under the Computer Name tab, click on "Change". Join mydomain.com. Log in with mydomain.com\jane_admin. 

</p>


<p>

![image](https://github.com/user-attachments/assets/7c388edc-e21d-464e-9f2e-f4618c1dd5f4)

![image](https://github.com/user-attachments/assets/bc915c92-9c4c-4b01-a715-76ccee6caa87)

![image](https://github.com/user-attachments/assets/00eb74c4-0517-4e80-b86a-5f8a74b4d5a7)


</p>

<p>

You can log in to the Domain Controller and verify that Client-1 shows up in ADUC. Create a new OU named “_CLIENTS” and drag Client-1 into there. 

</p>
<br/>

<h2> Setup Remote Desktop for non-administrative users on Client-1 </h2>

<p>
  
![image](https://github.com/user-attachments/assets/b521b43e-29de-4216-bd49-06824accd26f)

![image](https://github.com/user-attachments/assets/1199e506-385b-4282-8d56-936337c9594b)

![image](https://github.com/user-attachments/assets/74f48afe-ff0a-43e0-b55a-fc38e36de400)

![image](https://github.com/user-attachments/assets/ddfb866d-cf5c-4d8e-912b-89d0be6a40e1)




</p>

<p>

Right-click the "Start" icon and click "System" on the menu. Click on "Remote Desktop". Select "Users that can remotely access this PC". Add "domain users" to "domain users" access to the Remote Desktop. 


</p>

<h2> Create a bunch of additional users and attempt to log into client-1 with one of the users </h2>

<p>

![image](https://github.com/user-attachments/assets/7a778288-4322-401d-b691-b704a2c1bc86)

![image](https://github.com/user-attachments/assets/6910ad4b-7a52-4a3b-982b-0927697336c6)

![image](https://github.com/user-attachments/assets/77e26897-c3fb-4db0-be4c-fce182bbcafd)

![image](https://github.com/user-attachments/assets/51ae5fb6-55f7-4835-9708-7e2fa8ca70f1)




</p>

<p>
  
Log in to dc-1. Right-click "Windows Powershell ISE" and select "Run as administrator." Once the Windows Powershell is open, open a new file. Save the Powershell file as "Create Users" on the desktop. paste the contents of the script into it. Click on the green arrow to run the script. 
</p>

<p>
  
![image](https://github.com/user-attachments/assets/6979884e-3307-4aa5-b77f-1c8a84352bed)

![image](https://github.com/user-attachments/assets/3309a76a-74e0-44eb-a197-c513c8968d85)

![image](https://github.com/user-attachments/assets/c46a06ef-5a38-4210-9384-d7002ac35d89)




</p>

<p>
  
While the users are still being created, we can refresh the "_Employees" folder in "Active Directory Users and Computers" to see the users that have been created. Randomly select one of these accounts that have been created and login to client-1 with the user name and "Password1", a default password that has been set for all these accounts. Let's try logging in with the username "babe.mexo" and the default password. The login was successful. To verify this, you can open the Command Line and see if it has a local profile on this computer. 


</p>
