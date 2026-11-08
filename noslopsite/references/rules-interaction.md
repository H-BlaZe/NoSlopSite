---
description: "Interaction states, feedback, loading, empty states, micro-interactions, and keyboard behavior."
connections: [rules-design, rules-a11y, rules-forms]
---

# Interaction Rules

### interaction-distinct-states
**Priority**: critical  
**Applies to**: frontend  
**Why it matters**: Buttons and links with identical hover/focus/active states feel broken.  
**How to detect**: No `:hover`, `:focus-visible`, or `:active` styles, or they all look the same.  
**How to fix**: Define clear visual differences for default, hover, focus-visible, active, and disabled.

### interaction-skeleton-loaders
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Generic spinners feel cheap; skeletons feel intentional.  
**How to detect**: Full-page or component spinners on data loads.  
**How to fix**: Create skeleton components that match the shape of the real content.

### interaction-empty-states
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Blank screens confuse users.  
**How to detect**: No content when lists/tables are empty.  
**How to fix**: Add helpful empty state with illustration or icon + message + primary action.

### interaction-optimistic-ui
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Instant feedback makes apps feel fast.  
**How to detect**: UI only updates after server response.  
**How to fix**: Update UI immediately, then reconcile or rollback on error.

### interaction-loading-states-match-content
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Prevents layout shift and feels more polished.  
**How to detect**: Loaders that don't match the size/shape of content.  
**How to fix**: Use skeletons or placeholders that reserve the correct space.

### interaction-toast-system
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Browser alerts are unprofessional.  
**How to detect**: `alert()`, `confirm()`, or no feedback system.  
**How to fix**: Implement a toast/notification system with proper queuing and accessibility.

### interaction-undo-destructive
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Prevents accidental data loss.  
**How to detect**: Delete actions with only a confirm dialog.  
**How to fix**: Prefer soft delete + undo toast, or clear confirmation with specific copy.

### interaction-keyboard-shortcuts
**Priority**: low  
**Applies to**: frontend (apps)  
**Why it matters**: Power users expect them.  
**How to detect**: No keyboard shortcuts in complex UIs.  
**How to fix**: Add common shortcuts (e.g. Cmd+K command palette) and make them discoverable.

### interaction-command-palette
**Priority**: medium  
**Applies to**: frontend (apps)  
**Why it matters**: Modern apps almost all have one.  
**How to detect**: Complex navigation with no quick jump.  
**How to fix**: Implement Cmd/Ctrl+K palette for navigation and actions.

### interaction-focus-visible
**Priority**: critical  
**Applies to**: frontend  
**Why it matters**: Keyboard users need clear focus indicators.  
**How to detect**: `outline: none` without replacement, or focus styles that are invisible.  
**How to fix**: Use `:focus-visible` with a clear ring that meets contrast requirements.
