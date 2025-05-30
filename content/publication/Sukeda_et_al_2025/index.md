---
title: "A Japanese Language Model and Three New Evaluation Benchmarks for
Pharmaceutical NLP"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here 
# and it will be replaced with their full name and linked to their profile.
authors:
- Issey Sukeda
- Takuro Fujii
- Kosei Buma
- Shunsuke Sasaki
- admin

# Author notes (optional)
# author_notes:

date: "2025-05-22T00:00:00Z"
doi: "10.48550/arXiv.2505.16661"

# Schedule page publish date (NOT publication's date).
publishDate: "2021-08-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent; 9 = Reference Manual; 10 = Poster; 11 = Unpublished;
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: "*arXiv Preprint*"
publication_short: "*arXiv Preprint*"
volume: 
issue: 
article: 
pages: 15
page_start: 
page_end: 

abstract: |-
  We present a Japanese domain-specific language model for the pharmaceutical field, developed through continual pretraining on 2 billion Japanese pharmaceutical tokens and 8 billion English biomedical tokens. To enable rigorous evaluation, we introduce three new benchmarks: YakugakuQA, based on national pharmacist licensing exams; NayoseQA, which tests cross-lingual synonym and terminology normalization; and SogoCheck, a novel task designed to assess consistency reasoning between paired statements. We evaluate our model against both open-source medical LLMs and commercial models, including GPT-4o. Results show that our domain-specific model outperforms existing open models and achieves competitive performance with commercial ones, particularly on terminology-heavy and knowledge-based tasks. Interestingly, even GPT-4o performs poorly on SogoCheck, suggesting that cross-sentence consistency reasoning remains an open challenge. Our benchmark suite offers a broader diagnostic lens for pharmaceutical NLP, covering factual recall, lexical variation, and logical consistency. This work demonstrates the feasibility of building practical, secure, and cost-effective language models for Japanese domain-specific applications, and provides reusable evaluation resources for future research in pharmaceutical and healthcare NLP. Our model, codes, and datasets are released at this [https URL](https://github.com/EQUES-Inc/pharma-LLM-eval).

# Summary. An optional shortened abstract.
summary: "This paper presents a Japanese phamaceutical-specific langauge model, JPharmatron, along with a benchmark suite consisting three new benchmarks:  YakugakuQA (Japanese national pharmacist licensing exams); NayoseQA (cross-lingual synonym and terminology normalization); and SogoCheck (consistency reasoning between paired statements.)"

tags: ["Large Language Models", "Evaluation Benchmark", "Domain Specific LLMs"]

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: https://arxiv.org/pdf/2505.16661v1
url_code: https://github.com/EQUES-Inc/pharma-LLM-eval
url_dataset: https://huggingface.co/collections/EQUES/jpharmabench-680a34acfe96870e41d050d8
url_model: https://huggingface.co/collections/EQUES/jpharmatron-680a330b4dfce3ac43009984

# add Almetric adn dimensions badges
add_badge: true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Model and Evaluation Design'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
# projects:
# - mmpp

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

{{% callout note %}}
Click the *Cite* button above to get publication metadata for your reference management software in *.bib* format.
{{% /callout %}}
