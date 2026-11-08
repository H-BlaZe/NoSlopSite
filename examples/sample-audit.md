# Example Audit

This is what a typical NoSlopSite audit looks like on a vibe-coded React + Tailwind site.

## Critical
- **Missing focus-visible styles** — All interactive elements have `outline: none` with no replacement. Keyboard users get no indication of focus.
- **Images not optimized** — Hero and product images are large PNGs with no `srcset`, no modern formats, and no lazy loading.

## High Priority
- **Placeholder-only form labels** — Inputs rely solely on placeholders. This fails accessibility and UX.
- **No empty states** — Lists and tables just render nothing when empty.
- **Inconsistent spacing** — Mix of arbitrary values (13px, 18px, 22px) instead of a spacing scale.
- **Generic spinners** — Data loads use a centered spinner instead of skeleton loaders.

## Medium
- **No Open Graph tags** — Sharing links shows no preview image or description.
- **Missing reduced-motion support** — Animations ignore `prefers-reduced-motion`.

## Suggested next step
Fix the Critical and High items first. They give the biggest jump in perceived quality.
