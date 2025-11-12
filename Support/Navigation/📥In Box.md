This file shows any Notes that have been linked to but have not been created yet.

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

