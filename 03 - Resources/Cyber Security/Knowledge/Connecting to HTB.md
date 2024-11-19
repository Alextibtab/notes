---
Resource: Cyber Security
Module Name: "HTB: Getting Started"
Module Tier: 0
Platform: HTB
tags:
  - "#htb"
  - "#tier_0"
---
# Connecting Using a VPN
---
A virtual private network (VPN) allows a secure connection from a public network into a private (internal) network to access HTB hosts and resources. VPNs provide a degree of privacy and security by encrypting communications over the channel to prevent eavesdropping

# Connecting to HTB VPN
---
HTB and other services offering purposefully vulnerable VMs/Networks require users to connect to the target network via a VPN to access the private lab network. Hosts within HTB networks cannot connect directly out to the internet. When connected to HTB VPN, we should always consider the network to be "hostile". We should only connect from a virtual machine, disallow password authentication if SSH is enabled on our attacking VM, lockdown any web servers and not leave sensitive information on our attack VM.

![[connectVPN.png]]