Notes that have been linked to but not created and Notes that have not linked to anything else.

# Linked to but not created
```base
formulas:
  Untitled: file.links.filter(!value.asFile().isTruthy())
properties:
  file.name:
    displayName: Origin
  formula.Untitled:
    displayName: Uncreated files
views:
  - type: table
    name: Table
    filters:
      and:
        - file.links.filter(!value.asFile().isTruthy())
        - '!file.path.contains("Support")'
    order:
      - file.name
      - formula.Untitled

```

# Notes without links
```base
views:
  - type: table
    name: Table
    filters:
      and:
        - file.links.isEmpty()
        - '!file.path.contains("Files")'
        - '!file.path.contains("Support")'
        - '!file.path.contains("Daily")'

```
