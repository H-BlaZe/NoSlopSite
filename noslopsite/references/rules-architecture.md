---
description: "Architecture, reliability, error handling, progressive enhancement, and deep linking rules."
connections: [rules-performance, rules-interaction]
---

# Architecture Rules

### arch-error-boundaries
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: One broken component shouldn't crash the whole app.  
**How to detect**: No error boundaries in React or equivalent.  
**How to fix**: Add error boundaries with friendly fallback UI.

### arch-graceful-degradation
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Site should work without JS for core content.  
**How to detect**: Completely broken without JavaScript.  
**How to fix**: Ensure critical content is in HTML, enhance with JS.

### arch-deep-linking
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Users should be able to share specific views.  
**How to detect**: UI state not reflected in URL.  
**How to fix**: Sync filters, tabs, modals, and pagination to the URL.

### arch-back-button
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Back button must work as expected.  
**How to detect**: History broken by SPA routing or modals.  
**How to fix**: Properly manage history for modals and navigation.

### arch-optimistic-with-rollback
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Fast UI with correct error recovery.  
**How to detect**: Optimistic updates that don't handle failure.  
**How to fix**: Update UI immediately, then rollback and show error if request fails.

### arch-idempotent-actions
**Priority**: medium  
**Applies to**: full-stack  
**Why it matters**: Safe retries prevent duplicate actions.  
**How to detect**: Non-idempotent POST endpoints for create/update.  
**How to fix**: Design mutations to be safely retryable.

### arch-loading-error-empty
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Every data fetch needs three states.  
**How to detect**: Missing loading, error, or empty handling.  
**How to fix**: Always handle loading, success, error, and empty for async data.

### arch-feature-flags
**Priority**: low  
**Applies to**: full-stack  
**Why it matters**: Enables safe rollouts.  
**How to detect**: Hardcoded features with no toggle.  
**How to fix**: Introduce feature flags for new or risky features.

### arch-offline-tolerant
**Priority**: low  
**Applies to**: frontend  
**Why it matters**: Better resilience.  
**How to detect**: Complete failure when offline.  
**How to fix**: Cache critical assets, show offline UI, queue actions if appropriate.

### arch-proper-404
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Custom 404s feel professional.  
**How to detect**: Default server 404 page.  
**How to fix**: Create a branded 404 page with helpful navigation.
