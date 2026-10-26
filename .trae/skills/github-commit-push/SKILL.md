---
name: github-commit-push
description: Commit all changes and push the entire project to GitHub (https://github.com/Palovil/wxy.git). Invoke when user says "提交到github", "push到github", "上传到github", "commit and push to github", "push to github" etc.
---

# GitHub Commit & Push Workflow

Target remote: `https://github.com/Palovil/wxy.git` (remote name: `github`)

1. Record prompt details (timestamp, model, prompt content) to `wang_prompt.md` — append, never overwrite
2. Check status & branch: `git status`, `git branch --show-current`
3. Review recent commit style: `git log --oneline -5`
4. Add all: `git add -A`
5. Commit with a concise message summarizing the changes (follow existing commit style)
6. Ensure the `github` remote exists and points to the right URL:
   - `git remote add github https://github.com/Palovil/wxy.git` (skip if it already exists)
   - If it exists but points elsewhere: `git remote set-url github https://github.com/Palovil/wxy.git`
7. Push: `git push -u github main` (use the current branch name if not `main`)

## Project Context
- Static HTML/CSS coursework for "Advanced Web Design"
- No build, no dependencies — push the whole working tree as-is
- Entry point: `index.html`
- Some filenames contain Chinese characters — quote paths in shell commands

## Workflow Notes
- Keep the existing `origin` remote (gitee) untouched; only add/update the `github` remote
- Never force push; if push is rejected (non-fast-forward), run `git pull --rebase github main` then retry push
- Do NOT commit files that likely contain secrets (.env, credentials)
- Do NOT skip hooks (--no-verify)
- Report the final push result (success or error) to the user
