---
title: "Private Embedding Lookup with Encrypted Compact Queries under Fully Homomorphic Encryption"

authors:
  - Jung Hee Cheon
  - me
  - Jaehee Kang
  - Hanee Rhee

date: "2026-06-07T00:00:00Z"
publishDate: "2026-06-02T00:00:00Z"

publication_types: ["article"]

peer_reviewed: false
open_access: true
share: false

abstract: |
  Many NLP and recommendation models begin by mapping discrete client inputs to
  embedding vectors. Since these inputs can reveal sensitive information, the
  embedding step must be protected in privacy-preserving inference. Fully
  Homomorphic Encryption (FHE) enables inference over encrypted client data, but
  turns embedding lookup from simple table access into homomorphic computation.
  To keep the embedding table server-side and avoid transmitting encrypted
  embedding vectors from the client, this work focuses on server-side lookup:
  the client sends only a small encrypted index.

  Prior work first builds a one-hot vector from the encrypted index before
  multiplying it with the embedding table, making one-hot generation the
  dominant cost. This paper observes that private embedding lookup only requires
  a linearly independent representation of the encrypted index, not the one-hot
  basis itself. It proposes Independent Vector Evaluation (IVE), which evaluates
  a linearly independent vector from successive powers of one encrypted value,
  reducing vector-generation cost from O(p log p) to O(p). The method recovers
  the embedding vector through a precomputed change of basis instantiated with an
  orthogonal Discrete Cosine Transform (DCT). The implementation improves
  amortized lookup time by up to 78.4x over the prior method and reduces the
  vector-generation share of encrypted FastText inference time on Enron-Spam
  from 99.6% to 66.3%.

summary: "A private embedding lookup method using encrypted compact queries and Independent Vector Evaluation under fully homomorphic encryption."

tags:
  - Homomorphic Encryption
  - CKKS
  - Privacy-Preserving Machine Learning
  - Encrypted Inference

featured: true

author_order_note: "Authors listed alphabetically."

presentations:
  - kind: Poster
    name: FHE.org Conference 2026
    date: Mar. 2026
    location: Taipei, Taiwan
    url: https://fhe.org/conferences/conference-2026/
    links:
      - label: Poster
        url: https://fhe.org/conferences/conference-2026/resources/posters/%5B23%5D%20-%20Efficient%20Private%20Embedding%20Lookup%20via%20Independent%20Vector%20Evaluation.pdf

links:
  - type: pdf
    url: https://arxiv.org/pdf/2606.03191
  - type: custom
    label: arXiv
    url: https://arxiv.org/abs/2606.03191

image:
  caption: ''
  focal_point: ''
  preview_only: false

projects: []
slides: ""
---

Preprint available on arXiv. Latest checked version: v3, June 7, 2026.
