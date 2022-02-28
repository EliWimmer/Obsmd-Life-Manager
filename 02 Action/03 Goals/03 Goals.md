---
cssClasses: cards
---
# Goals Overview
```dataview
TABLE
	string("Target: " + target) AS "Target",
	string("Goal: ") + goal AS "Goal",
	string("Deadline: ") + deadline as "Deadline",
	string("Complete: ") + complete as "Complete"
FROM "02 Action/03 Goals"
WHERE file.name != "03 Goals"
```