# Instruction Guide

This repository supports a class exercise where students practice creating pull requests against a shared file.

---
## Part A — Instructor setup (once)

1. **Create the repository**
   - Create **RJBT04/class-comments-project** (Public). Initialize with a README (optional).

2. **Add starter files**
   - Easiest: upload the provided ZIP to GitHub (Add file → Upload files) and commit to `main`.
   - Or clone locally and copy the files, then push to GitHub.

3. **Enable GitHub Pages**
   - Go to **Settings → Pages**.
   - **Build and deployment** → *Source*: **Deploy from a branch**.
   - Select **Branch: `main`** and **Folder: `/docs`**. Save.
   - Your site will publish at **https://rjbt04.github.io/class-comments-project** within a few minutes.

4. **Protect `main`**
   - Go to **Settings → Branches → Add rule**.
   - Rule pattern: `main`.
   - Check:
     - ✅ **Require a pull request before merging** (set **Required approvals**: 1)
     - ✅ **Require review from Code Owners** (uses `.github/CODEOWNERS`)
     - ✅ **Require status checks to pass** → select **CI** workflow
     - ✅ **Do not allow bypassing the above settings** (recommended)
     - ✅ **Restrict who can push to matching branches** → allow only maintainers (prevents direct pushes)
   - Save changes.

5. **(Optional) Enable Discussions**
   - Settings → General → Enable Discussions.

6. **Test**
   - Open a small PR that edits `docs/comments.md` to verify checks & review flow.

---
## Part B — Student instructions

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

