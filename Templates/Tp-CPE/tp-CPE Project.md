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
id: 2305.01.V
Title: <% tp.file.title %> 
tags: CPE/Projects
Destination: <% tp.system.suggester(["Bilibili","YouTube"], ["Bilibili","YouTube"]) %> 
Sponsor: 
status:
DateStarted: 
DateModified: 
DateCompleted:
DateDue:
EST:
ACT:
Published: false
aliases:
---
## Metadata
#### 1. Relationships
- Back:: [Homepage](Homepage)  
- Topic:: 
- Down:: [tp-CPE Script](tp-CPE%20Script.md), [tp-Editing Checklist](tp-Editing%20Checklist.md),[tp-Publishing Checklist](tp-Publishing%20Checklist.md)
- Inspired by:: 
- Jumps::  
- Linked:: [tp-CPE Project](tp-CPE%20Project.md)
#### 2. Assets 
- SourceURL::
- PublicURL:: 
#### 3. Results Review
- Views::
- Length::
- ToKeep::
- ToImprove::
- Act::
## Preproduction
#### 1. Script⭐
- [tp-CPE Script](tp-CPE%20Script.md)

#### 2. Filming Plan
- Filming Plan

## While-production
#### 1. Recording & Filming

## Post-production
#### 1. Editing & Publishing Checklist
- [tp-Editing Checklist](tp-Editing%20Checklist.md)
- [tp-Publishing Checklist](tp-Publishing%20Checklist.md)

#### 2. Thumbnail

#### 3. Description

#### 4. Pinned Comment

#### 5. Timestamp

#### 6. Blog Posting ⭐

