---
title: "Cryptanalysis on Lightweight Verifiable Homomorphic Encryption"

authors:
  - Jung Hee Cheon
  - me

date: "2025-12-08T00:00:00Z"
publishDate: "2025-12-08T00:00:00Z"

publication_types: ["paper-conference"]

publication:
  name: "Advances in Cryptology - ASIACRYPT 2025"
  short_name: "ASIACRYPT 2025"
  pages: "366-397"

peer_reviewed: true
open_access: true
share: false

abstract: |
  Verifiable Homomorphic Encryption (VHE) integrates Homomorphic Encryption
  (HE) with Verifiable Computation (VC), aiming to provide privacy and integrity
  for outsourced computation. Chatel et al. introduced two VHE schemes,
  Replication Encoding (REP) and Polynomial Encoding (PE), and a similar
  approach to REP was used by Albrecht et al. to develop a Verifiable Oblivious
  PRF scheme (vADDG).

  This paper gives efficient forgery attacks against the verifiability guarantees
  of these schemes. The first strategy targets REP and vADDG by extracting
  embedded secret information in encrypted form and using it to forge output
  ciphertexts that pass verification. The second targets PE by exploiting its
  secret embedding structure to forge outputs that remain valid on verification
  inputs while violating verifiability. The vADDG attack shows that the proposed
  80-bit parameters provide at most 10 bits of concrete security, and the REP and
  PE attacks succeed with probability 1 in linear time when fully homomorphic
  encryption is used.

summary: "Cryptanalysis of lightweight verifiable homomorphic encryption schemes, including REP, PE, and vADDG-style constructions."

tags:
  - Homomorphic Encryption
  - Verifiable Computation
  - Cryptanalysis

featured: true

author_order_note: "Authors listed alphabetically."

presentations:
  - kind: Talk
    name: Korean Mathematical Society 2024 Fall Meeting
    date: Oct. 2024
    location: Suwon, Republic of Korea
    url: https://www.kms.or.kr/conference/2024_fall/
  - kind: Talk
    name: ASIACRYPT 2025
    date: Dec. 2025
    location: Melbourne, Australia
    url: https://asiacrypt.iacr.org/2025/

links:
  - type: pdf
    url: https://eprint.iacr.org/2025/1890.pdf
  - type: custom
    label: DOI
    url: https://doi.org/10.1007/978-981-95-5122-4_12

image:
  caption: ''
  focal_point: ''
  preview_only: false

projects: []
slides: ""
---

Published at ASIACRYPT 2025.
