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
### Private Daily

![[private-notes/06 - Daily/Private Daily Note <% tp.date.now("DD-MM-YYYY") %>]]

### Journal

#### 09:00

#### 17:00

***
### Tasks
- [ ] Japanese Study
    - [ ] WaniKani
    - [ ] Bunpro
    - [ ] Duolingo