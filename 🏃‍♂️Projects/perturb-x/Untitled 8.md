## Next Questions


## Questions for projects
```dataviewjs

function calloutRegex(pages, regex) { 
	for (const page of pages) {
	    const file = app.vault.getAbstractFileByPath(page.file.path)
	    // Read the file contents
	    const contents = await app.vault.read(file)
	    // Extract the summary via regex
	    for (const callout of contents.match(new RegExp(regex, 'g')) || []) {
	        const match = callout.match(new RegExp(regex, 's')) 
	        rows.push([match[1], page.file.link]) 
	    } 
	}
	dv.table(['Term', 'Link'], rows) 
exports.calloutRegex = calloutRegex;

var dataviewUtils = require(app.vault.adapter.basePath + "/Files/dataviewUtils.js");

// You can update this to filter as you like - filtering for just your daily notes would be good
let pg = dv.current()
let parentFolder = pg.file.folder
let pages = dv.pages().where(p => p.file.folder.includes(parentFolder))

// This regex will find the contents of a specifically formatted callout
const regex1 = />\s\[\!question\]\s+?(.+?)\s+\#next/
//const regex2 = />\s\[\!question\]\s+?(.+?)\s+\#next/
calloutRegex(pages, regex1)
//calloutRegex(pages, regex2)

```



---



```dataviewjs 
let pg = dv.current()
let parentFolder = pg.file.folder
let pages = dv.pages().where(p => p.file.folder.includes(parentFolder))
dv.list(pages.file.name)

```


