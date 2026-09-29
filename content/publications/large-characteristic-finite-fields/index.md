---
title: "Arithmetic for Large-Characteristic Finite Fields in CKKS"

authors:
  - me
  - Junho Lee

date: "2026-09-10T00:00:00Z"
publishDate: "2026-09-10T00:00:00Z"
lastmod: "2026-09-14T00:00:00Z"

publication_types: ["article"]

peer_reviewed: false
open_access: true
share: false

abstract: |
  Seuré and Suvanto (ePrint 2026/1102) recently showed that, for
  small-characteristic primes $p$, arithmetic over $\mathbb{F}_{p^r}$ can be
  homomorphically evaluated in CKKS via a technique they call *spectral
  encoding*. Their construction is, however, restricted to small
  characteristic: ciphertext multiplication amplifies the error by the
  operator norm of the multiplied plaintext.

  Under the spectral encoding, a field element in $\mathbb{F}_{p^r}$ is encoded
  to a plaintext with operator norm at most $O(rp)$. The error therefore grows
  by a factor of $rp$ in the worst case, limiting the supported size of the
  characteristic prime $p$. In this work, we propose *bi-spectral encoding*,
  which decomposes the coefficients of the plaintext polynomials used in the
  spectral encoding of Seuré and Suvanto.

  With a decomposition parameter $d$, a field element in $\mathbb{F}_{p^r}$ can
  be encoded to a plaintext with operator norm $O(rd p^{1/d})$, for a suitable
  choice of encoding parameters. We give a comprehensive analysis of error
  growth and derive a bound on error amplification under multiplication.

  For fields with a 256-bit prime characteristic (secp256k1) and extension
  degrees $1$, $2$, and $4$, we provide numerical simulations of error
  amplification and compute the maximum multiplication counts attainable in
  each case. We further present a bootstrapping procedure that reduces both
  the size of the plaintext and its noise.

summary: "Bi-spectral encoding for arithmetic over large-characteristic finite fields in CKKS, with bounds on error amplification and a bootstrapping procedure."

tags:
  - Homomorphic Encryption
  - CKKS
  - Finite-Field Arithmetic
  - Large Precision Arithmetic

featured: true

links:
  - type: pdf
    url: https://eprint.iacr.org/2026/1958.pdf
  - type: custom
    label: IACR ePrint
    url: https://eprint.iacr.org/2026/1958

image:
  caption: ''
  focal_point: ''
  preview_only: false

projects: []
slides: ""
---

Working draft. First posted on September 10, 2026; revised on September 14, 2026.
