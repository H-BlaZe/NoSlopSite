# NoSlopSite

**Turn vibe-coded websites into professional products.**

NoSlopSite is an AI skill that audits your codebase and selectively applies the details that separate polished, professional websites from generic AI-generated ones — design system consistency, accessibility, performance, forms, SEO, and interaction quality.

It doesn’t dump 150 rules at once. It looks at your project, loads only the relevant rules, and gives you a prioritized audit + concrete fixes.

## What it fixes

- Generic typography and inconsistent spacing
- Missing focus states, empty states, and loading feedback
- Accessibility gaps (semantic HTML, contrast, labels, keyboard nav)
- Performance issues (images, fonts, Core Web Vitals)
- Weak forms and error handling
- Missing SEO basics (Open Graph, meta tags, structure)
- Unpolished interactions that make sites feel unfinished

## Installation

1. Clone or download this repo
2. Copy the `noslopsite` folder into your skills directory:

```bash
# Example locations (adjust to your setup)
cp -r noslopsite ~/.grok/skills/
# or
cp -r noslopsite .grok/skills/
# or wherever your AI coding tool loads skills from
```

3. Restart or reload your AI tool if needed.

## Usage

Just talk to your AI normally. Examples that trigger the skill:

- “Audit this site and make it professional”
- “Fix the polish and accessibility of this React app”
- “This Next.js site feels vibe-coded. Upgrade it.”
- “Improve performance and UX details”
- “What professional details is this frontend missing?”

The skill will:
1. Analyze your stack and codebase
2. Load only the relevant rule categories
3. Give you a prioritized audit
4. Provide concrete code fixes for the highest-impact issues

## Example output

```
## Professional Polish Audit

### Critical
- Missing focus-visible styles — Keyboard users have no visible focus
- Images not optimized — Large PNGs with no srcset or modern formats

### High Priority
- No empty states on lists
- Form inputs using placeholder as label
- Inconsistent spacing system
...
```

## Structure

```
noslopsite/
├── SKILL.md              # Main workflow
├── CHANGELOG.md
├── evals/
└── references/
    ├── INDEX.md
    ├── rules-design.md
    ├── rules-interaction.md
    ├── rules-a11y.md
    ├── rules-performance.md
    ├── rules-seo.md
    ├── rules-forms.md
    └── rules-architecture.md
```

## Contributing

Contributions welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

Good additions:
- More rules with clear detection + fix guidance
- Stack-specific examples (Next.js, Tailwind, Vue, etc.)
- Real before/after case studies

## License

MIT
