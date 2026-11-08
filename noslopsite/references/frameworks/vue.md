---
description: "Vue / Nuxt specific polish guidance."
connections: [rules-performance, rules-architecture]
---

# Vue / Nuxt Guidance

### vue-suspense-and-loading
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Async components need clear loading and error states.  
**How to detect**: Async components with no loading or error handling.  
**How to fix**: Use `<Suspense>` with fallback slots, or Nuxt's built-in loading indicators.

### nuxt-image
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Nuxt Image provides optimization similar to Next.js.  
**How to detect**: Plain `<img>` tags in a Nuxt project that has `@nuxt/image` available.  
**How to fix**: Use `<NuxtImg>` or `<NuxtPicture>` with proper sizes and formats.

### vue-error-handling
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Uncaught errors in components crash the page.  
**How to detect**: No errorCaptured or global error handler.  
**How to fix**: Add error boundaries (via library or Nuxt error.vue) for critical sections.

### vue-lazy-components
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Heavy components should be loaded on demand.  
**How to detect**: All components imported eagerly in large apps.  
**How to fix**: Use `defineAsyncComponent` for non-critical UI.
