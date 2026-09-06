# Summary
Virtualized Windows server and network environment built in Hyper-V. This project includes a Active Directory domain with organizational units, security groups and group policy management. 
Also includes simulated IT help desk ticketing using ServiceNow.

---
# Tools
- Windows Server 2022
- Active Directory
- ServiceNow
- Windows 10/11
- DNS
- DHCP
- Hyper-V
- Group Policy


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
## Active Directory Users And Groups
Four organizational units create to simulate a university. User accounts were created within each organizational unit.
Security group was created for each OU users were added to their group to manage shard folder permissions at the group level.
![Structure](Project_Images/Server1_ou_structure_users.png)
![Structure](Project_Images/Server1_ou_structure.png)
![SecurityGroups](Project_Images/Server1_Security_Groups.png)

## Access Control Testing

Verifying permissions were enforced by accessing a folder while logged in as a faculty user.
![Access](Project_Images/Faculty_User_In_FacultyFolder.png)
Denied access to an unauthorized department folder
![Denied](Project_Images/Faculty_User_Denied_Access.png)




