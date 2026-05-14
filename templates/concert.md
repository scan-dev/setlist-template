<%*
  let title = tp.file.title
  if (title.startsWith("Untitled")) {
    title = tp.date.now("YYYY-MM-DD") + '-' + await tp.system.prompt("Title");
    await tp.file.rename(title);
  }
    tR += "---"
%>
title:  <%* tR += title %>
date: <% tp.file.creation_date("DD-MMM-YYYY HH:mm") %>
location: <% tp.file.folder() %>
type: concert
topic:
summary: "template"
tags: concert
---

# [[<%* tR +=title %>]]

## Organizer

- [[contacts/]]

## Agenda

## Log

## Actions
