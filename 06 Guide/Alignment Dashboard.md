## Alignment Dashboard
The Alignment dashboard is a place to view your life from the top down. Very inspired by August Bradley's PPV system in Notion. 

This dashboard is a Folder Note.

## Metadata
*yaml code*
```
---
tag: dashboard
cssClasses: row-alt, table-small, table-max
banner: https://i.redd.it/ghbmrbnbhba81.png
banner_x: 0.5
banner_y: 0.5
---
```
⠀
#  ▲ Alignment

####  ◩ VALUES
Your core values. These are not completable items, but rather defining who you are and the themes you wish to define your life.

*dataview code*
```
dataview
TABLE
why AS "Why"
FROM "300 Action/330 Values"
```

#### ◎ GOALS
Goals are large defined targets to reach. Quantifiable, should have a specific completion criterea. 

*dataview code*
```
dataview
TABLE
	why AS "Why",
	value as "Value",
	deadline as "Deadline",
	complete as "Complete"
FROM "02 Action/03 Goals"
WHERE file.name != "03 Goals"
```

#### ◺ PROJECTS
Projects are groups of tasks and relevant information. Should have a quantifiable completion criterea, however these differ from goals in that they needn't be linked to value or goal, and are generally smaller in scale and more actionable.

*dataview code*
```
dataview
TABLE
	target AS "Target",
	goal AS "Goal",
	deadline as "Deadline",
	complete as "Complete"
FROM "02 Action/02 Projects"
WHERE file.name != "02 Projects"
SORT complete DESCENDING
```

#### ⌁ ◶Trackers
A habit tracker. Pulled from the daily notes. Limited to show only the last 30 days.

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
```

