# Summary
Virtualized Windows server and network environment built in Hyper-V. This project includes an Active Directory domain with organizational units, security groups and group policy management. Simulated IT help desk queue in ServiceNow to document and resolve tickets.

## Contents
- [Tools](#tools)
- [Server01 IP Configuration](#server01-ip-configuration)
- [Client01 IP Configuration](#client01-ip-configuration)
- [Client Ping Test](#client-ping-test)
- [DHCP Configuration](#dhcp-configuration)
- [Active Directory Users And Groups](#active-directory-users-and-groups)
- [Access Control Testing](#access-control-testing)
- [Group Policy Configuration](#group-policy-configuration)
- [**Ticket Simulation (ServiceNow)**](#ticket-simulation)
  - [Users and Departments](#users-and-departments)
  - [Example Ticket Cases](#example-ticket-cases)

---
# Tools
- Windows Server 2022
- Active Directory
- Windows 10/11
- DNS
- DHCP
- Hyper-V
- Group Policy
- ServiceNow


---
## Server01 IP Configuration
![Server 1 IP](Project_Images/Server_1_IpConfig.png)
---
## Client01 IP Configuration
![Client 1 IP](Project_Images/Client_1_IpConfig.png)
---
## Client Ping Test
Confirming connectivity between the client and server after configuration

![Ping Test](Project_Images/Client_ServerPing_Test.png)
---
## DHCP Configuration
Scope was configured on server to automatically assign IP addresses

![Structure](Project_Images/DHCP_Config.png)
---
## Active Directory Users And Groups
Four organizational units were created to simulate a university. User accounts were created within each organizational unit.
Security group was created for each OU users were added to their group to manage shared folder permissions at the group level.

![Structure](Project_Images/Server1_ou_structure_users.png)
![Structure](Project_Images/Server1_ou_structure.png)
![SecurityGroups](Project_Images/Server1_Security_Groups.png)

## Access Control Testing
Verifying permissions were enforced by accessing a folder while logged in as a faculty user.

![Access](Project_Images/Faculty_User_In_FacultyFolder.png)

Denied access to an unauthorized department folder

![Denied](Project_Images/Faculty_User_Denied_Access.png)

Students folder permissions configuration. Shows only Students_Group and Administrators with access.

![Students](Project_Images/Server_1_Folder_Permissions.png)
---
## Group Policy Configuration
Password Policy requiring a minimum password length of 8 characters and enforcing password complexity requirements.

![Students](Project_Images/Computer_Configuration_GPO.png)

Restrictions and desktop policy. Prohibit access to control panel and pc settings and enforcing a desktop wallpaper.
![Students](Project_Images/User_Configuration_GPO.png)

## Ticket Simulation

ServiceNow was used to simulate a help desk queue for the lab environment. Users and departments were created to mirror the lab. Issues were reproduced, troubleshot, and documented with their resolutions.

### Users and Departments
![ServiceNow Users](Project_Images/servicenow_users.png)
![ServiceNow departments](Project_Images/servicenow_departments.png)

### Example Ticket Cases

#### INC0010009: New User Onboarding
**Request:** New employee Sarah Collins is starting in the Administration department and needs a domain account and access to her department's resources.

1. Created the user account in Active Directory under the administration OU. Furthermore added her to administration group to receive access to department shared folder.

![Account created](Project_Images/INC0010009_1.png)

2. Set a temporary password and making sure user changes password at next login. Sarah was able to set a new password and met the domain password policy.

![Account created](Project_Images/INC0010009_2.png)

3. Sarah signed in as scollins and opened the administration folder to confirm she could reach her department's shared folder.

![Account created](Project_Images/INC0010009_3.png)

**Resolution:** Account created and configured. The user logged in and accessed Administration resources.








