---
title: Publications
type: landing

sections:
  # TOP 6 FEATURED WITH IMAGES
  - block: collection
    content:
      title: Research Publications
      count: 6                     # Show only 6
      filters:
        folders:
          - publications
        featured_only: true        # Only show featured items
      order: desc
      sort_by: 'weight'
    design:
      view: article-grid           # Shows images
      columns: 2

  # OTHER PUBLICATIONS IN CITATION STYLE
  - block: collection
    content:
      title: Other Research Publications
      count: 0                     # Show all remaining
      offset: 6                    # Skip first 6
      filters:
        folders:
          - publications
        exclude_featured: true     # Don't show featured items
      order: desc
      sort_by: 'weight'
    design:
      view: citation               # Citation style, no images
---