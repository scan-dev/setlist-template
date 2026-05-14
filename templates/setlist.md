<%*
  let title = tp.file.title
  if (title.startsWith("Untitled")) {
    title = await tp.system.prompt("Song Title");
    await tp.file.rename(title);
  }
    tR += "---"
%>
title:  <%* tR += title %>
date: <% tp.file.creation_date("DD-MMM-YYYY HH:mm") %>
location: <% tp.file.folder() %>
band:
tags: ["song", "sample"]

---
## [[<%* tR += title %>]]


```dataview
TABLE artist as Artist, youtube
FROM "songs"
WHERE contains(tags,"sample")
SORT title
```
