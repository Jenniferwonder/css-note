---
tags:
publish: false
aliases: 
mood: <%tp.system.suggester(["🟪️","🟦️","🟩️","🟨️","🟧️","🟥️"],["🟪️","🟦️","🟩️","🟨️","🟧️","🟥️"], false, "Mood")%>
mien: <%tp.system.suggester(["❌️","✅️"],["❌️","✅️"], false, "Mien")%>
norsk: <%tp.system.suggester(["❌️","✅️"],["❌️","✅️"], false, "Norsk")%>
reading: <%tp.system.suggester(["❌️","✅️"],["❌️","✅️"], false, "Reading")%>
---

## On This Day...

```dataviewjs

let dates = {
  today: new Date(),
  activeFile: new Date(app.workspace.getActiveFile().name.substring(0, 10))
};

let dateToCompare = dates.today;

function pad(n, width, z) {
  z = z || "0";
  n = n + "";
  return n.length >= width ? n : new Array(width - n.length + 1).join(z) + n;
}

function formatDate(date) {
  let month = pad(date.getMonth() + 1, 2);
  let day = pad(date.getUTCDate(), 2);
  return `-${month}-${day}`;
}

let openFileDateFormatted = formatDate(dates.activeFile);

function formatDataviewDate(dateObject) {
  let month = pad(dateObject.file.day.month, 2);
  let day = pad(dateObject.file.day.day, 2);

  return `-${month}-${day}`;
}

function onThisDay(dailyNote) {
  return formatDataviewDate(dailyNote) == formatDate(dateToCompare);
}

let pages = dv.pages('"Journal/Daily"').where(onThisDay);
let columns = ["File"];

function render() {
  dates.activeFile = new Date(
    app.workspace.getActiveFile().name.substring(0, 10)
  );

  if (isNaN(dates.activeFile)) {
    dateToCompare = dates.today;
  } else {
    dateToCompare = dates.activeFile;
  }

  pages = dv.pages('"Journal/Daily"').where(onThisDay);

  dv.container.empty();

  //dv.header(2, "On this day");
  dv.list(pages.file.link);
}

render();

app.workspace.on("file-open", function cb() {
  render();
});

```

---

## Notes Created Today

```dataview
table created, updated as modified, tags, type, status
FROM ""
WHERE contains(created, "<% tp.date.now("YYYY-MM-DD") %>")
```

---

[<% tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>](<%%20tp.date.now("YYYY-MM-DD",%20-1,%20tp.file.title,%20"YYYY-MM-DD")%20%>) <== <button class="date_button_today">Today</button> ==> [<% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>](<%%20tp.date.now("YYYY-MM-DD",%201,%20tp.file.title,%20"YYYY-MM-DD")%20%>)

#### Hey Bryan, Whats On Your Mind? 

##### Goals

TBD

---

<%* if (tp.date.now("M-D") == "1-1") { %>
**Make Yearly Note**
<%* } _%>
<%* if (tp.date.now("D") == 1) { %>
**Make Monthly Note**
<%* } _%>
<%* if (tp.date.now("ddd") == "Sun") { %>
**Make Weekly Note**
<%* } _%>
<% tp.file.cursor(0) %>