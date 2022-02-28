[[Quick Start|← Back to Quick Start]]
---
The folders [[01 Daily]], [[02 Weekly]], and [[03 Monthly]] folders are all folder notes containing an overview.

# Periodic Overviews
## [[01 Daily|Daily Overview]]
Shows Last 30 Daily Notes with habits. Any habits need to be added to the dataview code on the [[01 Daily]] and [[02 Action]] pages.
*dataview code*
```
dataview
TABLE WITHOUT ID
	link(file.name) as "Day",
	wake-early AS "🌄",
	meditate AS "🧘",
	exercise AS "🏃‍♂️",
	plan-next-day AS "✏️"
	FROM "03 Periodic/01 Daily" 
	SORT file.name DESC
	LIMIT 30
	WHERE file.name != "01 Daily"
```
## [[02 Weekly|Weekly]]
Currently this is just a simple list of the last 8 weeks. It has been intentionally left blank to allow for your own weekly review process.
*dataview code*
```
dataview
LIST
FROM "03 Periodic/02 Weekly"
SORT file.name DESCENDING
WHERE file.name != "02 Weekly"
LIMIT 8
```
## [[03 Monthly|Monthly]]
Currently this is just a simple list of the last 12 months. It has been intentionally left blank to allow for your own monthly review process.
```
dataview
LIST
FROM "03 Periodic/03 Monthly"
SORT file.name DESCENDING
WHERE file.name != "03 Monthly"
LIMIT 12
```