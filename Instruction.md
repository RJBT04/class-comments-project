# Instruction Guide

This repository supports a class exercise where students practice creating pull requests against a shared file.

---
## Student instructions

> Goal: append your comment block to the shared page and submit a Pull Request.

1. **Fork** the repo
   - Visit https://github.com/RJBT04/class-comments-project → **Fork**.

2. **Create your branch**
   - In your fork, click **Add file → Create new file** *or* edit via the web UI.
   - Name your branch like `add-comment-<your-github-username>`.

3. **Add your comment**
   - Edit `docs/comments.md` and append your entry **at the bottom** of the file.
   - Use this template exactly:

   ```md
   ## @{your-github-username} — YYYY-MM-DD
   - Course: <course or cohort>
   - Comment: <your message>
   ```

4. **(Optional) Create your folder**
   - Add `submissions/<your-github-username>/README.md` using the template in `submissions/_TEMPLATE/README.md`.

5. **Commit & open a Pull Request**
   - Commit changes to your branch in your fork.
   - Click **Compare & pull request**.
   - Fill out the PR template and submit.

6. **Respond to review**
   - If the maintainer requests changes, update your branch and the PR will refresh automatically.

> Tips to avoid merge conflicts: Always **append** your entry at the bottom, and keep one blank line between entries.

---
## Maintainer tips

- If two PRs conflict in `docs/comments.md`, use the web editor to keep both blocks. Maintain the `---` separators.
- You can squash-merge to keep a tidy history.
- The CI workflow (`.github/workflows/ci.yml`) will fail any PR that changes files outside `docs/comments.md` and `submissions/**`.

