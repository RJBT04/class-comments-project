# Class-Comments

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Website](https://img.shields.io/website?url=https%3A%2F%2Frjbt04.github.io/class-comments-project)](https://rjbt04.github.io/class-comments-project)
[![CI](https://github.com/RJBT04/class-comments-project/actions/workflows/ci.yml/badge.svg)](https://github.com/RJBT04/class-comments-project/actions/workflows/ci.yml)
[![Python](https://img.shields.io/badge/Python-3.11%2B-blue.svg?logo=python)](https://www.python.org/)

A lightweight classroom exercise to practice **fork → branch → pull request → review** using a shared `comments.md` file and optional per-student folders.

- 📄 **Instructions (students):** see [Instruction.md](Instruction.md)
- 🌐 **GitHub Pages site:** [https://rjbt04.github.io/class-comments-project](https://rjbt04.github.io/class-comments-project)
- 💬 **Comments board:** [https://rjbt04.github.io/class-comments-project/comments](docs/comments.md)

## What students do
1. Fork this repo, create a branch, and append your entry to `docs/comments.md` using the template provided.
2. (Optional) Add your personal folder under `submissions/<your-github-username>/README.md`.
3. Open a Pull Request back to `main`.

## Rules
- Do **not** commit directly to `main` (protected).
- PRs should only change `docs/comments.md` and/or `submissions/<your-github-username>/**`.
- The CI checks will fail if other files are changed.

## Folder structure
```
.
├─ docs/                    # GitHub Pages content
│  ├─ index.md              # Landing page
│  ├─ comments.md           # Shared comment board (students append here)
│  └─ _config.yml           # Jekyll theme config (Minimal)
├─ submissions/
│  └─ _TEMPLATE/README.md   # Copy to submissions/<your-username>/README.md
├─ .github/
│  ├─ CODEOWNERS            # Requires maintainer review (with branch protection)
│  ├─ PULL_REQUEST_TEMPLATE.md
│  └─ workflows/ci.yml      # Path guard + basic checks
├─ Instruction.md           # Step-by-step for instructor & students
└─ LICENSE                  # MIT
```

---

> Maintained by @RJBT04. Issues and PRs welcome!
