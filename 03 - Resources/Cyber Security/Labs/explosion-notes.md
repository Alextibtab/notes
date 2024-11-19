---
Resource: Cyber Security
Lab Type: "HTB: Starting Point Labs"
Platform: HackTheBox
tags:
  - htb
  - lab
  - starting_point
---
Machine Name: Explosion
Machine IP: 10.129.1.13

Task 1: What does the 3-letter acronym RDP stand for? Remote Desktop Protocol

Task 2: What is a 3-letter acronym that refers to interaction with the host through a command line interface? CLI

Task 3: What about graphical user interface interactions? GUI

Task 4: What is the name of an old remote access tool that came without encryption by default? telnet

Task 5: What is the concept used to verify the identity of the remote host with SSH connections? public-key cryptography

Task 6: What is the name of the tool that we can use to initiate a desktop projection to our host using the terminal? xfreerdp

Task 7: What is the name of the service running on port 3389 TCP? ms-wbt-server

Task 8: What is the switch used to specify the target host's IP address when using xfreerdp? /v:

![[ explosionNmap.png]]
#### 10.129.1.13

| Port | State | Service | Version |
|------|-------|---------|---------|
| 135/tcp | open | *msrpc* | Microsoft Windows RPC  |
| 139/tcp | open | *netbios-ssn* | Microsoft Windows netbios-ssn  |
| 3389/tcp | open | *ms-wbt-server* | Microsoft Terminal Services  |
| 445/tcp | open | *microsoft-ds* |   |

![[explosionRDP.png]]

Root flag: 951fa96d7830c451b536be5a6be008a0