---
Date: <%tp.date.now("YYYY-MM-DD")%>T<%tp.date.now("HH:mm")%>
tags:
    - daily
<% "- " + tp.date.now("MMMM", 0, tp.file.title, "DD-MM-YYYY") %>
<% "- " + tp.date.now("YYYY", 0, tp.file.title, "DD-MM-YYYY") %>
cssclasses:
    - daily
<% "- " + tp.date.now("dddd", 0, tp.file.title, "DD-MM-YYYY").toLowerCase() %>
---
# DAILY NOTE
## <% tp.date.now("dddd, MMMM Do, YYYY", 0, tp.file.title, "DD-MM-YYYY") %>
***
### Journal
#### Time
***
### Tasks
- [] Task 1
- [] Task 2
- [] Task 3