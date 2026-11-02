# Setup and troubleshooting

## First run (once per computer)
1. Open the vault folder in Obsidian and click **Trust author and enable plugins**.
2. Settings → Templater → turn on **Trigger Templater on new file creation** and accept the warning. Check that **Template matching mode** says *Folder templates*.
   Templater stores this switch per device on purpose, so it can't come with the vault's settings.
3. If today's daily note was already created and shows raw `<% %>` code, fix it with Cmd+P → **Templater: Replace templates in the active file**, or delete it and press Cmd+Shift+D.

## Problems
| You see | Fix |
|---|---|
| Raw `<% ... %>` code in a new note | The Templater switch (step 2) is off. Turn it on, then Cmd+P → **Templater: Replace templates in the active file**. |
| A hotkey does nothing | Another app or command may use it. Settings → Hotkeys, search "Create Meeting" / "Create Project" / "daily note", and set a new key. Cmd+P → **Templater: Create Meeting** always works. |
| "JavaScript is now disabled in Tasks queries" | A query uses `filter by function`. Rewrite it without functions; the vault's own queries don't need them. |
| A Dataview or Tasks block shows as plain code | The plugin is off. Settings → Community plugins, enable Dataview / Tasks. |
| Empty notes appear at the vault root | Usually from clicking a link to a note that doesn't exist (e.g. an attendee). Delete them. |

## Moving to another computer
Copy or sync the whole folder, including the hidden `.obsidian/` folder. Then repeat **First run**.
