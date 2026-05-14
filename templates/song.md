<%*
  let title = tp.file.title
  if (title.startsWith("Untitled")) {
    title = await tp.system.prompt("Song Title");
    await tp.file.rename(title);
  }
    tR += "---"
%>
title:  <%* tR += title %>
artist:
writer:
date: <% tp.file.creation_date("DD-MMM-YYYY HH:mm") %>
location: <% tp.file.folder() %>
youtube: URL
tags: song

---
## [[<%* tR += title %>]]

>chords:
>bridge:

[intro]
[bridge]
[solo]
[bridge]
[outro]