---
description: "Accessibility rules covering semantic HTML, focus management, contrast, ARIA, and WCAG compliance."
connections: [rules-forms, rules-interaction]
---

# Accessibility Rules

### a11y-semantic-html
**Priority**: critical  
**Applies to**: frontend  
**Why it matters**: Screen readers and SEO depend on proper structure.  
**How to detect**: Everything is `<div>` and `<span>`, no `<button>`, `<nav>`, `<main>`, `<article>`.  
**How to fix**: Use semantic elements. Buttons for actions, links for navigation.

### a11y-heading-hierarchy
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Screen reader users navigate by headings.  
**How to detect**: Skipped heading levels (h1 → h3) or multiple h1s without reason.  
**How to fix**: Maintain logical heading order. One h1 per page usually.

### a11y-color-contrast
**Priority**: critical  
**Applies to**: frontend  
**Why it matters**: WCAG AA requires 4.5:1 for normal text.  
**How to detect**: Light gray text on white, low contrast buttons.  
**How to fix**: Audit with tools (axe, WAVE, or browser devtools). Adjust colors.

### a11y-focus-management
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Modals and dynamic content must manage focus.  
**How to detect**: Focus escapes modals or gets lost after actions.  
**How to fix**: Trap focus in modals, return focus on close, move focus to new content when appropriate.

### a11y-aria-live
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Dynamic updates need to be announced.  
**How to detect**: Status messages or errors that appear without announcement.  
**How to fix**: Use `aria-live="polite"` or `assertive` for important updates.

### a11y-skip-link
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Keyboard users shouldn't have to tab through entire nav.  
**How to detect**: No skip to main content link.  
**How to fix**: Add a visually hidden skip link that becomes visible on focus.

### a11y-form-labels
**Priority**: critical  
**Applies to**: frontend  
**Why it matters**: Every input needs a proper label.  
**How to detect**: Placeholder-only inputs, missing `<label>` or `aria-label`.  
**How to fix**: Always associate labels with inputs via `for`/`id` or wrapping.

### a11y-touch-targets
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Mobile users need large enough targets.  
**How to detect**: Buttons or links smaller than 44×44px.  
**How to fix**: Ensure interactive elements meet minimum size, use padding if needed.

### a11y-reduced-motion
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Some users get motion sick.  
**How to detect**: Animations without reduced motion support.  
**How to fix**: Respect `prefers-reduced-motion`.

### a11y-alt-text
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Images need descriptions or empty alt for decorative.  
**How to detect**: Missing `alt` attributes.  
**How to fix**: Provide meaningful alt text or `alt=""` for decorative images.
