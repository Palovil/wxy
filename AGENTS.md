## Project

Static HTML/CSS/JS coursework for "Advanced Web Design". No build, no bundler, no transpiler.

- Use **native HTML/CSS/JavaScript** only — no third-party libraries, no CDN, no frameworks (jQuery, Vue, React, etc. are all forbidden).
- Icons MUST use the local `font/` iconfont set (reference `font/iconfont.css` + `font/iconfont.woff2`); Font Awesome, Lucide, or any other icon libraries/CDNs are not allowed.
- Server-side data is fetched via the native `fetch()` API. Do NOT use XMLHttpRequest or jQuery `$.ajax`.
- Open `index.html` directly in a browser — no dev server needed (unless the page uses `fetch`, in which case serve via a local static server to avoid CORS/file:// restrictions).
- Entry point: `index.html` (portfolio grid linking all exercises).
- All pages are self-contained (inline `<style>`). Only `5-1 层叠与继承.html` uses the external `css.css`.
- Some filenames contain Chinese characters — quote paths when referencing them in shell commands.
- No lint, no typecheck, no tests — visual verification in a browser is the only check.

## Conventions

- All CSS class names, ID names, and JS variables must start with `wxy_`.
- Every HTML page must include a header comment with: 姓名：王欣怡 / 日期：<YYYY-MM-DD> / 功能名称：<brief description>.
- Before executing any user request, append the prompt details (timestamp, model, prompt content) to `wang_prompt.md`. Never overwrite existing content.
