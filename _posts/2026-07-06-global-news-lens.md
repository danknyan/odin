---
layout: post
title: "Global News Lens: NLP Topic Modeling of World News"
date: 2026-07-06 09:00:00 -0400
category: natural-language-processing
subcategory: natural-language-processing
author: dan
featured: true
image: world-news-preview.png
short-description: "An end-to-end NLP pipeline turning GDELT news data into an interactive global topic map, powered by hierarchical topic modeling and LLM-generated labels."
repo_url: https://github.com/danknyan/world-news-map
demo_url: https://danknyan.github.io/world-news-map/
---

Global News Lens is an end-to-end NLP pipeline that transforms raw global news text into an interactive choropleth dashboard of world news topics, built on data from [GDELT](https://www.gdeltproject.org/).

**Highlights:**

- Hierarchical topic modeling (TraCo) across a four-layer topology, tuned via k-top word selection
- Automated topic label generation using Qwen3, with multistep generation and validation/retry logic
- Large-scale deduplication pipeline combining MinHash, LSH, and Union-Find clustering
- Interactive three-panel dashboard: choropleth map, topic network, and article detail panel
- Deployed via GitHub Actions

[View the code on GitHub]({{ page.repo_url }}) · [Try the live dashboard]({{ page.demo_url }})

*Capstone project, Master of Engineering in Data Science, University of Sydney.*
