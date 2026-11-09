# How it's built

Reference for changing the setup. You don't need this for daily use.

## Folders
| Folder | Holds |
|---|---|
| `Daily/` | `YYYY-MM-DD.md`, one per day |
| `Meetings/` | `YYYY-MM-DD Title.md` |
| `Projects/` | one note per project (optional) |
| `Templates/` | Daily, Meeting, Project templates (Templater syntax) |
| `Docs/` | this documentation |
| root | `Home.md`, `Tags.md`; new notes made from links land here |

## Plugins (one job each)
| Plugin | Job |
|---|---|
| **Tasks** | every todo list (due, waiting, all open, done) |
| **Templater** | templates: prompts for titles, names and files notes, builds date links |
| **Dataview** | lists of notes: project's linked notes, the tag table in [[Tags]] |

The core **Templates** plugin is off so it doesn't overlap with Templater. Only add other plugins deliberately.

## Key settings
- **Daily notes** (core): folder `Daily`, format `YYYY-MM-DD`, template `Templates/Daily`. Settings → General → Default file to open = Daily note.
- **Templater**: templates folder `Templates`. Folder templates: `Daily` → Daily, `Meetings` → Meeting, `Projects` → Project. Create-only hotkey commands for Meeting and Project. "Trigger on new file creation" is a per-device switch (see [[Docs/Setup and troubleshooting|Setup]]).
- **Tasks**: no global filter (every checkbox counts), emoji format (`📅`, `✅`), done date added automatically. JavaScript in queries is off (the default).
- **Dataview**: inline queries on, JavaScript queries off.
- **Files**: new notes go to the vault root. Hotkeys are in `.obsidian/hotkeys.json`.

## Templates
- **Daily**: prev/next links come from the file's own name, so old notes stay correct. The query sections are plain Tasks blocks; edit them like text.
- **Meeting**: asks for a title, removes characters that aren't allowed in filenames, avoids name clashes, and moves the note to `Meetings/`.
- **Project**: asks for a name if the note is untitled, then moves it to `Projects/`.

Editing a template only affects notes created afterwards.

## Conventions used in queries
- Every Tasks query excludes `Templates/`.
- "Today" = not done and scheduled before tomorrow. "Backlog" = not done and no scheduled date or scheduled after today, so a todo is never in both.
- "Backlog" and project todos skip empty checkboxes (`description regex matches /\S/`).
- Project todos: `(path includes {{query.file.path}}) OR (description includes {{query.file.filenameWithoutExtension}})`.
