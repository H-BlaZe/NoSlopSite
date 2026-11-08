# NoSlopSite

**Turn vibe-coded websites into professional products.**

NoSlopSite is an AI skill that audits your codebase and selectively applies the details that separate polished, professional websites from generic AI-generated ones — design system consistency, accessibility, performance, forms, SEO, and interaction quality.

It doesn’t dump 150 rules at once. It looks at your project, loads only the relevant rules, and gives you a prioritized audit + concrete fixes.

Works with Claude Code, Codex, Grok, OpenCode, Cursor, and other AI coding assistants that support custom skills or instruction files.

## What it fixes

- Generic typography and inconsistent spacing
- Missing focus states, empty states, and loading feedback
- Accessibility gaps (semantic HTML, contrast, labels, keyboard nav)
- Performance issues (images, fonts, Core Web Vitals)
- Weak forms and error handling
- Missing SEO basics (Open Graph, meta tags, structure)
- Unpolished interactions that make sites feel unfinished

## Installation

Clone or download this repo, then copy the `noslopsite` folder into the skills / instructions directory used by your AI assistant.

### Common locations

| Assistant       | Typical install path                          |
|-----------------|-----------------------------------------------|
| **Grok**        | `~/.grok/skills/noslopsite` or `.grok/skills/` |
| **Claude Code** | `~/.claude/skills/noslopsite` or project `.claude/skills/` |
| **Codex**       | Place in your Codex skills / custom instructions folder |
| **OpenCode**    | Copy into OpenCode’s skills or agents directory |
| **Cursor**      | Add as a custom skill or include the folder in project rules |
| **Other**       | Any folder your tool watches for skills, rules, or custom instructions |

```bash
# Example (adjust path for your tool)
git clone https://github.com/H-BlaZe/NoSlopSite.git
cp -r NoSlopSite/noslopsite ~/.your-tool/skills/
```

Restart or reload your assistant if it doesn’t pick up new skills automatically.

## Usage

Just talk to your AI normally. Examples that trigger the skill:

- “Audit this site and make it professional”
- “Fix the polish and accessibility of this React app”
- “This Next.js site feels vibe-coded. Upgrade it.”
- “Improve performance and UX details”
- “What professional details is this frontend missing?”

Or use the recommended prompt in [`examples/recommended-prompt.md`](examples/recommended-prompt.md).

The skill will:
1. Analyze your stack and codebase
2. Load only the relevant rule categories (and framework-specific guidance when it detects Next.js, React+Vite, Tailwind, Vue, etc.)
3. Give you a prioritized audit
4. Provide concrete code fixes for the highest-impact issues
5. Suggest verification steps (Lighthouse, axe, visual/keyboard checks)

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

### Already solid
- Color contrast on primary buttons looks good
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
    ├── rules-*.md
    └── frameworks/       # Next.js, React+Vite, Tailwind, Vue
```

## Contributing

Contributions welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

Good additions:
- More rules with clear detection + fix guidance
- Additional framework examples
- Real before/after case studies

## License

MIT
