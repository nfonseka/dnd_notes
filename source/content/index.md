---
title: Home Page
---
## Session Notes
### [[Season 2]]
```dataview
TABLE Locations, file.outlinks as "Outlinks"
From "Session Notes/Season 2"
SORT file.name DESC
WHERE !contains(file.name, "One-Shot")
```

### Season 1
```dataview
TABLE file.outlinks as Outlinks
From "Session Notes/Season 1"
```
### One-Shots
```dataview
TABLE
WHERE contains(file.path, "One-Shot") OR contains(file.path, "Oneshot")
SORT file.ctime DESC
```

## Characters
```dataview
TABLE allies, Organisations, Class, Race, Enemies
FROM #Character 
WHERE !contains(file.path, "Archive")
SORT file.mtime DESC
```

## Locations
```dataview
TABLE file.inlinks, file.outlinks
FROM #Location 
SORT file.mtime DESC
```
## Organisations
```dataview
TABLE file.inlinks, file.outlinks
FROM #Organisation 
SORT file.mtime desc
```
## Items
```dataview
TABLE file.inlinks, file.outlinks 
FROM #Item 
SORT file.mtime desc
```
## Gods
```dataview
TABLE God_of, Allies, file.inlinks, file.outlinks
FROM #God 
```

