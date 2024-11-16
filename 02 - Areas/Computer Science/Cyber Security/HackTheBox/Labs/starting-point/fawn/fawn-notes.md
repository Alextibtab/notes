---
lab_type: [[Starting Point Labs]]
platform: HTB
---
Machine Name: Fawn
Machine IP: 10.129.1.14

Task 1: What does the 3-letter acronym FTP stand for? File Transfer Protocol

Task 2: What communication model does FTP use, architecturally speaking? client-server model

Task 3: What is the name of one popular GUI FTP program? filezilla

Task 4: Which port is the FTP service active on usually? 21 tcp

Task 5: What acronym is used for the secure version of FTP? SFTP

Task 6: What is the command we can use to test our connection to the target? ping

Task 7: From your scans, what version is FTP running on the target? vsftpd 3.0.3

Task 8: From your scans, what OS type is running on the target? unix

![[fawnNmap.png]]

#### 10.129.1.14

| Port | State | Service | Version |
|------|-------|---------|---------|
| 21/tcp | open | *ftp* | vsftpd 3.0.3 |

![[fawnFtp.png]]

Root Flag: 035db21c881520061c53e0536e44f815

up: [[Starting Point Labs]]
tags: #HTB #Starting_Point #Labs 