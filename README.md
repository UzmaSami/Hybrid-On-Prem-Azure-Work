# Hybrid-On-Prem-Azure-Work
# Active Directory Domain Controller with GPO and Azure AD Sync Project
## Project Overview
This Project demonstrates the deployment of a Windows Server Active Directory environment including:
Configuration of a Domain Controller
Joining a client machine to the domain
Implementation of Group Policy Objects (GPOs)
Integration with Microsoft Entra ID (Azure Active Directory) using Azure Ad Connect

This simulates a real-world hybrid identity infrastructure used in entraprise environments.
### Technologies Used
Windows Server 2022 (Domain Controller)
Windows 10 Pro Client Machine
Active Directory Domain Services (AD DS)
DNS Server Role
Group Policy Management (GPO)
Microsoft Entra ID (Azure AD)
Azure AD Connect
### Archirecture Overview
-------------------
Windows Server (Domain Controller)
        │
        ├── DNS Server
        ├── Active Directory Domain
        ├── Group Policies
        │
        └── Client Machine (Domain Joined)

        │
        ▼
Azure Cloud
-------------------
Microsoft Entra ID (Azure AD)
Azure AD Connect Syn
## Step-by-Step Deployment Guide
### Step1: Setup Domain Controller
1: Install Windows Server 2022
2: Set Static IP address
3: Install role: 
    >: Active Directory Domain Services (AD DS)
4: Promote server to DOmain Controller
    >: Create new forest (fatimazahrauzmasami.pk)
5: Install and configure DNS Server
### Step2: Create Active Directory Structure
1: Open Active Directory Users and Computers (ADUC)
2: Create:
   >: Organization Unite (OUs)
   >: Users
   >: Computers
   >: Groups
3: Create test user accounts
### Step3: Configure Client Machine
1: Install Windows 10 Pro
2: Set DNS to Domain Controller IP
3: Join system to domain:
   >: System Properties --> Computer Name --> Domain
4: Restart Machine
5: Login using Domain Credentials
### Step 4: Configure Group Policies (GPOs)
1: Open Group Policy Management Concole
2: Create new GPO 
3: Link to OU
4: Configure policies such as:
   >: Password policy
   >: Account lockout policy
   >: Disable Control Panel
   >: Desktop restrictions
5: Appli Policy:
    gpupdate /force
### Step 5: Azure AD Integration
1: Install Azure AD Connect
2: Sign in with Azure admin account
3: Select: 
     >: Password Hash Synchronization
4: Connect:
     >: On-prem Active Directory --> Azure AD
5: Start synchronization
Verify in Microsoft Entra Admin Center
### Step 6: Verify Sync
   >: Check users appear in Azure AD
   >: Confirm sync status is "Healthy"
# Author
# Uzma Shabbir

##
