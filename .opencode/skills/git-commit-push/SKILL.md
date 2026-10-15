---
name: git-commit-push
description: Commit all changes and push to remote repository. Use when user says "提交项目", "commit and push", "提交代码", "push to remote" etc.
---

# Git Commit & Push Workflow

1. Check status: `git status`
2. Add all: `git add -A`
3. Commit: `git commit -m "Initial commit: HTML/CSS coursework project"`
4. Add remote: `git remote add origin <url>`
5. Push: `git push -u origin main`

## Notes
- Project is static HTML/CSS coursework (Advanced Web Design)
- No build, no JS, no dependencies
- Entry point: index.html
- All class/ID names prefixed with `wang_`
- Filenames may contain Chinese characters
- After completing tasks, append prompt details to `wang_prompt.md`
