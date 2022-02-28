---
tags: weekly-note
week: <% tp.date.now("ww", 0, tp.file.title, "gggg-[W]ww") %>
month: <% tp.date.now("YYYY - MM-MMMM", 0, tp.file.title, "YYYY--WW") %>
year: <% tp.date.now("YYYY", 0, tp.file.title, "gggg-[W]ww") %>
banner: https://preview.redd.it/arqa352ph7x61.jpg?width=960&crop=smart&auto=webp&s=84f9245d607b029667d5bfc4abf36547fc6213de
---
⠀
###### [[<% tp.date.now("gggg-[W]ww", -7, tp.file.title, "gggg-[W]ww") %>|↶ PREVIOUS WEEK]] ⁝ [[<% tp.date.now("gggg-[W]ww", 7, tp.file.title, "gggg-[W]ww") %>|FOLLOWING WEEK ↷]]
# ◌ <% tp.file.title %>
## Days
Shows all days within the current week.
*dataview code*
```
dataview
TABLE
week as "Week"
FROM "03 Periodic/01 Daily"
WHERE week = "<% tp.file.title %>"
```