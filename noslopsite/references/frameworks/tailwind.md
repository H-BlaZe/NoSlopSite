---
description: "Tailwind CSS specific polish and consistency guidance."
connections: [rules-design, rules-interaction]
---

# Tailwind CSS Guidance

### tailwind-spacing-consistency
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Arbitrary values defeat the purpose of a spacing scale.  
**How to detect**: Heavy use of `p-[13px]`, `mt-[18px]`, etc.  
**How to fix**: Prefer the default scale or extend it in `tailwind.config`. Only use arbitrary values when truly necessary.

### tailwind-focus-visible
**Priority**: critical  
**Applies to**: frontend  
**Why it matters**: Default focus styles are often removed.  
**How to detect**: `outline-none` without a replacement focus style.  
**How to fix**: Use `focus-visible:ring-2 focus-visible:ring-offset-2` (or equivalent) on interactive elements.

### tailwind-design-tokens
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Hardcoded colors make dark mode and theming harder.  
**How to detect**: Many raw hex/rgb values instead of theme colors.  
**How to fix**: Extend the theme with semantic colors and use those classes.

### tailwind-component-extraction
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Repeated long class strings become hard to maintain.  
**How to detect**: Identical long class strings copied across components.  
**How to fix**: Extract to components or use `@apply` sparingly for true design system primitives.

### tailwind-reduced-motion
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Animations should respect user preference.  
**How to detect**: `animate-*` or transition classes with no motion-reduce variant.  
**How to fix**: Use `motion-reduce:animate-none` or `motion-reduce:transition-none` where appropriate.
