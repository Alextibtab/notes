---
Resource: Cyber Security
Module Name: "HTB: Getting Started"
Module Tier: 0
Platform: HackTheBox
tags:
  - htb
  - tier_0
---
# Basic Tools
---
- `SSH`
- `NetCat`
- `Tmux`	
- `Vim`

# Using SSH
---
Secure Shell (SSH) is a network protocol that runs on port `22` by def[[Common Tools]]ault and provides users such as system administrators a secure way to access a computer remotely. SSH can be configured with password authentication or passwordless using public-key authentication using an SSH public/private key pair. SSH can be used to remotely access systems on the same network , over the internet, facilitate connections to resources in other networks using port forwarding/proxying, and upload/download files to and from the remote systems.

SSH uses a client-server model, connecting a user running an SSH client application such as `OpenSSH` to an SSH server. While attacking a box or during a real world assessment , SSH is often used once obtaining credentials or an SSH private key to obtain an SSH connection to the machine.

Example Usage:
`ssh USERNAME@IPADDRESS`

# Using Netcat
---
Netcat, `ncat`, or `nc`, is an excellent network utility for interacting with TCP/UDP ports. It can be used for many thing during a pentest. Its primary usage is for connecting to shells. 

# Using Tmux
---
Terminal multiplexers like tmux or screen, are great utilities for expanding a standard Linux terminal's features, like having multiple windows within one terminal and jumping between them.

Install Command:
`sudo apt install tmux -y`

Tmux Cheat Sheet: https://tmuxcheatsheet.com/
Tmux ippsec Video: https://www.youtube.com/watch?v=Lqehvpe_djs

# Using Vim
---
Usage: 
`vim/vi file`

By default you can't enter any text are in read-only `normal mode` which allows for navigation. To edit the file hit `i` to enter `insert mode` 

Once finished with editing you can exit `insert mode` with the `esc` key.

Normal mode commands:

| Command | Description    |
| ------- | -------------- |
| `x`     | Cut character  |
| `dw`    | Cut word       |
| `dd`    | Cut full line  |
| `yw`    | Copy word      |
| `yy`    | Copy full line |
| `p`     | Paste          | 

When in normal mode you can type `:` followed by characters to perform certain commands

| Command | Description          |     |
| ------- | -------------------- | --- |
| `:1`    | Go to line number 1  |     |
| `:w`    | Write the file, save |     |
| `:q`    | Quit                 |     |
| `:q!`   | Quit without saving  |     |
| `:wq`   | Write and quit       |     |
