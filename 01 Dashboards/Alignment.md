---
tag: dashboard
cssClasses: row-alt, table-small, table-max
banner: https://i.redd.it/ghbmrbnbhba81.png
banner_x: 0.5
banner_y: 0.5
---
#  ▲ Alignment
####  ◩ VALUES
```dataview
TABLE
why AS "Why"
FROM "300 Action/330 Values"
```

#### ◎ GOALS
```dataview
TABLE
	why AS "Why",
	value as "Value",
	deadline as "Deadline",
	complete as "Complete"
FROM "300 Action/320 Goals"
```

#### ◺ PROJECTS
```dataview
TABLE
	target AS "Target",
	goal AS "Goal",
	deadline as "Deadline",
	complete as "Complete"
FROM "300 Action/310 Projects"
```
#### ⌁ ◶Trackers
```dataview
TABLE WITHOUT ID
	link(file.name) as "Day",
	wake-early AS "🌄",
	meditate AS "🧘",
	morning-hygiene AS "🪥",
	three-jobs AS "🔧",
	exercise AS "🏃‍♂️",
	evening-hygiene AS "🦷",
	plan-next-day AS "✏️",
	no-pmo as "🍆"
	FROM "100 Periodic/110 Daily" 
	SORT file.name DESC
```

