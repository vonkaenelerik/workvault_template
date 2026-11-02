<%*
let name = tp.file.title;
if (name.startsWith("Untitled")) {
  name = (await tp.system.prompt("Project name")) ?? "";
}
name = name.replace(/[\\/:*?"<>|#^\[\]]/g, " ").replace(/\s+/g, " ").trim() || "New project";
const base = `Projects/${name}`;
let path = base, n = 2;
while (tp.file.path(true) !== `${path}.md` && await tp.file.exists(`${path}.md`)) path = `${base} ${n++}`;
await tp.file.move(path);
-%>
---
description: 
status: active
tags: [project]
---
## Linked notes & meetings
```dataview
LIST FROM [[]] AND -"Templates" SORT file.day DESC
```

## Open todos
```tasks
not done
path does not include Templates/
# skip empty checkboxes
description regex matches /\S/
(path includes {{query.file.path}}) OR (description includes {{query.file.filenameWithoutExtension}})
group by filename
```

## Log
- <% tp.date.now("YYYY-MM-DD") %> Started.
