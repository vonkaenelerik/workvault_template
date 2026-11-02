<%*
const date = tp.date.now("YYYY-MM-DD");
let title = (await tp.system.prompt("Meeting title (leave empty for \"Meeting\")")) ?? "";
title = title.replace(/[\\/:*?"<>|#^\[\]]/g, " ").replace(/\s+/g, " ").trim() || "Meeting";
const base = `Meetings/${date} ${title}`;
let path = base, n = 2;
while (await tp.file.exists(`${path}.md`)) path = `${base} ${n++}`;
await tp.file.move(path);
-%>
---
date: <% date %>
attendees: []
project:
tags: []
---
## Notes
- <% tp.file.cursor() %>

## Action items
- [ ] 
