---
title: "Mitigating Reward Hacking in RLHF via Advantage Sign Robustness"

# Authors
authors:
- Shinnosuke Ono
- Johannes Ackermann
- Soichiro Nishimori
- Takashi Ishida
- Masashi Sugiyama

# Author notes (optional)
# author_notes:

date: "2026-04-03T00:00:00Z"
doi: "10.48550/arXiv.2604.02986"

# Schedule page publish date (NOT publication's date).
publishDate: "2026-04-03T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent; 9 = Reference Manual; 10 = Poster; 11 = Unpublished;
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "*EIML Workshop at ICML 2026*"
publication_short: "*EIML@ICML 2026*"
volume:
issue:
article:
pages:
page_start:
page_end:

abstract: |-
  Reward models (RMs) used in reinforcement learning from human feedback (RLHF) are vulnerable to reward hacking: as the policy maximizes a learned proxy reward, true quality plateaus or degrades. We make the assumption that reward hacking is often caused by flipped advantage signs: instead of reducing the likelihood of a bad response, a flipped sign causes the update to increase it. By considering an adversarial perturbation in the RM parameter space, we can derive a certified sign-preservation radius, which is the smallest perturbation that can flip the advantage sign during policy optimization. Based on this formulation, we propose Sign-Certified Policy Optimization (SignCert-PO), down-weighting non-robust completions in the policy gradient update. Unlike prior approaches that require multiple RMs or access to the RM training data, SignCert-PO is lightweight and operates purely at the policy optimization stage using only the RM parameters and on-policy completions. On TL;DR summarization and AlpacaFarm benchmarks, SignCert-PO consistently achieves a better win rate than baselines and reduces reward hacking.

# Summary. An optional shortened abstract.
summary: "We address reward hacking in RLHF by identifying flipped advantage signs as a key cause and proposing Sign-Certified Policy Optimization (SignCert-PO), a lightweight method that down-weights non-robust completions during policy optimization."

tags: ["Reinforcement Learning", "RLHF", "Reward Hacking", "Large Language Models"]

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: https://arxiv.org/pdf/2604.02986

# add Altmetric and Dimensions badges
add_badge: false

# Featured image
image:
  caption: ''
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
# projects:
# - example

# Slides (optional).
slides: ""
---

{{% callout note %}}
Click the *Cite* button above to get publication metadata for your reference management software in *.bib* format.
{{% /callout %}}
