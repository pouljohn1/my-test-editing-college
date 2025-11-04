# AGENTS.md

## Project Overview

This is a college learning platform template using MDX for content. The site includes courses (with optional modules), guides, and a home page.

## Project Structure

```
/
├── home.mdx              # Landing page
├── readme.mdx            # Project readme
├── courses/              # All courses
│   └── [course-name]/
│       ├── index.mdx     # Course metadata & description
│       └── *.mdx         # Chapter files
├── guides/               # Standalone guides
│   └── *.mdx
└── assets/               # Images and media (16:9 banners)
```

## Creating Content

### Adding a New Course

1. Create directory: `courses/your-course-name/`
2. Create `index.mdx` with required frontmatter:
```yaml
---
title: Your Course Title
description: Brief description of what students will learn
banner: ../assets/your-banner.png  # optional, 16:9 aspect ratio
---

Brief course introduction goes here.
```

3. Add chapter files: `1-intro.mdx`, `2-concepts.mdx`, etc.

### Adding a New Guide

Create `guides/your-guide.mdx`:
```yaml
---
title: Your Guide Title
description: What this guide teaches
banner: ../assets/guide-banner.png  # optional, 16:9 aspect ratio
---

Guide content here.
```

### Adding Chapter Content

Chapter files only need a title:
```yaml
---
title: Chapter Name
---

# Chapter Name

Your content here.
```

## Frontmatter Requirements

| File Type | Required Fields | Optional Fields |
|-----------|----------------|-----------------|
| Course index | `title`, `description` | `banner` |
| Guide | `title`, `description` | `banner` |
| Chapter | `title` | none |

## Banner Images

Banners appear on the feed page (16:9 aspect ratio recommended).

**Supported formats:** png, jpg, jpeg, webp

**Path options:**
- Relative: `../assets/filename.png` or `assets/filename.jpg`
- Absolute URL: `https://example.com/image.png`
- File must exist in `/assets` directory if using relative path

## Content Style Guide

- Use simple, concise English 📝
- Add some emojis where appropriate 😊
- Write in markdown but avoid excessive **bold** or *italic*
- Keep explanations clear and student-friendly
- Break complex topics into digestible sections

## Course Organization Options

**Simple course:** Chapters directly in course folder
```
courses/intro-to-python/
  ├── index.mdx
  ├── 1-basics.mdx
  └── 2-variables.mdx
```

**Course with modules:** Group chapters in module folders
```
courses/web-development/
  ├── index.mdx
  ├── 1-html-basics/
  │   ├── index.mdx
  │   ├── 1-structure.mdx
  │   └── 2-elements.mdx
  └── 2-css-styling/
      ├── 3-selectors.mdx
      └── 4-layout.mdx
```

## Special Components

Use the Woz component for interactive learning checks:

```mdx
<Woz 
title="Recap" 
description="Make sure you really understand 🙃" 
prompt="Ask me 3 questions about this chapter to test my understanding."
/>
```

With custom placeholder:
```mdx
<Woz 
title="Context" 
description="Apply what you learned" 
context="User is learning about web basics"
prompt=""
placeholder="Describe your understanding here"
/>
```

## Common Tasks

**Add a new course:**
```bash
mkdir -p courses/my-course
touch courses/my-course/index.mdx
touch courses/my-course/1-intro.mdx
```

**Add a banner image:**
```bash
# Place image in assets/
cp your-image.png assets/
# Reference in frontmatter as: ../assets/your-image.png
```

## File Naming Conventions

- Use lowercase with hyphens: `intro-to-python`, `web-basics`
- Number chapters for ordering: `1-intro.mdx`, `2-advanced.mdx`
- Use descriptive names: `setting-up-environment.mdx` not `setup.mdx`
- Keep names concise but clear

## Quality Checklist

Before committing new content:
- [ ] Frontmatter includes all required fields
- [ ] Banner image exists if referenced
- [ ] Content uses appropriate headers (start with `#`)
- [ ] Style follows guidelines (simple English, some emojis)
- [ ] Code examples use proper syntax highlighting
- [ ] Links are working and properly formatted