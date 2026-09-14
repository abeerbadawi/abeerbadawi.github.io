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
    id: spotlight
    content:
      title: Research in the Spotlight
      text: |-
        <div class="spotlight-box">

          <div class="spotlight-item">
            <div class="spotlight-source">York University News</div>
            <a href="https://www.yorku.ca/yfile/2026/07/15/york-prof-explores-ai-safeguards-for-youth-mental-health/"
               target="_blank">
              York researchers explore AI safeguards for youth mental health
            </a>
          </div>

          <div class="spotlight-item">
            <div class="spotlight-source">Vector Institute Annual Report 2025–26</div>
            <a href="https://annual-report.vectorinstitute.ai/"
               target="_blank">
              Where AI possibilities come to life
            </a>
          </div>

          <div class="spotlight-item">
            <div class="spotlight-source">Vector Institute News</div>
            <a href="https://vectorinstitute.ai/when-ai-helps-too-much-towards-understanding-and-measuring-cognitive-atrophy-in-llm-behaviour/"
               target="_blank">
              When AI helps too much: Towards understanding and measuring Cognitive Atrophy in LLM behaviour
            </a>
          </div>

        </div>

        <style>
          .spotlight-box {
            display: grid;
            grid-template-columns: repeat(3, minmax(0, 1fr));

            width: 94vw !important;
            max-width: none !important;

            position: relative;
            left: 50%;
            transform: translateX(-50%);

            border: 1px solid #e5e7eb;
            border-radius: 16px;
            background: #ffffff;
            overflow: hidden;

            margin-top: 1rem;
            margin-bottom: 1rem;

            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.04);
          }

          .spotlight-item {
            padding: 1.7rem 2rem;
            min-height: 150px;

            display: flex;
            flex-direction: column;
            justify-content: center;
          }

          .spotlight-item:not(:last-child) {
            border-right: 1px solid #e5e7eb;
          }

          .spotlight-source {
            font-size: 0.82rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.04em;
            opacity: 0.6;
            margin-bottom: 0.7rem;
          }

          .spotlight-item a {
            font-size: 1.08rem;
            font-weight: 600;
            line-height: 1.5;
            color: inherit;
            text-decoration: none;
          }

          .spotlight-item a:hover {
            text-decoration: underline;
          }

          @media (max-width: 900px) {
            .spotlight-box {
              width: 92vw !important;
              grid-template-columns: 1fr;
            }

            .spotlight-item {
              min-height: auto;
            }

            .spotlight-item:not(:last-child) {
              border-right: none;
              border-bottom: 1px solid #e5e7eb;
            }
          }
        </style>

    design:
      spacing:
        padding: [0.5rem, 0, 1rem, 0]
        
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
