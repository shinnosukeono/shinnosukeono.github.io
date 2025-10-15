---
title: "AIRoA MoMa Dataset: A Large-Scale Hierarchical Dataset for Mobile Manipulation"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
- Ryosuke Takanami
- Petr Khrapchenkov
- Shu Morikuni
- Jumpei Arima
- Yuta Takaba
- Shunsuke Maeda
- Takuya Okubo
- Genki Sano
- Satoshi Sekioka
- Aoi Kadoya
- Motonari Kambara
- Naoya Nishiura
- Haruto Suzuki
- Takanori Yoshimoto
- Koya Sakamoto
- Shinnosuke Ono
- Hu Yang
- Daichi Yashima
- Aoi Horo
- Tomohiro Motoda
- Kensuke Chiyoma
- Hiroshi Ito
- Koki Fukuda
- Akihito Goto
- Kazumi Morinaga
- Yuya Ikeda
- Riko Kawada
- Masaki Yoshikawa
- Norio Kosuge
- Yuki Noguchi
- Kei Ota
- Tatsuya Matsushima
- Yusuke Iwasawa
- Yutaka Matsuo
- Tetsuya Ogata

# Author notes (optional)
# author_notes:

date: "2025-09-29T00:00:00Z"
doi: "10.48550/arXiv.2509.25032"

# Schedule page publish date (NOT publication's date).
publishDate: "2025-09-29T00:00:00Z"

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
pages:
page_start:
page_end:

abstract: |-
  As robots transition from controlled settings to unstructured human environments, building generalist agents that can reliably follow natural language instructions remains a central challenge. Progress in robust mobile manipulation requires large-scale multimodal datasets that capture contact-rich and long-horizon tasks, yet existing resources lack synchronized force-torque sensing, hierarchical annotations, and explicit failure cases. We address this gap with the AIRoA MoMa Dataset, a large-scale real-world multimodal dataset for mobile manipulation. It includes synchronized RGB images, joint states, six-axis wrist force-torque signals, and internal robot states, together with a novel two-layer annotation schema of sub-goals and primitive actions for hierarchical learning and error analysis. The initial dataset comprises 25,469 episodes (approx. 94 hours) collected with the Human Support Robot (HSR) and is fully standardized in the LeRobot v2.1 format. By uniquely integrating mobile manipulation, contact-rich interaction, and long-horizon structure, AIRoA MoMa provides a critical benchmark for advancing the next generation of Vision-Language-Action models. The first version of our dataset is now available at [this https URL](https://huggingface.co/datasets/airoa-org/airoa-moma).

# Summary. An optional shortened abstract.
summary: "A large-scale real-world multimodal dataset for mobile manipulation featuring 25,469 episodes with synchronized RGB images, joint states, force-torque signals, and a novel two-layer annotation schema for hierarchical learning."

tags: ["Robotics", "Mobile Manipulation", "Vision-Language-Action Models", "Dataset", "Multimodal Learning"]

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: https://arxiv.org/pdf/2509.25032v1
url_dataset: https://huggingface.co/datasets/airoa-org/airoa-moma

# add Almetric adn dimensions badges
add_badge: true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'AIRoA MoMa Dataset Overview'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
# projects:
# - example

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
