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
id: 2305.01.V.SRT
Title: <% tp.file.title %> 
tags: CPE/Script
Destination: <% tp.system.suggester(["Bilibili","YouTube"], ["Bilibili","YouTube"]) %> 
status:
DateStarted: 
DateModified: 
DateCompleted:
DateDue: 
EST:
ACT:
---
## Metadata
### Relationships
- Back:: [Homepage](Homepage)  
- Topic::
- Up:: [tp-CPE Project](tp-CPE%20Project.md) 
- Related:: 
- Jumps::  
- Linked:: [tp-CPE Script](tp-CPE%20Script.md)

## 💡Title Ideas
```ad-tip
😃 Suggest at least 10 and tick/star your favorite one. Keep all titles less than 55 characters. Market research + thinking outside the box will help 
```

|No.|🧡|Name|Length|Notes|SourceURL |
|:--|:--|:--|:--|:--|:--|
|1|  |有趣的笔记概念——生产力神器 |  |  |  |
|2|  |  |  |  |   |
|3|  |  |  |  |   |
|4|  |  |  |  |   |
|5|  |  |  |  |   |
|6|  |  |  |  |   |
|7|  |  |  |  |   |
|8|  |  |  |  |   |
|9|  |  |  |  |   |
|10|  |  |  |  |   |

## 🎣 1. Hook
```ad-tip
title: Guidance
💡 The first 15 seconds should immediately reinforce the value proposition that was promised in the title + thumbnail. We no longer want an extended 'welcome back to the channel my name is ali i'm a junior doctor working in cambridge blah blah'. We need a snappy hook that tells people "this video will deliver on what I was promised". This is arguably the most important part of the video.
```

- "Hey friends welcome back to the channel. Today we're talking about abc" is the longest that the intro should be. In an ideal world, we'd design a hook that doesn't even have a 'welcome back to the channel', it just launches straight into delivering value.

## 💭 2. Intro

Hey friends, welcome back to the channel. If you're new here my name's Ali, I'm a doctor based in the UK, and on this channel we explore the strategies and tools that help us live healthier, happier, more productive lives.

Today,

## 💰 3. Value


## 🌤 4. End Screen Sales Pitch
```ad-tip
title: Guidance
💡The objective of the ending is to keep them watching by pointing them to a custom playlist of 3-4 other videos that they might be interested in. Eg: "if you liked this video you'll love this custom playlist i've made for you that has my most popular videos about how to study that have apparently changed people's lives. Thanks for watching, and see you later".
```




