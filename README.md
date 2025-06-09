# Configuring On-Premises Active Directory within Azure VMs

<p align="center">
  <img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

## Overview

This tutorial outlines the steps to deploy and configure an **on-premises-style Active Directory** environment using **Azure Virtual Machines**.

---

## 🧰 Technologies & Tools Used

- **Microsoft Azure** (Virtual Machines / Compute)
- **Remote Desktop**
- **Active Directory Domain Services**
- **PowerShell**

---

## 💻 Operating Systems

- **Windows Server 2022** (Domain Controller)
- **Windows 10 (21H2)** (Client Machine)

---

## 🔧 High-Level Steps

1. Create and configure Azure VMs (DC-1 and Client-1)
2. Set up networking and DNS between VMs
3. Install and configure Active Directory on DC-1
4. Join Client-1 to the domain
5. Create users and Organizational Units (OUs)
6. Enable Remote Desktop for domain users
7. Create bulk users using PowerShell and test login

---

## 🚀 Deployment & Configuration

### 🔹 Network and DNS Configuration

- Set **Client-1's DNS** to **DC-1's private IP**
- Restart Client-1
- Verify connectivity by pinging DC-1

### 🔹 Installing Active Directory on DC-1

1. Open **Server Manager** on DC-1
2. Click **Add Roles and Features**
3. Select:
   - Role-based installation
   - Active Directory Domain Services
4. Follow prompts to install, then click the flag icon → **Promote this server to a domain controller**
5. Create a **new forest**, set domain name, and complete installation
6. Log in as: `mydomain.com\labuser`

---

## 👥 Active Directory Configuration

- Open **Active Directory Users and Computers (ADUC)**
- Create OUs:
  - `_EMPLOYEES`
  - `_ADMINS`
- Create user **Jane Doe** (`jane_admin`)
- Add `jane_admin` to **Domain Admins**
- Log out and back in as `mydomain.com\jane_admin`

---

## 🖥️ Domain Join and Remote Desktop

- Log in to **Client-1** as local admin
- Join it to the domain: `mydomain.com`
- Log in using domain admin credentials
- Move Client-1 to a new OU `_CLIENTS` in ADUC
- Enable **Remote Desktop** and allow **Domain Users**

---

## ⚙️ Bulk User Creation with PowerShell

1. Log in to DC-1
2. Open **PowerShell ISE as Administrator**
3. Create and run a script to generate test users
4. Confirm users appear in `_EMPLOYEES` OU
5. Log in to Client-1 using one of the test accounts

---

## ✅ Verification

- Confirm test user login is successful
- Use `whoami` or `echo %username%` to verify domain login
- Check local profiles on Client-1

---

## 📎 Notes

- All test users are created with the default password: `Password1`
- Ensure network security groups and firewalls allow RDP
- Consider setting password expiration policies for real deployments

---

© 2025 | Tutorial by Yuet Chan
