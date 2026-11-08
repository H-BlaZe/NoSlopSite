---
name: noslopsite
description: "Upgrade vibe-coded websites to professional quality. Use when auditing or improving a website's design polish, accessibility, performance, UX details, SEO, forms, or overall professional feel. Analyzes the codebase and applies only relevant rules."
type: workflow
lifecycle: active
---

# NoSlopSite — Professional Website Upgrade Skill

Turn vibe-coded sites into polished, professional products by selectively applying proven rules for design, UX, accessibility, performance, and reliability.

## When to Use

Trigger on requests like:
- "Make this site look and feel professional"
- "Audit my vibe-coded website"
- "Fix the polish / accessibility / performance of this frontend"
- "Upgrade this Next.js / React / HTML site to production quality"
- "What professional details is this site missing?"

## Workflow

1. **Analyze the project**
   - Detect stack: look at `package.json`, framework files, language (React, Next.js, Vue, Svelte, Astro, plain HTML/CSS/JS, etc.).
   - Identify scope: frontend-only, full-stack, marketing site, web app, admin dashboard.
   - Scan key areas: components, styles, forms, layout, SEO meta, error handling, loading states.
   - Note any existing design system, spacing scale, or deliberate patterns that should be preserved.

2. **Select relevant rules**
   - Read `references/INDEX.md` for the rule categories.
   - Load only the category files that match the detected stack and user request.
   - Load framework-specific guidance from `references/frameworks/` when applicable (e.g. nextjs.md, react-vite.md, tailwind.md, vue.md).
   - Filter rules by `applies_to` and priority.
   - Default to top critical + high priority issues (aim for 10–20 concrete items unless user asks for full audit).

3. **Produce phased output**
   - **Phase 1 — Audit**: Short prioritized list of missing professional details found in this codebase. Group by category. Include severity and note anything that is already working well.
   - **Phase 2 — Fixes**: Concrete code changes, component improvements, or CSS/HTML patches for the highest-impact items. Prefer actual code over vague advice. Propose changes before large architectural modifications.
   - **Phase 3 — Verification**: Suggest or run available checks (Lighthouse, axe-core, Playwright visual/keyboard tests). Do not claim performance or accessibility improvements without measurement or testing evidence.
   - **Phase 4 — Optional deeper**: Offer next steps (e.g. design system, performance budget, full a11y pass).

4. **Principles**
   - Prefer fixing over listing.
   - Keep changes minimal and focused — don’t rewrite the entire app.
   - Respect existing design language; enhance rather than replace unless it’s broken. Do not blindly enforce generic systems (e.g. force an 8px grid) if a deliberate system already exists.
   - Do not introduce unnecessary dependencies.
   - Always consider accessibility and performance alongside visual polish.
   - Preserve the product’s identity. The goal is production quality, not making every site look the same.

## Rule Selection Guidance

| Scope detected | Priority categories to load |
|----------------|-----------------------------|
| Frontend / UI  | design, interaction, a11y, performance, forms |
| Marketing site | design, seo, performance, a11y, content |
| Web app        | interaction, forms, a11y, architecture, performance |
| Full-stack     | All relevant + backend reliability rules |
| User says "polish" | design + interaction + a11y |
| User says "performance" | performance + architecture |
| User says "accessible" | a11y + forms |

## Knowledge Graph

Start at `references/INDEX.md`.

Load individual rule files only when needed:
- `references/rules-design.md`
- `references/rules-interaction.md`
- `references/rules-a11y.md`
- `references/rules-performance.md`
- `references/rules-seo.md`
- `references/rules-forms.md`
- `references/rules-architecture.md`

Framework-specific guidance (load when stack matches):
- `references/frameworks/nextjs.md`
- `references/frameworks/react-vite.md`
- `references/frameworks/tailwind.md`
- `references/frameworks/vue.md`

## Output Format

### Audit Report
```
## Professional Polish Audit

### Critical
- [Rule] — Why it matters here + quick fix direction

### High Priority
...

### Already solid
- [What is already good and should be preserved]
```

### Fixes
Provide ready-to-apply code snippets or clear patch instructions for the top items. Propose substantial changes before implementing them.

### Verification
List concrete next checks (Lighthouse, axe, visual regression, keyboard testing) and only claim success when evidence supports it.

