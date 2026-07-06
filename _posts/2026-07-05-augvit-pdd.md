---
layout: post
title: "AugViT: Vision Transformers for Plant Disease Diagnosis in the Field"
date: 2026-07-05 09:00:00 -0400
category: advanced-projects
subcategory: advanced-projects
author: dan
featured: true
short-description: "A Vision Transformer approach to plant disease classification on real-world smartphone imagery, reaching a 0.9471 F1 score via the FlipMix augmentation strategy."
repo_url: https://github.com/danknyan/PLACEHOLDER_augvit-pdd
---

AugViT investigates Vision Transformers (ViTs), paired with aggressive regularisation, for plant disease diagnosis on the **FieldPlant** dataset — real, messy, smartphone-captured imagery from rural Cameroon.

**Highlights:**

- F1 score of 0.9471, Accuracy of 0.9457
- The "FlipMix" online augmentation strategy alone contributed a +0.1837 increase in F1
- Outperforms established CNN baselines on noisy, in-field imagery
- Explores the patch size vs. precision vs. compute trade-off for real-world deployment

[View the code and full write-up on GitHub]({{ page.repo_url }})
