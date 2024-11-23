## Cyber Security

### Platforms

#### HackTheBox
```dataview
TABLE 
    module-name as "Module",
    file.mtime as "Modified"
FROM -#lab
WHERE Platform = "HackTheBox"
```
#### TryHackMe
```dataview
TABLE 
    thm-path as "Module",
    file.mtime as "Modified"
FROM -#lab
WHERE Platform = "TryHackMe"
```
#### OverTheWire
### Notes
```dataview
LIST WHERE Area = "Cyber Security"
```