---
tags: [navigation]
---
Note: Any notes tagged "favorites" will show up here

```dataview
TABLE WITHOUT ID link(file.path, fact) as "Favorites"
FROM "Notes"
WHERE contains(tags, "favorite")
```
