# Tags

What each tag means. Add a line when you start using a new tag.

- #waiting: blocked on someone else; shows under "Waiting on others" in the daily note
- #project: marks notes in Projects/ (added by the Project template)

## Tags in use
Tags without a line above are undocumented.

```dataview
TABLE WITHOUT ID tag AS Tag, length(rows) AS Notes
WHERE !startswith(file.path, "Templates/") AND file.path != this.file.path
FLATTEN file.etags AS tag
GROUP BY tag
SORT tag ASC
```
