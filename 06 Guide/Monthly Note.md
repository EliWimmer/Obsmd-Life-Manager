---
tags: monthly-note
month: <% tp.date.now("MM", 0, tp.file.title, "YYYY--WW") %>-<% tp.date.now("MMM", 0, tp.file.title, "gggg-[W]ww") %>
year: <% tp.date.now("YYYY", 0, tp.file.title, "gggg-[W]ww") %>
banner: https://preview.redd.it/arqa352ph7x61.jpg?width=960&crop=smart&auto=webp&s=84f9245d607b029667d5bfc4abf36547fc6213de
---
⠀
###### [[<% tp.date.now("gggg-[W]ww", -7, tp.file.title, "gggg-[W]ww") %>|↶ PREVIOUS WEEK]] ⁝ [[<% tp.date.now("gggg-[W]ww", 7, tp.file.title, "gggg-[W]ww") %>|FOLLOWING WEEK ↷]]
# ◌ <% tp.file.title %>

## Weeks
Shows all weeks within the current month.
*dataview code*
```
dataview
TABLE
month as "Month"
FROM "03 Periodic/02 Weekly"
WHERE month = "<% tp.file.title %>"
```

## Days
Shows all days within the current month.
*dataview code*
```
dataview
TABLE
month as "Month"
FROM "03 Periodic/01 Daily"
WHERE month = "<% tp.file.title %>"
```