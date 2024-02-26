---
read_book: 
good_reads_review: 
roth_ira: 
youtube_collab: 
ulfar_event: 
social_outing: 
---

# Monthly Review:
%% This template Requires the Templater plugin %%
[<% tp.date.now("YYYY-[M]MM", "P-1M") %>](<%%20tp.date.now("YYYY-[M]MM",%20"P-1M")%20%>) <== <button class="date_button_today">This Month</button> ==> [<% tp.date.now("YYYY-[M]MM", "P+1M") %>](<%%20tp.date.now("YYYY-[M]MM",%20"P+1M")%20%>)

---

- [<% tp.date.weekday("YYYY-[W]ww", 0, tp.file.title, "YYYY-[M]MM") %>](<%%20tp.date.weekday("YYYY-[W]ww",%200,%20tp.file.title,%20"YYYY-[M]MM")%20%>)
- [<% tp.date.weekday("YYYY-[W]ww", 7, tp.file.title, "YYYY-[M]MM") %>](<%%20tp.date.weekday("YYYY-[W]ww",%207,%20tp.file.title,%20"YYYY-[M]MM")%20%>)
- [<% tp.date.weekday("YYYY-[W]ww", 14, tp.file.title, "YYYY-[M]MM") %>](<%%20tp.date.weekday("YYYY-[W]ww",%2014,%20tp.file.title,%20"YYYY-[M]MM")%20%>)
- [<% tp.date.weekday("YYYY-[W]ww", 21, tp.file.title, "YYYY-[M]MM") %>](<%%20tp.date.weekday("YYYY-[W]ww",%2021,%20tp.file.title,%20"YYYY-[M]MM")%20%>)
- [<% tp.date.weekday("YYYY-[W]ww", 28, tp.file.title, "YYYY-[M]MM") %>](<%%20tp.date.weekday("YYYY-[W]ww",%2028,%20tp.file.title,%20"YYYY-[M]MM")%20%>)
