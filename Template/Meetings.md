---
"attendant :": 
"date:": 
tipe: meeting
---
# subject 
# note
```dataviewjs 
dv.taskList(dv.pages('"REUNION"').file.tasks 
.where(t => !t.completed)) 
```
