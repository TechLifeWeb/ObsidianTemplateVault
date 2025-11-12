- 〽️ Stats
	- File Count: `$=dv.pages().length`

# Recent file updates

```base
views:
  - type: table
    name: Recent file updates
    order:
      - file.name
    sort:
      - property: file.mtime
        direction: DESC
      - property: file.name
        direction: ASC
    limit: 10

```
