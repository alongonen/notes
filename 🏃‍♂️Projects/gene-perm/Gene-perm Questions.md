
```dataviewjs
// You can update this to filter as you like - filtering for just your daily notes would be good


//pages from current folder
let pg = dv.current()
let parentFolder = pg.file.folder
let pages = dv.pages().where(p => p.file.folder.includes(parentFolder))

// This regex will find the contents of a specifically formatted callout
// const regex1 = />\s\[\!question\]\s(.+?)\s\#next/
const regex1 = />\s\[\!question\]\s(.+?)\s\#next/
const regex2 = />\s\[\!question\]\s(.+?)\s\#someday/

const rows1 = []
const rows2 = []
for (const page of pages) {
    const file = app.vault.getAbstractFileByPath(page.file.path)
    // Read the file contents
    const contents = await app.vault.read(file)
    // Extract the summary via regex
    for (const callout of contents.match(new RegExp(regex1, 'g')) || []) {
        const match = callout.match(new RegExp(regex1, 's')) 
        rows1.push([match[1], page.file.link]) 
    }  
    for (const callout of contents.match(new RegExp(regex2, 'g')) || []) {
        const match = callout.match(new RegExp(regex2, 's')) 
        rows2.push([match[1], page.file.link]) 
    } 
} 
dv.header(3, "Next Questions")
dv.table(['Term', 'Link'], rows1)
dv.header(3, "Someday Questions")
dv.table(['Term', 'Link'], rows2)
```
