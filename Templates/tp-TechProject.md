---
Title: 
Type: 
tags: 
DateStarted: 
DateModified: 
DateDo: 
DateDone: 
status: 
mindmap-plugin: basic
---

<%-*  
let  newtitle  
if(tp.file.title.includes("未命名") || tp.file.title.toLowerCase().includes("untitled"))  
{ title=await tp.system.prompt("请输入要创建的文件名");  
  newtitle=title||tp.date.now("YYYYMMDDHHmmss")  
	await tp.file.rename(newtitle)}  
	else newtitle=tp.file.title  
-%>
# <% newtitle %> 
## Purpose
## Reference & Design
## Requirement Breakdown
## Tech Stack
### Front-End
### Back-End
## Resources
### Database
### 3-rd Party Service
### Deployment
