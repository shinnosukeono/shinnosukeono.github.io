---
layout: page
title: false negatives in multimodal contrastive learning
description: the non-diagonal pairs in a minibatch are unlabeled, not negative
img: assets/img/pu_clip_false_negatives.png
importance: 1
category: research
---

Contrastive learning excels at learning high-quality representations from web-scale datasets
with implicit supervision, such as image-text pairs where captions serve as loose contextual
cues rather than explicit annotations for the downstream tasks. It does so by bringing
semantically similar pairs closer in the representation space while pushing dissimilar pairs
away. In multimodal contrastive learning such as CLIP, however, it is often difficult to
identify dissimilar pairs. In the common implementation, all image-text pairs within a
minibatch that do not correspond to each other, the non-diagonal pairs, are considered to be
the negative pairs. Yet these pairs sometimes have semantically similar information, leading
to the problem of *false negatives* and alignment degradation.

{% include figure.liquid path="assets/img/pu_clip_false_negatives.png" class="img-fluid rounded z-depth-1" %}

<div class="caption">
  The motivating example from my defense: an image of "a dog playing in a park" may be
  negatively paired with a caption of "a dog retrieving a ball outdoors". The standard CLIP
  loss cannot tell the two apart from a genuinely dissimilar pair, so it treats them as
  negative.
</div>

To mitigate this, I proposed PU CLIP, a modified contrastive learning objective where the
non-diagonal pairs in a minibatch are treated as unlabeled, inspired by the
positive-unlabeled learning technique. Experiments on real-world datasets suggest that CLIP
training suffers from false negatives especially for large batch sizes, and that PU CLIP
partially leads to improved zero-shot classification performance.

My bachelor's thesis, supervised by Prof. Masashi Sugiyama and Prof. Takashi Ishida.

---

Shinnosuke Ono. *Improving Multimodal Contrastive Learning with Positive-Unlabeled Learning*.
Bachelor's thesis, Department of Information Science, the University of Tokyo, January 2025.
