```dataview
TABLE file.title, status
FROM "📚Literature/Zotero"
WHERE regexmatch("@.*", file.name) = True
SORT status DESC
```
