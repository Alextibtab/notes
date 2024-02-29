Machine name: Forest
Machine IP: 10.129.95.210

## NMAP
![[forestNmap.png]]

#### 10.129.95.210

| Port | State | Service | Version |
|------|-------|---------|---------|
| 135/tcp | open | *msrpc* | Microsoft Windows RPC  |
| 139/tcp | open | *netbios-ssn* | Microsoft Windows netbios-ssn  |
| 3268/tcp | open | *ldap* | Microsoft Windows Active Directory LDAP  |
| 3269/tcp | open | *tcpwrapped* |   |
| 389/tcp | open | *ldap* | Microsoft Windows Active Directory LDAP  |
| 445/tcp | open | *microsoft-ds* | Microsoft Windows Server 2008 R2 - 2012 microsoft-ds  |
| 464/tcp | open | *kpasswd5* |   |
| 53/tcp | open | *domain* | Simple DNS Plus  |
| 593/tcp | open | *ncacn_http* | Microsoft Windows RPC over HTTP 1.0 |
| 636/tcp | open | *tcpwrapped* |   |
| 88/tcp | open | *kerberos-sec* | Microsoft Windows Kerberos  |