# Work notes

Everything is organized by **date**. Write in today's daily note; give real meetings their own note.
Todos can live anywhere: write `- [ ]` in any note and today's daily note picks it up.
Context comes from `[[Name]]` links and `#tags` in the line itself, so search finds it later.
Projects are optional: make one only when something gets big, then link to it.

Full guide: [[Docs/README|Docs]].

## Hotkeys
- **Cmd+Shift+D**: open today's daily note (also opens on startup)
- **Cmd+Shift+M**: new meeting (asks for a title, files it as `Meetings/YYYY-MM-DD Title`)
- **Cmd+Shift+J**: new project (asks for a name, files it in `Projects/`)
- **Cmd+Shift+F**: search, e.g. `budget path:Meetings`, `line:(Jane budget)`, `tag:#vendor`
- **Cmd+O**: jump to a note by name (e.g. `Tags` for what each tag means)

## Todos
- `- [ ] thing` is a todo
- `- [ ] thing 📅 2026-11-05` has a due date
- `- [ ] thing #waiting [[Jane Doe]]` means you're waiting on someone

## Tips
- Meeting attendees go in the `attendees` property as `[[Jane Doe]]`. No person note is needed; don't click the link, or it creates an empty note.
- To link a meeting to a project, put `"[[Project name]]"` in its `project` property.
- A project's todo list shows todos in the project note plus any todo that mentions it, e.g. `- [ ] send quote [[Vendor migration]]`.

## First-time setup (once per computer)
1. Open this folder as a vault and click **Trust author and enable plugins**.
2. Settings → Templater → turn on **Trigger Templater on new file creation** and accept the warning. (Templater keeps this switch per device, so it couldn't be preset.) Check that **Template matching mode** says *Folder templates*.
3. If today's daily note opened before step 2 and shows raw `<% %>` code, delete it and press Cmd+Shift+D.

## 2-minute smoke test
- Cmd+Shift+D → links and todo sections render (no raw `<% %>`).
- Cmd+Shift+M → type "Test" → note appears as `Meetings/<today> Test`.
- Add `- [ ] try it 📅 <today>` to the meeting → it shows under "Due / overdue" and "All open todos". Tick it → it moves to "Done today".
- Delete the test meeting when done.
