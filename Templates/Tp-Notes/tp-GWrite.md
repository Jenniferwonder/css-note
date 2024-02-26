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
tags: 
DateStarted: 
DateModified: 
---
## Metadata
### Relationships
- Topic:: 
- Inspired by:: 
- Related:: [HIVEs Framework](HIVEs%20Framework), [Tell the Story](Tell%20the%20Story), [Creative Writing](Creative%20Writing), [Trending Points](Trending%20Points)
- Linked:: [tp-GWrite](tp-GWrite.md)
# ⛰ Tell the Story
1. **Who** is the character?
2. **What** do they want?
3. **Why** can’t they get what they want?
4. What are the **stakes**? Ie: What will happen if they don’t get what they want?
5. Who or what **helps** them?
6. **How** do they get what they want?
7. How are they **transformed** by this experience?
## Story Structures
![](Pasted%20image%2020230504154224.png)