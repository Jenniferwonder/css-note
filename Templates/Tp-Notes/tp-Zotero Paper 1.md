---
Title: {{title}}
Type: Note
tags: [{{allTags}}] 
Pages: {{pages}}
DOI: {{doi}}
Citekey: {{citekey}}
DateStarted: 
DateModified: 
aliases: {{citekey}}
---
# {{title}}
## Metadata
- Authors:: {{authors}} {{directors}}
- ZoteroLink:: {{pdfZoteroLink}}
{{extra}}
- Related:: [O-JS {{title}}](O-JS%20{{title}})
- Source:: {{url}}
- Abstract:: {{abstractNote}}
{% for relation in relations -%}
{%- if relation.citekey -%}
- Cited:: {{relation.citekey}}
{% endif -%}
{%- endfor %}
## Notes
```dataview
TABLE DateCreated, DateModified, tags, Cited
FROM ""
WHERE contains(Cited, "{{citekey}}")
```
## Summary

## Highlights
![](tp-Zotero%20Paper%20Notes.png)
{% for annotation in annotations -%}
	{% if annotation.annotatedText  -%}
- <mark class="hltr-{{annotation.colorCategory|lower}} "> {{annotation.annotatedText}}</mark> [Page {{annotation.page}} ]( zotero://open-pdf/library/items/{{annotation.attachment.itemKey}}?page={{annotation.page}}&annotation={{annotation.id}})
	{%- endif %}
	{%- if annotation.imageRelativePath -%}
	![]({{annotation.imageRelativePath}})
	{%- endif %}
{% if annotation. comment %}
- {{annotation.comment}}
{% endif %}
{% endfor -%}