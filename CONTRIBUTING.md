## 🧭 Contributing
Welcome to Homebrew Hackers College Template.
This repo powers your college content on the platform. Keep it simple, structured, and useful.

### ⚙️ How to Contribute
- **Fork + clone the repo**

```bash
git clone https://github.com/<your-username>/college-template.git
cd college-template
```

- **Create a branch for your change**

```bash
git checkout -b content/<your-slug>
```

- **Add or edit files**
  - `courses/<course>/index.mdx` → course overview
  - `courses/<course>/chapter-x.mdx` → chapters
  - `guides/<slug>.mdx` → standalone guides
  - `assets/` → images or diagrams

- **Commit + push**

```bash
git commit -m "content: add guide on AI workflows"
git push origin content/<your-slug>
```

- **Open a Pull Request** with a short, clear title.

### 🧱 Rules
- **Use kebab-case** for folders/files.
- **Each `.mdx` file must include frontmatter:**

```yaml
---
title: Short and clear
description: One-sentence summary
---
```

- **Use Markdown + MDX.** Include language tags on code blocks.
- **Images** go in `assets/` and use relative paths.

### 🧠 Writing Style
- Write like you talk — no academic tone.
- Show first, explain after.
- One topic = one file.
- Keep chapters short.
- Examples > theory.

### 🪞 Review Checklist
- [ ] Correct folder structure
- [ ] Valid frontmatter
- [ ] Optimized images with alt text
- [ ] Working links
- [ ] Clear, concise copy

### ⚖️ License
By contributing, you agree your work follows this repo’s license.
