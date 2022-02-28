---
cssClasses: cards
---
# Goals Dashboard
```dataview
TABLE
	string("Why: " + why) AS "Why",
	string("Value: ") + value AS "Value",
	string("Deadline: ") + deadline as "Deadline",
	string("Complete: ") + complete as "Complete"
FROM "02 Action/03 Goals"
WHERE file.name != "03 Goals"
```