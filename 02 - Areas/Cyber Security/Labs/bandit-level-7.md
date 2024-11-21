---
Area: Cyber Security
OTW Game: bandit
Platform: OverTheWire
tags:
  - overthewire
  - lab
---
Level Goal: The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

Solution: using find command with added flags
command: find / -size 33c -group bandit6 -user bandit7 2> /dev/null -exec cat {} +
password: z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

![[Pasted image 20231006215532.png]]