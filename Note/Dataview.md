
# Work to be done
```dataview
	table without id file.link as "Next 2 weeks", choice((date < date(today)),"<span style='color:red;'>"+ (date - date(today))+"</span>", choice((date>date(today)),(date - date(today)),"Today")) as "Due Date"
	Where date > date(today)-dur(2 w) and date < date(today)+dur(2 w)
	where !done
	sort date asc
```
---
# Tasks to be done
```dataview
TASK
FROM #todo 
WHERE !completed
```
---

# question 
```dataview
TASK
FROM #qst
WHERE !completed
```








```dataview
	table without id file.link as "Long term", choice((date < date(today)),"<span style='color:red;'>"+ (date - date(today))+"</span>", choice((date>date(today)),(date - date(today)),"Today")) as "Due Date" 
	from #Project 
	Where date 
	where !done
	where !contains(file.name, "template")
	sort date asc
```





