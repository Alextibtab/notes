---
Area: Cyber Security
Platform: TryHackMe
THM Room: https://tryhackme.com/room/winadbasics
tags:
  - thm
  - active_directory
---
# Windows Active Directory Basics
## Windows Domains
A windows domain is a group of users and computers under the administration of a given business. The main idea behind a domain is to centralise the administration of common components of a windows network into a single repository called **Active Directory (AD)**. The server that runs the active directory services is known as a **Domain Controller (DC)**.

The main advantages of having a configured windows domain are:
- **Centralised Identity Management**: All users across the network can be configured from Active Directory with minimum effort,
- **Managing Security Policies**: You can configure security policies directly from Active Directory and apply them to users and computers across the network as needed.

The core of any Windows Domain is the **Active Directory Domain Service (AD DS)**. This service acts as a catalogue that holds the information of all of the "objects" that exist on the network. Amongst the many objects supported by AD, there is users, groups, machines, printers and many others.

### Users
Users are one of the most common object types in Active Directory. Users are one of the objects known as **security principals**, meaning that they can be authenticated by the domain and can be assigned privileges over **resources** like files or printers. A security principal is an object that can act upon resources in the network.

Users can be used to represent two types of entities:
- **People**: users will generally represent persons in an organisation that need to access the network like employees.
- **Services**: you can also define users to be used by services like IIS or MSSQL. Every single service requires a user to run, but service users are different from regular users as they will only have privileges needed to run their specific service.

### Machines
Machines are another type of object within Active Directory; for every computer that joins the Active Directory domain, a machine object will be created. Machines are also considered "security principals" and are assigned an account just as any regular user. This account has somewhat limited rights within the domain itself.

The machine accounts themselves are local administrators on the assigned computer, they are generally not supposed to be accessed by anyone except the computer itself, but as with any other account, if you have the password, you can use it to log in.

Identifying machine accounts is relatively easy. They follow a specific naming scheme. The machine account name is the computer's name followed by a dollar sign. Example a machine with the hostname `DC01` will become `DC01$`

### Security Groups
Security groups are also considered security principals and, therefore can have privileges over resources on the network.

Groups can have both users and machines as members, if needed groups can include other groups as well.

Several groups are created by default in a domain that can be used to grant specific privileges to users.

| Security Group     | Description |
| ------------------ | ----------- |
| Domain Admins      | Users of this group have administrative privileges over the entire domain. By default, they can administer any computer on the domain, including the DCs.            |
| Server Operators   | Users in this group can administer Domain Controllers. They cannot change any administrative group memberships.            |
| Backup Operators   | Users in this group are allowed to access any file, ignoring their permissions. They are used to perform backups of data on computers.            |
| Account Operators  | Users in this group can create or modify other accounts in the domain.            |
| Domain Users       | Includes all existing user accounts in the domain.            |
| Domain Computers   | Includes all existing computers in the domain.            |
| Domain Controllers | Includes all existing DCs on the domain.           |

### Organisational Units
In Windows domains, Organisational Unit (OU) refers to containers that hold users, groups and computers to which similar policies should apply. In most cases, OUs will match departments in an enterprise

Some default OUs are created by Windows automatically and contain the following:
- **Builtin**: Contains default groups available to any Windows host.
- **Computers**: Any machine joining the network will be put here by default. You can move them if needed.
- **Domain Controllers**: Default OU that contains the DCs in the network
- **Users**: Default users and groups that apply to a domain-wide context.
- **Managed Service Accounts**: Holds accounts used by services in your Windows domain.

### Security Groups vs OUs
- **OUs** are handy for applying policies to users and computers, which include specific configurations that pertain to sets of users depending on their particular role in the enterprise. A user can only be a member of a single OU at a time, as it wouldn't make sense to try to apply two different sets of policies to a single user.
- **Security Groups**, on the other hand, are used to grant permissions over resources. For example, you will use groups if you want to allow some users to access a shared folder or networked printer. A user can be a part of many groups, which is needed to grant access to multiple resources.