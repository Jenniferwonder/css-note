```dataview
TABLE title, DateStarted, status
FROM "学习记录"
WHERE file.cday >= date(2022-11-28) AND file.cday <= date(2022-12-11)
SORT file.cday ASC
```
