## Project

Static HTML/CSS coursework for "Advanced Web Design". No build, no JS, no dependencies.

- Open `index.html` directly in a browser — no dev server needed.
- Entry point: `index.html` (portfolio grid linking all exercises).
- All pages are self-contained (inline `<style>`). Only `5-1 层叠与继承.html` uses the external `css.css`.
- Some filenames contain Chinese characters — quote paths when referencing them in shell commands.
- No lint, no typecheck, no tests — visual verification in a browser is the only check.

## Conventions

- All CSS class names, ID names, and JS variables must start with `wang_`.
- Before executing any user request, append the prompt details (timestamp, model, prompt content) to `wang_prompt.md`. Never overwrite existing content.
