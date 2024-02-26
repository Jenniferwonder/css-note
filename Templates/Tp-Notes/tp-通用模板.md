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
tags: <% tp.system.prompt("这个笔记相关标签", "PKM") %>
DateStarted: <% tp.date.now("YYYY-MM-DD") %>
DateModified:  
type: <% tp.system.suggester(["🗒️Resource", "🚀Project", "💪Tracking"], ["🗒️Resource", "🚀Project", "💪Tracking"]) %> 
status: <% tp.system.suggester(["⚪Capturing", "🟡Organizing", "🟠Distilling","🟢Published","🔵Archived"], ["⚪Capturing", "🟡Organizing", "🟠Distilling", "🟢Published", "🔵Archived"]) %>
due:
Source:
URL:
---

## Purpose

## Problems

## Solutions

## Highlights

## Reflections

## Reference

## Related Notes

```start-multi-column
ID: ID_sbs3
Number of Columns: 2
Largest Column: standard
Border: disabled
```

**Previous**

--- column-end ---

**Next**

=== end-multi-column
