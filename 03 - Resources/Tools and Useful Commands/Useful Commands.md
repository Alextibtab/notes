---
tags:
  - resource
  - linux
  - cheatsheet
---
Convert NMAP output to Markdown table
```bash
~/Tools/nmap2md/./nmap2md.py nmap -c "Port,State,Service,Version" --hs 4 --rc "[port.number]/[port.protocol],[state],*[service.name]*,[service.product] [service.version]"
```