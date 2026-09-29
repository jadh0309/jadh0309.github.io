---
title: "SWIFT: Shallow and SIMD-Aware CKKS Functional Bootstrapping for Low-Latency"

authors:
  - Jung Hee Cheon
  - me
  - Jaehee Kang

date: "2026-06-09T00:00:00Z"
publishDate: "2026-06-09T00:00:00Z"

publication_types: ["article"]

peer_reviewed: false
open_access: true
share: false

abstract: |
  The CKKS homomorphic encryption scheme
  can achieve high throughput for large batches, typically of
  tens of thousands of inputs, whereas DM/CGGI schemes offer low latency for a single input.
  In existing CKKS approaches, the multiplicative depth required for nonlinear function evaluation demands a large ciphertext modulus, which forces a large ring degree regardless of the input size.
  Practical applications, such as encrypted MLP inference, may require
  only a few hundred function evaluations at a time.
  For these moderate batch sizes, existing CKKS-based methods
  requiring large multiplicative depth incur high latency
  without fully benefiting from their high throughput.

  We present SWIFT, a CKKS functional-bootstrapping
  method that reduces latency by using multiple slots to lower
  multiplicative depth.
  For input $x$, SWIFT packs its integer multiples $\ell x$ into unused slots. Exponential bootstrapping then generates the powers $\exp(2\pi\mathrm{i}\ell x)=\exp(2\pi\mathrm{i} x)^\ell=\alpha^\ell$ in parallel. Compared to previous approaches that compute these powers through homomorphic multiplications, SWIFT directly generates those powers and reduces the required multiplicative depth and ciphertext modulus, allowing a smaller ring degree and lower latency.

  We also introduce a trigonometric approximation method for
  singular functions such as $1/\sqrt{x}$, whose derivative
  is unbounded near zero.
  We observe that the previous Fourier extension method of Bian et al.
  (EUROCRYPT'26) can produce extremely large coefficient norms
  for these functions when focusing solely on reducing the polynomial degree.
  Instead, we solve an optimization problem to find a trigonometric polynomial that minimizes the coefficient norm while satisfying the required approximation accuracy for the target function.
  The resulting trigonometric polynomial can be evaluated
  efficiently and with numerical stability using SWIFT.

  Our implementation evaluates ReLU on $[-1,1]$ and $1/\sqrt{x}$ on $[0.0005,1]$ with 12-bit absolute and relative precision, respectively, at ring degree $\log N=15$. For batches of 512 inputs, SWIFT achieves speedups of $3.94\times$ and $2.86\times$ over the corresponding CKKS baselines for ReLU and $1/\sqrt{x}$, respectively.
  Compared with latency estimates of DM/CGGI-based methods, SWIFT achieves
  lower latency for 8-to-8 LUT and 12-to-12 LUT
  at batch sizes as small as 32 inputs.

summary: "A shallow and SIMD-aware CKKS functional bootstrapping method designed for low-latency encrypted computation."

tags:
  - Homomorphic Encryption
  - CKKS
  - Functional Bootstrapping

featured: true

author_order_note: "Authors listed alphabetically."

presentations:
  - kind: Talk
    name: International Conference for the 80th Anniversary of the Korean Mathematical Society
    date: Jun. 23, 2026
    location: Seoul, Republic of Korea
    url: https://www.kms.or.kr/conference/meeting/index.html?period=91
  - kind: Talk
    name: "PACOH Workshop: Homomorphic Encryption 2026"
    date: Jun. 29, 2026
    location: Sokcho, Republic of Korea
    url: https://symposia.kias.re.kr/pacoh-he2026

links:
  - type: pdf
    url: https://eprint.iacr.org/2026/1163.pdf
  - type: custom
    label: IACR ePrint
    url: https://eprint.iacr.org/2026/1163

image:
  caption: ''
  focal_point: ''
  preview_only: false

projects: []
slides: ""
---
