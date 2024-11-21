---
Area: Cyber Security
Lab Type: "HTB: Starting Point Labs"
Platform: HackTheBox
tags:
  - htb
  - lab
  - starting_point
---
Machine Name: Meow
Machine IP: 10.129.28.117

Task 1: What does the acronym VM stand for? Virtual machine

Task 2: What tool do we use to interact with the operating system in order to start our VPN connection? Terminal

Task 3: What service do we use to form our VPN connection? OpenVPN

Task 4: What is the abreviated name for a tunnel interface in the output of your VPN boot-up sequence output? TUN

Task 5: What tool do we use to test our connection to the target? ping

Task 6: What is the name of the tool we use to scan the target's ports? nmap

![[meowNmap.png]]

#### 10.129.28.117 - NMAP

| Port |  State |  Service |  Version |
|------|--------|----------|----------|
| 23/tcp | open | *telnet* | Linux telnetd  |

![[meowTelnet.png]]

Root flag: b40abdfe23665f766f9c61ecba8a4c19