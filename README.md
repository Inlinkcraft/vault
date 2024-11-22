# Bienvenue dans mes notes qui regroupe tous mes connaissance !

## Ecole

```dataview
TABLE name as "Name", session as "Session"
WHERE type = "Course" and name != null
```

### Révision récente
```dataview
TABLE class as "Cours", name as "Nom", date as "Date"
WHERE type = "Revision" and name != null
SORT date DESC
```
