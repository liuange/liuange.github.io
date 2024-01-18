---
title: "Automated Classification of Municipal Zoning Codes"
date: 2022-03-01
draft: false
project_tags: ["python", "nlp", "geospatial"]
weight: 1
links:
  another_link:
    text: "Github Repo"
    icon: "fab alt brands fa-github"
    href: "#"
    weight: 1
---

Can we use natural language processing to label the allowed residential uses of zoning districts in California?
Data science project for INFO 259 Natural Language Processing with Prof. David Bamman.

---

# The Problem {#problem}

Zoning districts define what kind of building structures or uses are allowed on different parcels of land. These districts are officially established by cities in the text of municipal codes. Our task is to categorize cities’ highly granular zoning districts into **three distinct categories (single-family, multifamily, and non-residential)** based on the expressed purpose statements of the zoning definition.

# The Approach {#approach}

- Scrape data from publicly hosted municipal code websites.
- Specifically, we want to identify a particular paragraph present in the articles defining each zone: the "intent" or "purpose" paragraph.

# Currently working on {#current}

The scraping strategy: the structure of municipal code pages vary. How can we identify these intent/purpose paragraphs efficiently?
