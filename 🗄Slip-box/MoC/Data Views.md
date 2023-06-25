
## Questions for projects
```dataviewjs
// You can update this to filter as you like - filtering for just your daily notes would be good
const pages = dv.pages('"🏃‍♂️Projects"')

// This regex will find the contents of a specifically formatted callout
// const regex = 
const regex = />\s\[\!question\]\s(.+?)\s\#(.+?)((\n>\s.*?)*)\n/

const rows = []
for (const page of pages) {
const file = app.vault.getAbstractFileByPath(page.file.path)
// Read the file contents
const contents = await app.vault.read(file)
// Extract the summary via regex
for (const callout of contents.match(new RegExp(regex, 'sg')) || []) {
	const match = callout.match(new RegExp(regex, 's')) 
	rows.push([match[1], match[2], page.file.link]) 
	} 
} 
dv.table(['Term', 'Flag', 'Link'], rows)
```
## Questions for Lit Notes

```dataviewjs
// You can update this to filter as you like - filtering for just your daily notes would be good
const pages = dv.pages('"📚Literature"')

// This regex will find the contents of a specifically formatted callout
// const regex = 
const regex = />\s\[\!question\]\s(.+?)\s\#(.+?)((\n>\s.*?)*)\n/

const rows = []
for (const page of pages) {
    const file = app.vault.getAbstractFileByPath(page.file.path)
    // Read the file contents
    const contents = await app.vault.read(file)
    // Extract the summary via regex
    for (const callout of contents.match(new RegExp(regex, 'sg')) || []) {
        const match = callout.match(new RegExp(regex, 's')) 
        rows.push([match[1], match[2], page.file.link]) 
        } 
    } 
dv.table(['Term', 'Flag', 'Link'], rows)
```