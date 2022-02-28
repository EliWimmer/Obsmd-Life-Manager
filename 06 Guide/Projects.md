---
cssClasses: cards
---
# Projects Dashboard
The WHERE statement is required to prevent the folder note (dashboard) from appearing in the list.
*dataview code*
```
dataview
TABLE
	string("Target: " + target) AS "Target",
	string("Goal: ") + goal AS "Goal",
	string("Deadline: ") + deadline as "Deadline",
	string("Complete: ") + complete as "Complete"
FROM "02 Action/02 Projects"
WHERE file.name != "02 Projects"
```