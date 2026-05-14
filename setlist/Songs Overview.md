
```dataview
TABLE artist as Artist, tags, youtube as YT
FROM "songs"
WHERE contains(tags,"song")
SORT artist
```