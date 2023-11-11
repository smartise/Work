---
tipe: manipulation
Done: true
---
# Description 
mesure of the oxygen production and consumption 

| site   | place     |
| ------ | --------- |
| perlas | saboga    |
| perlas | mogomogo  |
| perlas | cantadora |

# Manip used 
[[Respirometry]]
[[Field_work]]
# Result 
```dataview
TABLE rows.Tasks.text AS "Note"
FROM "journal"
FLATTEN file.tasks as Tasks
WHERE contains(Tasks.text, "[[Oxygen_analysis]]") AND contains(Tasks.text, "[[Respirometry]]") 
GROUP BY file.link

```
