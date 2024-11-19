---
Resource: Cyber Security
THM Room: https://tryhackme.com/room/chocolatefactory
Platform: TryHackMe
tags:
  - thm
  - lab
---
# Chocolate Factory

## NMAP Scan

```bash
sudo nmap -sS -sV -O -p- 10.10.40.128 -oX nmap
```
#### 10.10.40.128

| Port | State | Service | Version |
|------|-------|---------|---------|
| 100/tcp | open | *newacct* |   |
| 101/tcp | open | *hostname* |   |
| 102/tcp | open | *iso-tsap* |   |
| 103/tcp | open | *gppitnp* |   |
| 104/tcp | open | *acr-nema* |   |
| 105/tcp | open | *csnet-ns* |   |
| 106/tcp | open | *pop3pw* |   |
| 107/tcp | open | *rtelnet* |   |
| 108/tcp | open | *snagas* |   |
| 109/tcp | open | *pop2* |   |
| 110/tcp | open | *pop3* |   |
| 111/tcp | open | *rpcbind* |   |
| 112/tcp | open | *mcidas* |   |
| 113/tcp | open | *ident* |   |
| 114/tcp | open | *audionews* |   |
| 115/tcp | open | *sftp* |   |
| 116/tcp | open | *ansanotify* |   |
| 117/tcp | open | *uucp-path* |   |
| 118/tcp | open | *sqlserv* |   |
| 119/tcp | open | *nntp* |   |
| 120/tcp | open | *cfdptkt* |   |
| 121/tcp | open | *erpc* |   |
| 122/tcp | open | *smakynet* |   |
| 123/tcp | open | *ntp* |   |
| 124/tcp | open | *ansatrader* |   |
| 125/tcp | open | *locus-map* |   |
| 21/tcp | open | *ftp* | vsftpd 3.0.3 |
| 22/tcp | open | *ssh* | OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 |
| 80/tcp | open | *http* | Apache httpd 2.4.29 |

## Website
![[chocolateFactorySite.png]]

#### Gobuster
```bash
sudo gobuster dir -u http://10.10.40.128 -w ~/Tools/SecLists/Discovery/Web-Content/directory-list-2.3-medium.txt
```