# Repository Guidelines

## Project Overview

A self-paced DevOps curriculum — 16 Chinese-language lessons from fundamentals (Linux CLI, Git, Docker, CI/CD, IaC, monitoring) through advanced topics (Linux troubleshooting, networking, Kubernetes production). Pure static HTML with inline CSS/JS; no build step, no framework, no package manager.

**Audience**: A frontend developer with partial backend experience, zero DevOps background, transitioning toward DevOps/SRE roles.

## Architecture & Data Flow

```
index.html (course catalog + dependency graph)
  ├── lessons/0001-0016.html   ← self-contained lesson pages
  ├── reference/glossary.html  ← 100+ term DevOps glossary
  ├── reference/linux-cheatsheet.html ← categorized command reference
  ├── assets/style.css         ← single shared stylesheet
  ├── MISSION.md               ← learning goals & constraints
  ├── RESOURCES.md             ← curated external links
  ├── NOTES.md                 ← teaching notes & infrastructure config
  └── learning-records/        ← adr-style progress markdown files
```

- `index.html` is the entry point — renders the full course catalog with a text-art dependency graph and lesson cards.
- Each lesson is a standalone HTML page with no shared JS modules; quizzes use inline `<script>` blocks.
- `assets/style.css` is the sole stylesheet, shared across all pages via `<link rel="stylesheet" href="../assets/style.css">`.
- Learning records (`learning-records/000N-*.md`) track the student's progress and prior knowledge.

## Key Directories

| Directory | Purpose |
|-----------|---------|
| `lessons/` | 16 numbered lesson files (`0001`–`0016`), self-contained HTML |
| `reference/` | Supplementary reference pages (glossary, cheatsheet) |
| `assets/` | Single shared stylesheet (`style.css`) |
| `learning-records/` | Student progress tracking in adr-style markdown |

## Development Commands

There are **no build, test, lint, or run commands**. This is static HTML.

- **Preview locally**: Open `index.html` in a browser, or `python3 -m http.server 8000` and visit `http://localhost:8000`.
- **Deploy**: Copy files to any static host (Nginx, GitHub Pages, VPS). The course references a RackNerd VPS (2 vCPU / 2GB RAM, Ubuntu 22.04) for student exercises.

## Code Conventions & Common Patterns

### HTML Structure
```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lesson NNNN — Topic</title>
<link rel="stylesheet" href="../assets/style.css">
<!-- Page-specific <style> block for unique components only -->
</head>
<body>
  <!-- Lesson content: h1, h2, h3, p, pre>code, table, ul/ol, blockquote -->
  <!-- Interactive quiz with inline <script> -->
  <!-- Footer: .cite div with nav links -->
</body>
</html>
```

### Content Conventions
- **Language**: Simplified Chinese (zh-CN). Technical terms keep English originals with Chinese explanations in parentheses — avoid translation ambiguity (e.g., "Pod（最小调度单元）").
- **Lesson structure** (canonical order): `h1` title → theory sections (`h2`) → hands-on exercise with copy-paste commands → quiz (`<form id="quiz" onsubmit="return checkQuiz(event)">`) → recommended resources → next/prev lesson links in `.cite` footer.
- **Callout classes**: `.note` (info callout, prefix "💡"), `.tip` (actionable tip), `.cite` (footer navigation, smaller muted text).
- **Code blocks**: Always `<pre><code>...</code></pre>` — no syntax highlighting, no external JS library for it.

### CSS
- **Design system**: Tufte-inspired — clean, readable, print-friendly. CSS custom properties define the palette in `:root` (see `assets/style.css`).
- **Fonts**: Inter (body), JetBrains Mono (code), Noto Sans SC (Chinese) — loaded via Google Fonts `@import`.
- **Page-specific styles** go in a `<style>` block in `<head>`, NOT in `style.css`. The shared stylesheet covers typography, code blocks, blockquotes, tables, lists, and utility classes only.

### Quiz Pattern
Every lesson has an inline quiz. The canonical pattern:
```html
<form id="quiz" onsubmit="return checkQuiz(event)">
  <fieldset>...</fieldset>
  <button type="submit">检查答案</button>
</form>
<div id="quiz-result" style="margin-top:1rem;"></div>

<script>
function checkQuiz(e) {
  e.preventDefault();
  const answers = { q1: 'c', q2: 'b', /* ... */ };
  let correct = 0, feedback = [];
  for (const [q, a] of Object.entries(answers)) {
    const sel = document.querySelector(`input[name="${q}"]:checked`);
    if (!sel) feedback.push(q + ': 未作答');
    else if (sel.value === a) { correct++; feedback.push(q + ': ✓ 正确'); }
    else feedback.push(q + ': ✗ 错误');
  }
  const pct = Math.round(correct / Object.keys(answers).length * 100);
  // render result into #quiz-result with success/warn background
}
</script>
```

### Learning Records
- Named `learning-records/NNNN-slug.md` (adr-style zero-padded numbering).
- Format: `# Title`, followed by narrative text, followed by `**Evidence:**` line.
- Track student milestones: prior knowledge assessment → course completions → plan decisions.

## Important Files

| File | Role |
|------|------|
| `index.html` | Course catalog entry point, dependency graph, lesson navigation |
| `assets/style.css` | Single shared stylesheet for all pages |
| `lessons/0001-what-is-devops.html` | First lesson — establishes the course pattern |
| `reference/glossary.html` | 100+ term glossary (Chinese + English), organized by domain |
| `NOTES.md` | Teaching preferences (language, style, pacing) and infrastructure details |
| `MISSION.md` | Student's learning objectives, constraints, scope boundary |
| `RESOURCES.md` | External links organized as Knowledge / Wisdom / Gaps |

## Runtime/Tooling Preferences

- **No runtime**: Static HTML. No Node.js, no Bun, no framework.
- **No package manager**: No `package.json`, no npm/pnpm/yarn.
- **No build step**: Files are served as-is. No bundler, no minification, no transpilation.
- **No test framework**: Quizzes are self-contained inline JS with no test runner.
- **Student's exercise environment** (from `NOTES.md`): Ubuntu 22.04, Docker 29.6.2, Bash, SSH ed25519 keys, kind for K8s, RackNerd VPS (2 vCPU / 2GB RAM).
- **Browser**: Any modern browser. Pages use no ES modules, no JSX, no framework — vanilla HTML/CSS/JS only.

## Testing & QA

There is no automated test suite. Manual QA checklist when authoring or editing a lesson:
1. Open the lesson HTML directly in a browser.
2. Verify all internal links (prev/next lesson, glossary, cheatsheet, index) resolve correctly.
3. Complete the quiz — confirm all answers register and the score renders with correct styling.
4. Check that `<pre><code>` blocks render with proper monospace font and wrapping.
5. Run `grep -r "assets/style.css" lessons/` — every lesson must link the shared stylesheet.
6. Verify Chinese text renders correctly (no mojibake, proper Noto Sans SC fallback).
7. Print-preview check: `@media print` rules in `style.css` should produce readable output.
