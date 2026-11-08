---
description: "Design system, typography, spacing, visual consistency, icons, imagery, and motion rules."
connections: [rules-interaction, rules-a11y]
---

# Design Rules

### design-typography-system
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Default system fonts or random Google Fonts with no hierarchy make sites look unfinished.  
**How to detect**: Single font family, no size/weight scale, or heavy use of browser defaults.  
**How to fix**: Define a type scale (e.g. 12/14/16/20/24/32/40), choose 1–2 font families max, set proper line-heights and letter-spacing.

### design-spacing-system
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Random margins and paddings create visual chaos.  
**How to detect**: Inconsistent spacing values (7px, 13px, 18px, etc.).  
**How to fix**: Adopt a 4px or 8px base unit. Use CSS variables or Tailwind spacing scale consistently.

### design-icon-system
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Mixed icon libraries or inconsistent stroke widths look amateur.  
**How to detect**: Multiple icon packages or inline SVGs with different styles.  
**How to fix**: Pick one icon set (Lucide, Heroicons, Phosphor, etc.) and use it exclusively. Match stroke width to design.

### design-color-system
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Random hex colors and missing semantic tokens break consistency and dark mode.  
**How to detect**: Hardcoded colors everywhere, no CSS variables for colors.  
**How to fix**: Create design tokens for primary, secondary, neutral, success, error, warning. Support light/dark if relevant.

### design-consistent-radius-shadow
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Mixed border radii and shadows destroy visual cohesion.  
**How to detect**: Cards with 4px, 8px, 12px, 16px radii mixed; random box-shadows.  
**How to fix**: Define 2–3 radius tokens and 2–3 elevation shadows. Apply consistently.

### design-no-stock-photos
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Generic stock photos scream "template".  
**How to detect**: Unsplash or obvious stock imagery.  
**How to fix**: Use custom photography, high-quality illustrations, or abstract graphics that match the brand.

### design-intentional-whitespace
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Cramped layouts feel cheap.  
**How to detect**: Elements jammed together, little breathing room between sections.  
**How to fix**: Increase section padding, use generous vertical rhythm, let content breathe.

### design-optical-alignment
**Priority**: low  
**Applies to**: frontend  
**Why it matters**: Pixel-perfect alignment is the difference between good and great.  
**How to detect**: Icons or text that look slightly off.  
**How to fix**: Manually adjust optical alignment for icons next to text, buttons, etc.

### design-reduced-motion
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Required for accessibility and good UX.  
**How to detect**: Animations with no `prefers-reduced-motion` media query.  
**How to fix**: Wrap non-essential animations in `@media (prefers-reduced-motion: no-preference)`.

### design-custom-selection
**Priority**: low  
**Applies to**: frontend  
**Why it matters**: Small brand detail that feels polished.  
**How to detect**: Default blue text selection.  
**How to fix**: Style `::selection` with brand colors.
