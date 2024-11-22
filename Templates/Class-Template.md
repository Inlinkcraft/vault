---
name: 
type: Class
session: 
faculter: 
teacher: 
calendar: 
---
# 
---
...

## General information
---
**Temps:** 0-0-0
**Site de cours:** [Portail]()

## Revision
---
```dataview
TABLE name AS "Name", date AS "Date"
WHERE class = "AAA-XXXX"
WHERE type = "Revision"
SORT date DESC
```

## Travaux
---
```dataview
Table name AS "Name", du AS "Du date"
WHERE class = "AAA-XXXX"
WHERE type = "Travail"
SORT du ASC
```

## Exercise
---
```dataview
TABLE numero AS "Numero", date AS "Date"
WHERE class = "AAA-XXXX"
WHERE type = "Exercise"
SORT date DESC
```