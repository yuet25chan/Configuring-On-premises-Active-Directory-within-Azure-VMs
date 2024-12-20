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

Once the Active Directory has been installed, we can promote DC-1 as a domain controller. To promote it as a domain controler, we need to click on the flag on the upper right and click "Promote this server to a domain controller". 

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

