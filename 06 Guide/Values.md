---
cssClasses: cards
---
# Values Dashboard
The WHERE statement is required to prevent the folder note (dashboard) from appearing in the list.
*dataview code*
```
dataview
TABLE
	string("Why: " + why) AS "Why"
FROM "02 Action/04 Values"
WHERE file.name != "04 Values"
```