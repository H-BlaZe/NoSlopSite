---
description: "Index of all professional website polish rules. Start here to choose which category files to load."
---

# NoSlopSite Knowledge Graph

Use this index to decide which rule files to load based on the codebase and user request.

## Categories

- [[rules-design]] — Typography, spacing, visual consistency, icons, imagery, motion
- [[rules-interaction]] — States, feedback, micro-interactions, loading, empty states, keyboard
- [[rules-a11y]] — Semantic HTML, focus, contrast, ARIA, screen readers, WCAG
- [[rules-performance]] — Core Web Vitals, images, fonts, loading, caching, bundle size
- [[rules-seo]] — Meta tags, structured data, sitemaps, Open Graph, technical SEO
- [[rules-forms]] — Labels, validation, errors, autofill, multi-step, accessibility
- [[rules-architecture]] — Error handling, state management, deep linking, reliability, progressive enhancement

## Quick Selection

| User intent / detected focus | Load these |
|------------------------------|------------|
| Overall polish / "make it professional" | design, interaction, a11y |
| Performance / speed / Core Web Vitals | performance, architecture |
| Accessibility / WCAG | a11y, forms |
| SEO / marketing site | seo, performance, design |
| Forms / checkout / auth | forms, a11y, interaction |
| Full audit | All (but still prioritize) |

## Rule Format

Each rule file contains entries with:
- **ID**
- **Title**
- **Priority** (critical / high / medium / low)
- **Applies to** (frontend, backend, full-stack, etc.)
- **Why it matters**
- **How to detect**
- **How to fix**
- Optional examples
