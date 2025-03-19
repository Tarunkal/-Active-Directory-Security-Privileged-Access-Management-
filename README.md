# -Active-Directory-Security-Privileged-Access-Management-

# Objective

I'm currently working on building a secure and functional Active Directory (AD) environment designed for learning, testing, and enhancing technical skills in AD administration. This project involves configuring Group Policies, implementing security controls, and simulating real-world enterprise conditions to demonstrate essential AD features and best practices. The goal is to create a robust environment that mirrors real-world scenarios, improving my understanding of AD security and management.

## Step-by-Step Methodology

1. **Install Windows Server 2016**
   - Install the Windows Server 2016 operating system.
   - Configure network settings and assign a static IP address.

2. **Install Active Directory Domain Services (AD DS)**
   - Add the AD DS role via Server Manager.
   - Promote the server to a **Domain Controller** with DNS and Global **Catalog** roles.

3. **Create a New Forest and Domain**
   - Specify the root domain name as `_WindowAD.local_`.
   - Configure the **Directory Services Restore Mode (DSRM)** password.

4. **Organizational Unit (OU) Structure Creation**
   - Create the following OUs under `_Homelab_`:
     - IT  
     - HR  
     - Finance  
     - Marketing  
   - Add respective users and computer accounts to their designated OUs.
5. **Group Policy Configuration**
   - Open Group Policy Management.
   - Modify password policies to enforce:
     - **Enforced password history:** 24 passwords remembered  
     - **Maximum password age:** 42 days  
     - **Minimum password length:** 6 characters  
     - **Password complexity requirements:** Enabled  

6. **Computer Account Management**
   - Create computer objects for each department.  
   - Assign **Domain Admins** permissions for IT OU computers.  

7. **PowerShell Automation for Delegation and Password Control (In Progress)**
   - Delegate IT team members with permissions to reset passwords for users in other departments.  
   - Automate user creation and password management using PowerShell.  
   - Set a **single logon password** for all users and enforce **password change on first login** using PowerShell scripts.  

8. **Future Enhancements**
   - Implement **Sysmon** for advanced endpoint monitoring.  
   - Integrate **CrowdSec** for enhanced threat intelligence.  
   - Deploy **BadBlood** to simulate AD misconfigurations and improve security hardening techniques.
      
## Tools and Technology Used
  - Windows Server 2016 (Domain Controller)
  - Active Directory Domain Services (AD DS)
  - Group Policy Management
  - Windows 10 (Client System)
  - PowerShell (for automation)

## Key Features and Configurations
1. **Active Directory Installation**
   - Installed Active Directory Domain Services (AD DS)
   - Created a new forest with the root domain name: `_WindowAD.local_`
   - Configured DNS and Global Catalog (GC) roles

