---
<%-*  
let  newtitle  
if(tp.file.title.includes("未命名") || tp.file.title.toLowerCase().includes("untitled"))  
{ title=await tp.system.prompt("请输入要创建的文件名");  
  newtitle=title||tp.date.now("YYYYMMDDHHmmss")  
	await tp.file.rename(newtitle)}  
	else newtitle=tp.file.title  
-%>

Title: <% newtitle %>
Type: A-React
tags: 
DateStarted: 2023-12-08
DateModified: 2023-12-08
DateDo: 
DateDone: 
DateDue: 
DateReviewed: 
status: 
TimeNeed: 
Comment: 
Reviewed:
Demo:
---

# <% newtitle %> 