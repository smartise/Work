---
title: "{{title}}"
Abstract_read: false
Read: false
Used: false
collections: {% for c in collections %}[[{{c.fullPath}}]]{% if not loop.last %}, {% endif %}{% endfor %}
---
## {{title}}
---
tipe: {{itemType}}
Creators: {% for c in creators %}[[{{c.firstName}} {{c.lastName}}]]{% if not loop.last %}, {% endif %}{% endfor %}
collections: {% for c in collections %}[[{{c.fullPath}}]]{% if not loop.last %}, {% endif %}{% endfor %}
Link to zotero:: {{pdfZoteroLink}}
Journal: {{publicationTitle}}
DOI: {{DOI}}
Tags: {% for t in tags %}#{{t.tag}}{% if not loop.last %}, {% endif %}{% endfor %}

---
```ad-note
title: Abstract
color:: 
{% if abstractNote %}
{{abstractNote}}
{% endif %}
```

---
### Highlight

{% persist "annotations" %}
{% set newAnnotations = annotations | filterby("date", "dateafter", lastImportDate) %}
{% if newAnnotations.length > 0 %}


### Imported: {{importDate | format("YYYY-MM-DD h:mm a")}}
{% for a in newAnnotations %}
```ad-note
title: [[{{citationKey}}]]
> {{a.annotatedText}}
> [Page{{a.page}}](zotero://open-pdf/library/items/{{a.attachment.itemKey}}?page={{a.page}}&a={{a.id}})
> {% if a.comment %}
> ```ad-note
> {{a.comment}}
> {% endif %}
> ```
> {% if a.hashTags %}
> ```ad-note
> {{a.hashTags}}
> {% endif %}
> ```
> {% if a.imageRelativePath %}
>  ![[{{a.imageRelativePath}}]]
>  {% endif %}
```
{% endfor %}
{% endif %}
{% endpersist %}

## Bibliography

{{bibliography}}