---
Date: <%tp.date.now("YYYY-MM-DD")%>T<%tp.date.now("HH:mm")%>
tags:
    - daily
    <% "- " + tp.date.now("MMMM", 0, tp.file.title, "DD-MM-YYYY") %>
    <% "- Y" + tp.date.now("YYYY", 0, tp.file.title, "DD-MM-YYYY") %>
cssclasses:
    - daily
    <% "- " + tp.date.now("dddd", 0, tp.file.title, "DD-MM-YYYY").toLowerCase() %>
---
# DAILY NOTE
## <% tp.date.now("dddd, MMMM Do, YYYY", 0, tp.file.title, "DD-MM-YYYY") %>
***
### Journal

#### 09:00

#### 10:00

#### 11:00

#### 12:00

#### 13:00

#### 14:00

#### 15:00

#### 16:00

#### 17:00

***
### Tasks
- [ ] Japanese Study
    - [ ] WaniKani
    - [ ] Bunpro
    - [ ] Duolingo
- [ ] Task 2
- [ ] Task 3

```rust
println!("Hello, World!");
```

![[Pasted image 20241214003145.png]]