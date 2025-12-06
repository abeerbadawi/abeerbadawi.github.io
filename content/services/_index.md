---
title: "Services & Talks"
type: landing

sections:

  # Services Section
  - block: collection
    id: services
    content:
      title: Services
      filters:
        folders:
          - services
      order: desc
      sort_by: date
    design:
      view: article-grid
      columns: 2

  # Talks Section
  - block: collection2
    id: talks
    content:
      title: Talks 
      filters:
        folders:
          - talks
      order: asc
      sort_by: 'weight'
      count: 0 
    design:
      view: article-grid
      columns : 3
---