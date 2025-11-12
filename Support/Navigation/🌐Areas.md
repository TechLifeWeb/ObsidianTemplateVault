---
tags:
  - navigation
aliases:
  - Projects
---

> [!info]- About
> Areas of Responsibility are the **roles you take on in life** and the **hats you wear** (Spouse, Mother/Father, Team Leader, Soccer Coach), the ongoing standards where the buck stops with you (Product Development, Company Newsletter, Legal), and **things that take a certain amount of constant attention** (Exercise, Finances, Apartment, Pets).  
> **Guideline**: put **_personally_ relevant** information here

```base
filters:
  and:
    - file.hasLink(this.file)
views:
  - type: table
    name: Areas
    order:
      - file.name

```