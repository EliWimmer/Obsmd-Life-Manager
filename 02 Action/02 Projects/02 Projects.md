---
cssClasses: cards
banner_icon: 📐
---
# Projects Overview
```dataview
TABLE
	string("Target: " + target) AS "Target",
	string("Goal: ") + goal AS "Goal",
	string("Deadline: ") + deadline as "Deadline",
	string("Complete: ") + complete as "Complete"
FROM "02 Action/02 Projects"
WHERE file.name != "02 Projects"
```
`button-addbanner`