---
cssClasses: cards
---
# Goals Dashboard
The WHERE statement is required to prevent the folder note (dashboard) from appearing in the list.
*dataview code*
```
dataview
TABLE
	string("Why: " + why) AS "Why",
	string("Value: ") + value AS "Value",
	string("Deadline: ") + deadline as "Deadline",
	string("Complete: ") + complete as "Complete"
FROM "02 Action/03 Goals"
WHERE file.name != "03 Goals"
```