---
tags: 
publish: true
aliases: {{citekey}}
type: paper
status: 🟥️
created: 
updated: 
---

<%*
	let title = "{{title}}";
	let date = tp.date.now("YYYY-MM-DD");
	await tp.file.rename(`& ${date} ${title}`);
_%>
## Metadata:

- type: [&](&)
- author:: {{author}}
	- notable_authors:: 
- keywords:: {{tags}}
- specific_subject:: 
- general_subject:: 
- doi:: {{DOI}}
- zotero_url:: [{{localLibrary}}]({{localLibrary}})
- reviewed_date:: [<% tp.date.now("YYYY-MM-DD") %>](<%%20tp.date.now("YYYY-MM-DD")%20%>)
{{dateAdded}}
- collections:: {{collections}}
- pdf_attachments:: {{pdfAttachments}}
- abstract_note:: {{abstractNote}}
- related:: {{related}}

```dataview
table created, updated as modified, tags, type, related
from ""
where contains(related, "{{citekey}}")
```

## Citation

```latex

```

## Hypothesis:

- 

## Methodology:

- 

## Result(s):

- 

## Summary of key points:

- 

## Notes
