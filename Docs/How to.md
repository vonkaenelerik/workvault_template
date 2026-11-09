# How to

## Daily notes
**Open today's note:** Cmd+Shift+D. It also opens when Obsidian starts.
**Open another day:** click ← / → at the top of a daily note, or Cmd+O and type the date (`2026-10-28`).

## Meetings
**Create a meeting note**
1. Cmd+Shift+M
2. Type a title and press Enter. Empty gives "Meeting".
3. The note opens as `Meetings/<today> <title>` with the cursor under Notes.

**Add attendees**
1. Click the `attendees` value in the properties.
2. Type `[[Jane Doe]]` and press Enter. Repeat for more people.

**Link a meeting to a project:** click the `project` value and type `[[Project name]]`.

**Find a meeting:** Cmd+O and type part of the title or the date. Or search `path:Meetings budget`.

## Todos
**Add a todo:** in any note, type `- [ ] ` followed by the text.

| Type | Result |
|---|---|
| `- [ ] send slides` | todo |
| `- [ ] send slides 📅 2026-11-05` | todo due Nov 5 |
| `- [ ] contract back #waiting [[Jane Doe]]` | shows under "Waiting on others" |
| `- [ ] send quote [[Vendor migration]]` | also shows on the project note |

**Add a due date with a date picker:** put the cursor on the todo, Cmd+P → **Tasks: Create or edit task**, pick a due date, save.
**Complete a todo:** click its checkbox (in the note or in any list), or put the cursor on it and press Cmd+L. A `✅ date` is added.
**See all open todos:** today's daily note, section "All open todos".
**Jump to where a todo lives:** in any todo list, click the note name shown after the todo.

## Projects
**Create a project**
1. Cmd+Shift+J
2. Type the name and press Enter.
3. Fill in `description` in the properties.

**Connect things to a project**
| To get | Do |
|---|---|
| A meeting under "Linked notes & meetings" | set the meeting's `project` property to `[[Project name]]` |
| A daily-note line under "Linked notes & meetings" | write `[[Project name]]` in the line |
| A todo under "Open todos" | write `[[Project name]]` on the todo line, or write the todo in the project note |

**Close a project:** change `status` to `done`.

## Search
**Search everything:** Cmd+Shift+F and type.

| Type | Finds |
|---|---|
| `budget` | any line with "budget" |
| `budget path:Meetings` | only in meeting notes (`path:Daily`, `path:Projects` also work) |
| `line:(Jane budget)` | lines containing both words |
| `"Q3 forecast"` | exact phrase |
| `tag:#vendor` | notes with that tag |
| `task-todo:budget` | open todos containing "budget" |

Click a result to jump to that line.

## Tags
**Add a tag:** type `#` and a word in any line, or add it to a note's `tags` property. Typing `#` suggests existing tags.
**Nested tag:** `#vendor/acme`. Searching `tag:#vendor` also finds it.
**See all tags:** Cmd+P → **Tags: Show tags**. Click a tag to search for it.
**Describe a tag:** open the **Tags** note (Cmd+O → `Tags`) and add a line like `- #vendor: suppliers and contracts`. The table below it lists tags that have no description yet.
