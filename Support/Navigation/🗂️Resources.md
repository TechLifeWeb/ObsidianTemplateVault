---
tags:
  - navigation
---

>[!info]- About
>Things I interested in



```base
filters:
  and:
    - file.hasLink(this.file)
views:
  - type: table
    name: Resources
    order:
      - file.name

```
