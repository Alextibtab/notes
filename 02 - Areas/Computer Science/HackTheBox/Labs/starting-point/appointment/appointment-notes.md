---
lab_type: [[Starting Point Labs]]
platform: HTB
---
Machine Name: Appointment
Machine IP: 10.129.29.102

Task 1: What does the acronym SQL stand for? structured query language

Task 2: What is one of the most common type of SQL vulnerabilities? sql injection

Task 3: What does PII stand for? personally identifiable information

Task 4: What does the OWASP Top 10 list name the classification for this vulnerability? A03:2021-Injection

Task 5: What service and version are running on port 80 of the target? Apache httpd 2.4.38 ((Debian))
 
Task 6: What is the standard port used for the HTTPS protocol? 443

Task 7: What is one luck-based method of exploiting login pages? brute-forcing

Task 8: What is a folder called in web-application terminology? directory

Task 9: What response code is given for "Not Found" errors? 404

Task 10: What switch do we use with Gobuster to specify we're looking to discover directories, and not subdomains? dir

Task 11: What symbol do we use to comment out parts of the code? #

![[appointmentNmap.png]]

#### 10.129.29.102

| Port | State | Service | Version |
|------|-------|---------|---------|
| 80/tcp | open | *http* | Apache httpd 2.4.38 |

![[appointmentGobuster.png]]

![[appointmentFlag.png]]

Flag: e3d0796d002a446c0e622226f42e9672

up: [[Starting Point Labs]]
tags: #HTB #Starting_Point #Labs 