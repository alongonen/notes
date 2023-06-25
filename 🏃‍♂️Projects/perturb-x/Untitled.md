## Next Questions


## Questions for projects
```dataviewjs
// You can update this to filter as you like - filtering for just your daily notes would be good
//const pages = dv.pages('"🏃‍♂️Projects"')
let parentFolder = dv.current().file.folder 
const lsFolder = app.vault.getFiles() .filter(file => file.parent.path == parentFolder).map(file => dv.fileLink(file.path)) 


//const pages = dv.pages('"${dv.current().file.folder}"')
const pages = dv.pages(lsFolder)

// This regex will find the contents of a specifically formatted callout
const regex = />\s\[\!question\]\s(.+?)\s\#next/

const rows = []
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
```



`$= dv.current().file.mtime`

`$=dv.current().file.folder`

```dataviewjs 
let parentFolder = dv.current().file.folder 
const lsFolder = app.vault.getFiles() .filter(file => file.parent.path == parentFolder).map(file => dv.fileLink(file.path)) 
  
dv.list(lsFolder)
```

