# Site Build Log - 2026-06-24

This file summarizes the working conversation and site decisions so future
sessions can continue without relying on chat history alone.

Repository and deployment:

- The active repository is `/Users/apple/jadh0309.github.io`.
- Git remote is `https://github.com/jadh0309/jadh0309.github.io`.
- Main branch tracks `origin/main`.
- Site `baseURL` was updated to `https://jadh0309.github.io/`.

Profile and bio:

- About Me was changed from third-person wording to first-person wording.
- Prof. Jung Hee Cheon is linked to the SNU-domain homepage:
  `https://web.math.snu.ac.kr/~jhcheon/`.
- Profile links include email, GitHub, LinkedIn, and Google Scholar.
- Japanese was removed from the Languages section; Korean and English remain.

Design and theme:

- Dracula theme is used as the main visual direction.
- Dark/light toggle remains enabled.
- Navbar colors were adjusted to better match the Dracula palette.
- Skills section was removed from the visible site.

Publications:

- Publication pages include paper-wise notes that author order is alphabetical.
- Talks and posters are attached to their corresponding publication pages.
- Publication social share buttons were hidden with `share: false`.
- `data/page_sharer.yaml` exists as a local override, currently keeping only the
  email share link if sharing is enabled on any page.

Specific publication notes:

- `cryptanalysis-lightweight-vhe` uses IACR/ePrint-style links as requested.
- `private-embedding-lookup` uses the latest arXiv version checked during the
  site build work.
- `private-embedding-lookup` includes:
  - FHE.org Conference 2026 poster.
  - 2025 KMS Annual Meeting talk information found from the KMS program page.
    The official program identified the presenter as Jaehee Kang.
- `swift-functional-bootstrapping` includes KMS 2026 information using the
  official event name:
  `International Conference for the 80th Anniversary of the Korean Mathematical Society`.

CV:

- CV source is `cv/daehyun-jang-cv.tex`.
- Download PDF is `static/uploads/resume.pdf`.
- After editing the CV source, compile with:

```bash
cd cv
latexmk -pdf -interaction=nonstopmode -halt-on-error daehyun-jang-cv.tex
latexmk -c daehyun-jang-cv.tex
cd ..
cp cv/daehyun-jang-cv.pdf static/uploads/resume.pdf
```

Current convention:

- Keep site-visible content polished and concise.
- Keep implementation notes in `.codex/` rather than publishing them as blog
  posts.
- Do not store secrets or private material in `.codex/`; it is part of the
  repository if committed.
