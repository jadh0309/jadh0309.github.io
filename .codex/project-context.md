# Project Context

Repository: `jadh0309.github.io`

Purpose: Personal academic website for Daehyun Jang, built with Hugo Blox's
academic CV template and deployed with GitHub Pages.

Current site identity:

- Name: Daehyun Jang
- Affiliation: Seoul National University
- Role: Ph.D. Student in Mathematical Sciences
- Advisor: Prof. Jung Hee Cheon
- Research areas: homomorphic encryption, CKKS, lattice-based cryptography,
  privacy-preserving computation

Important files:

- `data/authors/me.yaml`: profile, bio, social links, education, experience
- `content/_index.md`: home page blocks
- `content/experience.md`: experience page layout and language section
- `content/publications/*/index.md`: publication pages
- `layouts/publications/single.html`: local publication page override
- `cv/daehyun-jang-cv.tex`: source CV
- `static/uploads/resume.pdf`: downloadable CV on the site
- `data/page_sharer.yaml`: local override for page share buttons

Useful commands:

```bash
PATH="/opt/homebrew/bin:$PATH" hugo --minify --cleanDestinationDir
PATH="/opt/homebrew/bin:$PATH" ./node_modules/.bin/pagefind --site public
git diff --check
```

Deployment flow:

```bash
git add <changed-files>
git commit -m "<message>"
git push
```
