---
<%-* 
let  newtitle
if(tp.file.title.includes("未命名") || tp.file.title.toLowerCase().includes("untitled")) 
{ title=await tp.system.prompt("请输入要创建的文件名");
  newtitle=title||tp.date.now("YYYYMMDDHHmmss")
	await tp.file.rename(newtitle)}
	else newtitle=tp.file.title
-%>

UID: <% tp.date.now("YYYYMMDDHHmmss") %> 
Title: <% tp.file.title %> 
Type: Note
tags: <% tp.system.suggester(["PKM", "English", "Codespace", "Content-Making","PMP","Life","TechSkills","People","Published","CPE","AI"], ["PKM", "English", "Codespace", "Content-Making","PMP","Life","TechSkills","People","Published","CPE","AI"]) %> 
DateStarted: 
DateModified: 
status:
---
## Metadata
- Topic:: 
- Up::
## Purpose
## Actions
## Scope
%% Error: Cannot create a waypoint in a note that's not the folder note. For more information, check the instructions [here](https://github.com/IdreesInc/Waypoint) %%
## Highlights

## Reference Links