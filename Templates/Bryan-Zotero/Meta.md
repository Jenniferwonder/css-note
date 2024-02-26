<%* if (tp.file.title.charAt(0) == "{") { %>
<%-tp.file.include("[Book](Book.md)")%>
<%* } else if (tp.file.title.charAt(0) == "@") { %>
<%-tp.file.include("[Person](Person.md)")%>
<%* } else if (tp.file.title.charAt(0) == "!") { %>
<%-tp.file.include("[Tweet](Tweet.md)")%>
<%* } else if (tp.file.title.charAt(0) == "%") { %>
<%-tp.file.include("[Podcast](Podcast.md)")%>
<%* } else if (tp.file.title.charAt(0) == "+") { %>
<%-tp.file.include("[Youtube](Youtube.md)")%>
<%* } else if (tp.file.title.charAt(0) == "(") { %>
<%-tp.file.include("[Article](Article.md)")%>
<%* } else if (tp.file.title.charAt(0) == "&") { %>
<%-tp.file.include("[Paper](Paper.md)")%>
<%* } else if (tp.file.title.charAt(0) == "=") { %>
<%-tp.file.include("[Thought](Thought.md)")%>
<%* } else { %>
<%-tp.file.include("[New](New.md)")%>
<%* } _%>