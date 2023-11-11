---
Used: false
tipe: article
collections: "{% for c in collections %}[[{{c.fullPath}}]]{% if not loop.last %}, {% endif %}{% endfor %}"
---
## {{title}}
---

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

{% for a in annotations %}
{% if a.annotatedText %}
---
*{{citationKey}}*
	{{a.annotatedText}} 
	
[Page{{a.page}}](zotero://open-pdf/library/items/{{a.attachment.itemKey}}?page={{a.page}}&a={{a.id}})
	{% if a.comment %}
	{{a.comment}}
	{% endif %}
	{% if a.hashTags %}
{{a.hashTags}}
	{% endif %}
	{% if a.imageRelativePath %}
	![[{{a.imageRelativePath}}]] 
	{% endif %}
	reference:
{% endif %}

{% endfor %}
---
## Bibliography

{{bibliography}}