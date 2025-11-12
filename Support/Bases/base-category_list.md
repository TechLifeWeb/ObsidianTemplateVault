```base
formulas:
  Note: file.asLink(if(title, title, file.name))
properties:
  file.name:
    displayName: Note
  note.category:
    displayName: Category
views:
  - type: table
    name: Related Files
    filters:
      and:
        - file.hasLink(this.file)
    order:
      - category
      - file.name
    sort:
      - property: category
        direction: ASC
      - property: file.name
        direction: ASC

```
