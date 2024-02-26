---
<%-* 
let  newtitle
if(tp.file.title.includes("未命名") || tp.file.title.toLowerCase().includes("untitled")) 
{ title=await tp.system.prompt("请输入要创建的文件名");
  newtitle=title||tp.date.now("YYYYMMDDHHmmss")
	await tp.file.rename(newtitle)}
	else newtitle=tp.file.title
-%>
<%-*
var cleanTitle = tp.user.getTitleSnippet(newtitle) 
var title = `${cleanTitle}`;
await tp.file.rename(`${title}`);
let filetype = await tp.system.suggester(["Content-Making", "Tech-Fundamentals", "Front-End", "PKM", "PMP", "Design","English-Learning"], ["Content-Making", "Tech-Fundamentals", "Front-End", "PKM", "PMP", "Design","English-Learning"], false, "路径放到哪里？") 
if (filetype === "Projects") { 
myFilePath = "Resources/Content-Making/" +  `${title}`;
await tp.file.move(`${myFilePath}`);
} else if (filetype === "Tech-Fundamentals") { 
myFilePath = "Resources/Tech-Fundamentals/" +  `${title}`;
await tp.file.move(`${myFilePath}`);
} else if (filetype === "Front-End") { 
myFilePath = "Resources/Front-End Tech Stack/" +  `${title}`;
await tp.file.move(`${myFilePath}`);
} else if (filetype === "PKM") { 
myFilePath = "Resources/PKM/" +  `${title}`;
await tp.file.move(`${myFilePath}`);
} else if (filetype === "PMP") { 
myFilePath = "Resources/PMP/" +  `${title}`;
await tp.file.move(`${myFilePath}`);
} else if (filetype === "Design") { 
myFilePath = "Resources/Design/" +  `${title}`;
await tp.file.move(`${myFilePath}`);
} else if (filetype === "English-Learning") { 
myFilePath = "Resources/English-Learning/" +  `${title}`;
await tp.file.move(`${myFilePath}`);
} else { 
myFilePath = "Resources/ReadItLater/" +  `${title}`;
await tp.file.move(`${myFilePath}`);
}
-%>

uid: <% tp.date.now("YYYYMMDDHHmmss") %> 
Title: <% `${title}` %> 
tags: <% `${filetype}` %>
Topic: <% tp.system.suggester(["🗒️Resource", "🚀Project", "💪Tracking"], ["🗒️Resource", "🚀Project", "💪Tracking"]) %> 
DateStarted: <% tp.file.creation_date() %>
DateModified:  <%+ tp.file.last_modified_date("YYYY-MM-DD ddd") %>
status: <% tp.system.suggester(["⚪Captured", "🟡Organized", "🟠Distilled","🟢Published","🔵Archived"], ["⚪Captured", "🟡Organized", "🟠Distilled", "🟢Published", "🔵Archived"]) %>
---

## Purpose

## Problems

## Solutions

## Highlights

## Reflections

## Related Notes

## Reference
