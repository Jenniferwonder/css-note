<%-*  let filetype = await tp.system.suggester(["Resource","Project","Tracking","Temp"], ["Resource","Project","Tracking","Temp"], false, "Which template do you want to use?") -%>
<%-* if (filetype === "Resource") {  -%>
<%-tp.file.include("[tp-资源分类模板](tp-资源分类模板.md)")-%>
<%-* } else if (filetype === "Project") {  -%>
<%-tp.file.include("[tp-Tasks](tp-Tasks.md)")-%>
<%-* } else if (filetype === "Tracking") {  -%>
<%-tp.file.include("[tp-人物模板](tp-人物模板.md)")-%>
<%-* } else if (filetype === "Temp") {  -%>
<%-tp.file.include("[tp-GNotes](tp-GNotes.md)")-%>
<%-* } else { -%>
<%-tp.file.include("[tp-GNotes](tp-GNotes.md)")-%>
<%-* } -%>