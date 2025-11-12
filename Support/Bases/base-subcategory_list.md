```base
formulas:
  Note: file.asLink(if(title, title, file.name))
properties:
  file.name:
    displayName: Note
  note.subcategory:
    displayName: Subcategory
views:
  - type: table
    name: Related Files
    filters:
      and:
        - file.hasLink(this.file)
    order:
      - subcategory
      - formula.Note
    sort:
      - property: subcategory
        direction: ASC
      - property: file.name
        direction: ASC

```
