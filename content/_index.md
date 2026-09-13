---
# Leave the homepage title empty to use the site title
title: "Abeer's Homepage"
date: 2022-10-24
type: landing

design:
  spacing: '0rem'

sections:

  # =========================================================
  # PROFILE / BIO / INTERESTS
  # =========================================================
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


  # =========================================================
  # RESEARCH LABS
  # =========================================================
  - block: collection
    id: labs
    content:
      title: Research Labs
      sort_by: weight
      order: asc
      filters:
        folders:
          - labs
    design:
      view: article-grid
      columns: 2
      spacing:
        padding: [1rem, 0, 1rem, 0]


  # =========================================================
  # RESEARCH IN THE SPOTLIGHT
  # =========================================================
  - block: markdown
    id: featured
    content:
      title: Research in the Spotlight
      text: |-
        <div class="featured-links">

          <a href="https://www.yorku.ca/yfile/2026/07/15/york-prof-explores-ai-safeguards-for-youth-mental-health/"
             target="_blank"
             class="featured-card">
            <div class="featured-source">
              Featured in York University News
            </div>
            <div class="featured-title">
              York researchers explore AI safeguards for youth mental health
            </div>
          </a>

          <a href="https://annual-report.vectorinstitute.ai/"
             target="_blank"
             class="featured-card">
            <div class="featured-source">
              Featured in Vector Institute Annual Report 2025–26
            </div>
            <div class="featured-title">
              Where AI possibilities come to life
            </div>
          </a>

          <a href="https://vectorinstitute.ai/when-ai-helps-too-much-towards-understanding-and-measuring-cognitive-atrophy-in-llm-behaviour/"
             target="_blank"
             class="featured-card">
            <div class="featured-source">
              Featured in Vector Institute News
            </div>
            <div class="featured-title">
              When AI helps too much: Towards understanding and measuring Cognitive Atrophy in LLM behaviour
            </div>
          </a>

        </div>

        <style>
          .featured-links {
            display: grid;
            grid-template-columns: repeat(3, minmax(0, 1fr));
            gap: 1.5rem;

            width: min(1250px, 94vw);
            position: relative;
            left: 50%;
            transform: translateX(-50%);

            margin-top: 1.5rem;
          }

          .featured-card {
            display: flex;
            flex-direction: column;
            justify-content: center;

            min-height: 190px;
            padding: 1.75rem;

            background: #ffffff;
            border: 1px solid #e2e8f0;
            border-radius: 16px;

            color: inherit;
            text-decoration: none !important;

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
            margin-bottom: 0.8rem;

            font-size: 0.85rem;
            font-weight: 700;
            letter-spacing: 0.04em;
            text-transform: uppercase;

            opacity: 0.65;
          }

          .featured-title {
            font-size: 1.25rem;
            font-weight: 700;
            line-height: 1.4;
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
        padding: [1rem, 0, 2rem, 0]


  # =========================================================
  # RESEARCH PUBLICATIONS
  # =========================================================
  - block: collection
    id: publications
    content:
      title: Research Publications
      sort_by: weight
      order: desc
      count: 6
      filters:
        folders:
          - publications
    design:
      view: article-grid
      columns: 2
      spacing:
        padding: [1rem, 0, 1rem, 0]

---