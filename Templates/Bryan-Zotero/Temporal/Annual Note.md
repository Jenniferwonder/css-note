<%* 
	// This template can get inserted into a new note that still has the name
	// "Untitled", the code will rename the file based on your answer to the prompt
	const year = await tp.system.prompt("4 digit year") 
	await tp.file.rename(year);
%>
<%* 
	tR = "---\n"
	tR += "tags: \n"
	tR += "publish: false\n"
	tR += "aliases:\n  - \n"
	tR += "---\n\n"
	tR += "# Annual Review:"
	tR += "\n\n"
	tR += "[["
	tR += year - 1
	tR += "-Y]] "
	tR += "<== <button class='date_button_today'>This Month</button> ==> "
	tR += "[["
	tR += parseInt(year) + 1
	tR += "-Y]]"
	tR += "\n\n"
	for (let i = 0; i < 12; i++) {
		tR += "![]("%20+%20tp.date.now("YYYY-[M]MM",%20"P+"%20+%20i%20+%20"M",%20year,%20"YYYY")%20+%20")\n"
	}
%>
