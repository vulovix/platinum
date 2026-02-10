---
type: space
status: Active
description: ""
tags:
  - space
---

#### Space: <% tp.file.title %>

#### Notes

```dataview
TABLE topic, created_date
FROM "Spaces/<% tp.file.title %>/Notes"
SORT created_date DESC
```

```dataview
LIST
FROM "Spaces" OR "Journal"
WHERE contains(file.outlinks, [[<% tp.file.title %>]])
LIMIT 10
```
