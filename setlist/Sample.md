---
title: Sample
date: 14-May-2026 16:08
location: setlist
band:
tags:
  - song
  - sample
---
## [[Sample]]


```dataview
TABLE sample as Order, artist as Artist, youtube
FROM "songs"
WHERE contains(tags,"sample") and sample > 0
SORT sample
```
