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
</p>
<br />
