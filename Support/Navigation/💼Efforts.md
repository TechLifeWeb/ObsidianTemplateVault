---
tags: [navigation]
---

> [!info]- About
> Things I'm actively working on  
> **Define your projects or they will define you.**  
> Projects fall into Areas. e.g., Publishing a book is a project, whereas Writing is an area  
> **Projects**: Write them in the past tense (e.g., Podcast episode published)  
> **Tasks**: Use verbs (e.g., Go to library)

# Active
```base
filters:
  and:
    - file.hasLink(this.file)
views:
  - type: table
    name: Tagged "active"
    filters:
      and:
        - file.tags.contains("active")
    order:
      - file.name

```
# Done
```base
filters:
  and:
    - file.hasLink(this.file)
views:
  - type: table
    name: Tagged "done"
    filters:
      and:
        - file.tags.contains("done")
    order:
      - file.name
```

### Hold
```base
filters:
  and:
    - file.hasLink(this.file)
views:
  - type: table
    name: Tagged "hold"
    filters:
      and:
        - file.tags.contains("hold")
    order:
      - file.name
```

### Canceled
```base
filters:
  and:
    - file.hasLink(this.file)
views:
  - type: table
    name: Tagged "canceled" or "cancelled"
    filters:
      or:
        - file.tags.contains("canceled")
        - file.tags.contains("cancelled")
    order:
      - file.name

```
