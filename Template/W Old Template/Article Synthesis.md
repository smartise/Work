---

kanban-plugin: basic
date:
  "{ title }": null

---

{% persist "annotations" %}
{% set newAnnotations = annotations | filterby("date", "dateafter", lastImportDate) %}
{% if newAnnotations.length > 0 %}

# Imported: {{importDate | format("YYYY-MM-DD h:mm a")}}

{% for a in newAnnotations %}
 - [ ]  {{a.annotatedText}} {{a.comment}} {{a.tag}} {% endfor %} 

{% endif %} 
{% endpersist %}


# retained

%% kanban:settings
```
{"kanban-plugin":"basic"}
```
%%