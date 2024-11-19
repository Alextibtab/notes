---
Resource: Cyber Security
Lab Type: "HTB: Starting Point Labs"
Platform: HackTheBox
tags:
  - htb
  - lab
  - starting_point
---
Machine Name: Preignition
Machine IP: 10.129.29.95

Task 1: What is considered to be one of the most essential skills to possess as a Penetration Tester? dir busting

Task 2: What switch do we use for nmap's scan to specify that we want to perform version detection? -sV

Task 3: What service type is identified as running on port 80/tcp in our nmap scan? http

Task 4: What service name and version of service is running on port 80/tcp in our nmap scan? nginx 1.14.2

Task 5: What is a popular directory busting tool we can use to explore hidden web directories and resources? gobuster

Task 6: What switch do we use to specify to gobuster we want to perform dir busting specifically? dir

Task 7: What page is found during our dir busting activities? admin.php

Task 8: What is the status code reported by gobuster upon finding a successful page? 200

![[preignitionNmap.png]]

#### 10.129.29.95

| Port | State | Service | Version |
|------|-------|---------|---------|
| 80/tcp | open | *http* | nginx 1.14.2 |

![[preignitionGobuster.png]]

Flag: 6483bee07c1c1d57f14e5b0717503c73