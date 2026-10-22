---
name: git-commit-push
description: Commit all changes and push to remote repository. Invoke when user says "提交项目", "commit and push", "提交代码", "push to remote", "推送到远程" etc.
---

# Git Commit & Push Workflow

1. Check status: `git status`
2. Add all: `git add -A`
3. Commit: `git commit -m "Initial commit: HTML/CSS coursework project"`
4. Add remote (if not already configured): `git remote add origin <url>`
5. Push: `git push -u origin main`

## Project Context
- Static HTML/CSS coursework for "Advanced Web Design"
- No build, no JS, no dependencies
- Entry point: `index.html` (open directly in browser, no dev server needed)
- All pages are self-contained (inline `<style>`); only `5-1 层叠与继承.html` uses external `css.css`
- All CSS class/ID names and JS variables are prefixed with `wang_`
- Some filenames contain Chinese characters — quote paths in shell commands

## Workflow Notes
- Before executing, verify current branch with `git branch --show-current`
- If remote `origin` already exists, skip step 4
- If push is rejected (non-fast-forward), run `git pull --rebase origin main` then retry push
- After completing tasks, append prompt details (timestamp, model, prompt content) to `wang_prompt.md` — never overwrite existing content
