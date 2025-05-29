---
sticker: lucide//person-standing
---
```dataview
TABLE allies, Organisations, Enemies
FROM #Character 
WHERE !contains(file.path, "Archive")
SORT file.mtime DESC
```
