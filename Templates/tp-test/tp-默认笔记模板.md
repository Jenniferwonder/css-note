---
<%-*
var cleanTitle = tp.user.getTitleSnippet(tp.file.title) 
var title = `${cleanTitle}`;
await tp.file.rename(`${title}`);
-%>
<%-*
let filetype = await tp.system.suggester(["GeekEnglish", "Tech-Fundamentals", "Front-End", "PKM"], ["GeekEnglish", "Tech-Fundamentals", "Front-End", "PKM"], false, "路径放到哪里？") 
if (filetype === "Projects") { 
myFilePath = "/00-GeekEnglish/" +  `${title}`;
await tp.file.move(`${myFilePath}`);
} else if (filetype === "Tech-Fundamentals") { 
myFilePath = "/04-Tech-Fundamentals/" +  `${title}`;
await tp.file.move(`${myFilePath}`);
} else if (filetype === "Front-End") { 
myFilePath = "/05-Front-End Tech Stack/" +  `${title}`;
await tp.file.move(`${myFilePath}`);
} else if (filetype === "PKM") { 
myFilePath = "/06-PKM/" +  `${title}`;
await tp.file.move(`${myFilePath}`);
} else { 
myFilePath = "01-Inbox" +  `${title}`;
await tp.file.move(`${myFilePath}`);
}
-%>

Title: <% `${title}` %> 
tags: <% `${filetype}` %>
topic: [[<% tp.system.prompt("这个笔记对应的主题MOC ", "比如：时间管理") %>]]
DateStarted: <% tp.file.creation_date() %>
DateModified:  <%+ tp.file.last_modified_date("YYYY-MM-DD dddd HH:mm:ss") %>
uid: <% tp.date.now("YYYYMMDDHHmmss") %> 
status: <% tp.system.suggester(["⚪Captured", "🟡Organized", "🟠Distilled","🟢Published","🔵Archived"], ["⚪Captured", "🟡Organized", "🟠Distilled", "🟢Published", "🔵Archived"]) %>
due:
cssclass: 
---

## Purpose

## Problems

## Solutions

## Highlights

## Reflections

## Related Notes

## Reference
