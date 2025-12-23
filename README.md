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
   - Specify the root domain name as `WindowAD.local`.
   - Configure the **Directory Services Restore Mode (DSRM)** password.

4. **Organizational Unit (OU) Structure Creation**
   - Create the following OUs under `Homelab`:
     - IT  
     - HR  
     - Management 
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


## Tools and Technology Used
  - Windows Server 2016 (Domain Controller)
  - Active Directory Domain Services (AD DS)
  - Group Policy Management
  - Windows 10 (Client System)
  - PowerShell (for automation)

## Key Features and Configurations
1. **Active Directory Installation**
   - Installed Active Directory Domain Services (AD DS)
   - Created a new forest with the root domain name: `WindowAD.local`
   - Configured DNS and Global Catalog (GC) roles
  
2. **Organizational Unit (OU) Structure**
   - Created an IT Department OU under `Homelab`
   - Created OUs for all other departments under `Homelab`
   - Added multiple user accounts and computer objects for structured access control

3. **Group Policy Management (GPO)**
   - Modified password policy to enforce stronger security measures:
     - Enforced password history: 24 passwords remembered
     - Maximum password age: 42 days
     - Minimum password length: 6 characters
     - Password complexity requirements: Enabled
    
4. **Computer Account Management**
   - Created new computer objects in the IT OU for endpoint management
   - Ensured computer accounts are properly registered with the AD domain
  
5. **PowerShell Automation for Delegation and Password Control (In Progress)**
   - Delegating IT team members with permissions to reset passwords for users in other departments
   - Automating user creation and password management using PowerShell
   - Setting a single login password for all users and enforcing password change on first login

## How to Set Up the Lab 
 1. Install Windows Server 2016 and configure it as a Domain Controller.
 2. Create OUs for your organizational structure.
 3. Add users and computers to their respective OUs.
 4. Implement Group Policy configurations to enforce security policies.
 5. Use PowerShell to automate user creation, delegation, and password enforcement.
 6. Monitor and manage the environment for improved AD security.
      

## Screenshots

![Image](https://github.com/user-attachments/assets/5525a6e0-1fdc-4a5f-afdb-fca816213679)

           Fg 1. AD Installation Process


![Image](https://github.com/user-attachments/assets/21cf1299-195f-485a-a470-fbcf22b73d77)

        Fg 2. Setup Root Domain Password



![Image](https://github.com/user-attachments/assets/cabfcbb7-9bfc-442b-9b88-23576bc48136)
         
        Fg 3. Setting New Doamin Local

![Image](https://github.com/user-attachments/assets/77bd185b-e568-4816-98fb-ea835af5fa82)

         Fg 4. organization unit Active Directory

![Image](https://github.com/user-attachments/assets/99d34f81-dbbb-41f1-b104-3a366daa7a83)

         Fg 5. AD Users

![Image](https://github.com/user-attachments/assets/75b01f85-6051-4d15-8107-f287e1f18590)

         Fg 6. AD Machines

![Changing Computer properties](https://github.com/user-attachments/assets/4d1cf726-faab-4f58-8f71-15d599d8ed2d)

           Fg 7. Machine owner
         

 ![Image](https://github.com/user-attachments/assets/9b16048c-fd2f-4974-8452-ae1667c23b45)

         Fg 8. DC Linked GPO 

 ![Image](https://github.com/user-attachments/assets/eb203407-a1de-40e9-b770-dd02cb5f349d)

         Fg 9. Changing password policy in GPO
        
