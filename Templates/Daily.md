<%* const d = moment(tp.file.title, "YYYY-MM-DD"); const prev = d.clone().subtract(1, "day").format("YYYY-MM-DD"); const next = d.clone().add(1, "day").format("YYYY-MM-DD"); -%>
[[Daily/<% prev %>|← <% prev %>]] · [[Daily/<% next %>|<% next %> →]]
# <% d.format("dddd, D MMMM YYYY") %>

## Notes
- <% tp.file.cursor() %>

## Today
```tasks
not done
scheduled before tomorrow
path does not include Templates/
sort by scheduled
```

## Due / overdue
```tasks
not done
due before tomorrow
path does not include Templates/
sort by due
```

## Waiting on others
```tasks
not done
tags include #waiting
path does not include Templates/
```

## Backlog
```tasks
not done
(no scheduled date) OR (scheduled after today)
path does not include Templates/
# skip empty checkboxes
description regex matches /\S/
group by folder
group by filename
```

## Done today
```tasks
done on {{query.file.filenameWithoutExtension}}
```
