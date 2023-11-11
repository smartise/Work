{{title}}

| title        | value                    |
| ------------ | ------------------------ |
| Authors      | [[{{authors}}{{directors}}]] |
| type         | {{itemType}}             |
| tags         | {{tags}}                 |
| URl          | {{uri}}                  |
| citation key | {{citationKey}}          |
# Hightlight

{% for a in annotations %}
{% if a.annotatedText %}
```ad-note
title:[[{{citationKey}}]]
color::{{a.color}}
> {{a.annotatedText}}
> {% endif %}
> [Page{{a.page}}](zotero://open-pdf/library/items/{{a.attachement.itemKey}}?page={{a.page}}&a={{a.id}})
> ```ad-note
> {% if a.comment %}
> {{a.comment}}
> ```
{% endif %}
```
{% endfor %}

{% persist "annotations" %}
{% set newAnnotations = annotations | filterby("date", "dateafter", lastImportDate) %}
{% if newAnnotations.length > 0 %}

### Imported: {{importDate | format("YYYY-MM-DD h:mm a")}}

{% for a in newAnnotations %}
> {{a.annotatedText}}
{% endfor %}
{% endif %}
{% endpersist %}