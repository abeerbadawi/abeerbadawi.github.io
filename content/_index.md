---
# Leave the homepage title empty to use the site title
#The name appearing at the navbar
title: "Abeer's Homepage" # Abeer Badawi
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: '0rem'

sections:
  - block: resume-biography-3
    content:
      username: admin
      text: ''
      headings:
        about: ''
        interests: ''
      show:
        education: false
    design:
      spacing:
        padding: [0, 0, 0, 0]
      css_class: hbx-bg-gradient
      avatar:
        size: medium
        shape: circle


  - block: markdown
    id : research
    design:
      spacing:
        padding: [0, 0, 0, 0]
    content:
      title: 
      text: |
        <style>
        section.home-section {
          padding-top: 0rem !important;
          padding-bottom: 0rem !important;
        }

        .research-navigation {
          display: flex;
          gap: 1.5rem;
          justify-content: center;
        }

        .research-btn {
          padding: 2rem;     
          background: #eef2ff;
          color: #3730a3;
          border: 2px solid rgba(191, 219, 254, 0.6);
          border-radius: 20px;
          text-decoration: none;
          font-weight: 700;            
          font-size: 1.25rem;          
          transition: all 0.25s ease;
        }

        .research-btn:hover {
          background: #3730a3;
          color: #eef2ff;
          border-color: #3730a3;
          transform: translateY(-2px);
        }
        </style>

        <div class="research-navigation">
          <a href="#publications" class="research-btn">Research Publications</a>
          <a href="#labs" class="research-btn">Research Labs</a>
        </div>

  - block: markdown
    id: featured
    content:
      title: Featured in the News
      text: |-
        <div class="featured-links">

          <a href="https://annual-report.vectorinstitute.ai/" target="_blank" class="featured-card">
            <div class="featured-source">Vector Institute</div>
            <div class="featured-title">Annual Report 2025–26</div>
            <div class="featured-description">
              Featured in Vector Institute's annual report highlighting research in safe and trustworthy AI for mental health and dementia care.
            </div>
          </a>

          <a href="https://www.yorku.ca/yfile/2026/07/15/york-prof-explores-ai-safeguards-for-youth-mental-health/" target="_blank" class="featured-card">
            <div class="featured-source">York University YFile</div>
            <div class="featured-title">York prof explores AI safeguards for youth mental health</div>
            <div class="featured-description">
              Feature on responsible AI, mental health, and safeguards for the use of LLMs in youth mental-health support.
            </div>
          </a>

          <a href="https://vectorinstitute.ai/when-ai-helps-too-much-towards-understanding-and-measuring-cognitive-atrophy-in-llm-behaviour/" target="_blank" class="featured-card">
            <div class="featured-source">Vector Institute</div>
            <div class="featured-title">When AI Helps Too Much</div>
            <div class="featured-description">
              Towards understanding and measuring Cognitive Atrophy in LLM behaviour.
            </div>
          </a>

        </div>

        <style>
          .featured-links {
            display: grid;
            grid-template-columns: repeat(3, minmax(0, 1fr));
            gap: 1.5rem;

            /* Make section wider than default markdown container */
            width: min(1200px, 92vw);
            position: relative;
            left: 50%;
            transform: translateX(-50%);

            margin-top: 1.5rem;
          }

          .featured-card {
            display: block;
            min-height: 230px;
            padding: 1.6rem;
            border: 1px solid #e2e8f0;
            border-radius: 16px;
            text-decoration: none !important;
            color: inherit;
            background: #ffffff;
            transition:
              transform 0.2s ease,
              box-shadow 0.2s ease,
              border-color 0.2s ease;
          }

          .featured-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.08);
            border-color: #cbd5e1;
          }

          .featured-source {
            font-size: 0.9rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.04em;
            margin-bottom: 0.7rem;
            opacity: 0.65;
          }

          .featured-title {
            font-size: 1.25rem;
            font-weight: 700;
            line-height: 1.35;
            margin-bottom: 0.8rem;
          }

          .featured-description {
            font-size: 1rem;
            line-height: 1.6;
            opacity: 0.82;
          }

          @media (max-width: 900px) {
            .featured-links {
              grid-template-columns: 1fr;
              width: min(700px, 92vw);
            }

            .featured-card {
              min-height: auto;
            }
          }
        </style>

    design:
      spacing:
        padding:
          - 1rem
          - 0
          - 2rem
          - 0

  - block: collection
    id: publications  
    content:
      title: Research Publications
      order: desc
      sort_by: 'weight'
      count: 6
      filters:
        folders:
          - publications
    design:
      spacing:
        padding: [1, 0, 0, 0]
      view: article-grid
      columns: 2
  
  - block: collection
    id: labs  # This matches the button link
    content:
      title: Research Labs
      order: asc
      sort_by: 'weight'
      filters:
        folders:
          - labs
    design:
      view: article-grid
      spacing:
        padding: [0, 0, 0, 0]
      columns: 2
  # - block: collection
  #   id: publication  # ← This enables /#publication linking
  #   content:
  #     title: Research Publications
  #     order: desc
  #     sort_by: 'weight'
  #     filters:
  #       folders:
  #         - publication
  #   design:
      # view: grid

      # - block: resume-awards
  # - block: resume-awards
  #   id: awards  # ← This enables /#awards linking
  #   content:
  #     title: Awards
  #     username: admin
  #   design:
  #     # Optional: Add spacing or styling
  #     spacing:
  #       padding: [2rem, 0, 2rem, 0]

  # - block: markdown  
  #   content:
  #     title: '📚 My Research'
  #     subtitle: ''
  #     text: |-
  #       Use this area to speak to your mission. I'm a research scientist in the Moonshot team at DeepMind. I blog about machine learning, deep learning, and moonshots.

  #       I apply a range of qualitative and quantitative methods to comprehensively investigate the role of science and technology in the economy.

  #       Please reach out to collaborate 😃
  #   design:
  #     columns: '1'
  # - block: collection
  #   id: papers
  #   content:
  #     title: Featured Publications
  #     filters:
  #       folders:
  #         - publications
  #       featured_only: true
  #   design:
  #     view: article-grid
  #     columns: 2
  # - block: collection
  #   content:
  #     title: Recent Publications
  #     text: ''
  #     filters:
  #       folders:
  #         - publications
  #       exclude_featured: false
  #   design:
  #     view: citation
  # - block: collection
  #   id: talks
  #   content:
  #     title: Recent & Upcoming Talks
  #     filters:
  #       folders:
  #         - events
  #   design:
  #     view: card
  # - block: collection
  #   id: news
  #   content:
  #     title: Recent News
  #     subtitle: ''
  #     text: ''
  #     # Page type to display. E.g. post, talk, publication...
  #     page_type: blog
  #     # Choose how many pages you would like to display (0 = all pages)
  #     count: 5
  #     # Filter on criteria
  #     filters:
  #       author: ''
  #       category: ''
  #       tag: ''
  #       exclude_featured: false
  #       exclude_future: false
  #       exclude_past: false
  #       publication_type: ''
  #     # Choose how many pages you would like to offset by
  #     offset: 0
  #     # Page order: descending (desc) or ascending (asc) date.
  #     order: desc
  #   design:
  #     # Choose a layout view
  #     view: card
  #     # Reduce spacing
  #     spacing:
  #       padding: [0, 0, 0, 0]
  # - block: cta-card
  #   demo: true # Only display this section in the Hugo Blox Builder demo site
  #   content:
  #     title: 👉 Build your own academic website like this
  #     text: |-
  #       This site is generated by Hugo Blox Builder - the FREE, Hugo-based open source website builder trusted by 250,000+ academics like you.

  #       <a class="github-button" href="https://github.com/HugoBlox/hugo-blox-builder" data-color-scheme="no-preference: light; light: light; dark: dark;" data-icon="octicon-star" data-size="large" data-show-count="true" aria-label="Star HugoBlox/hugo-blox-builder on GitHub">Star</a>

  #       Easily build anything with blocks - no-code required!

  #       From landing pages, second brains, and courses to academic resumés, conferences, and tech blogs.
  #     button:
  #       text: Get Started
  #       url: https://hugoblox.com/templates/
  #   design:
  #     card:
  #       # Card background color (CSS class)
  #       css_class: 'bg-primary-300 dark:bg-primary-700'
  #       css_style: ''
---
