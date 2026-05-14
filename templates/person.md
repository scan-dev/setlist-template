---
email:
venue: festival/club
location:
date_last_spoken:
follow_up:
---

# [[<% tp.file.title  %>]]

<% await tp.file.move("contacts/" + tp.file.title) %>

## Meetings

```dataview
TABLE summary as "Summary", date_last_spoken as "Previous Meeting"
FROM [[<% tp.file.title %>]]
WHERE contains(type,"meeting") AND summary!= "templates"
SORT date desc
```
