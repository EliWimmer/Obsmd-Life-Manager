## Metadata
All YAML data autofills via templater on new day creation.
```
---
tags: daily-note
full-date: <% tp.file.title %>
week: <% tp.date.now("ww", 0, tp.file.title, "YYY-MM-DD") %>
month: <% tp.date.now("MM", 0, tp.file.title, "YYYY-MM-DD") %>-<% tp.date.now("MMM", 0, tp.file.title, "YYYY-MM-DD") %>
year: <% tp.date.now("YYYY", 0, tp.file.title, "YYYY-MM-DD") %>
banner: https://preview.redd.it/arqa352ph7x61.jpg?width=960&crop=smart&auto=webp&s=84f9245d607b029667d5bfc4abf36547fc6213de
---
```
⠀
## Header
The links to previous and next day and day name autofill via templater on new day creation. "New file location" in the core settings must be set to *Same folder*.
###### [[<% tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>|↶ YESTERDAY]] ⁝ [[<% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>|TOMORROW ↷]]
# ◌ Day

#### ✓  TASKS
Top task pulls from both tasks and project, filtered to show only due on or before today, and of highest priority.

Tasks shows all other incomplete tasks due on or before today.

Completed Today shows all tasks completed today.

######  ↑ TOP TASK
*tasks plugin code*
```
tasks
due <% tp.date.now("YYYY-MM-DD",0, tp.file.title, "YYYY-MM-DD") %>
not done
priority is high
hide task count
```
###### ○ TASKS
*tasks plugin code*
```
tasks
due <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %>
not done
priority is below high
short mode
hide task count
```
###### ✓ COMPLETED TODAY
*tasks plugin code*
```
tasks
done date is <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %>
hide task count
```
####  ↻ DAILIES
Dailies include a daily journal, which will appear in the weekly note, Habits, which will appear in the [[02 Action|Alignment]] dashboard and the weekly & monthly note.

Run log is included for example of other things you may want to put here and query from somewhere else.

###### ◧ MORNING JOURNAL
[Morning Gratitude :: ]
[Daily Intention :: ]

###### ↻ HABITS
[Wake Early :: ]
[Meditate :: ]
[Exercise :: ]
[Plan Next Day :: ]

###### ◷ RUN LOG
[Run Time :: 0]
[Run Distance :: 0]

###### ◨ EVENING JOURNAL
[Evening Gratitude ::]
[Do Better :: ]

####  OTHER NOTES
You may want to add other things to the daily note, just append them to the [[Daily Template]]