---
description: "React + Vite specific polish guidance."
connections: [rules-performance, rules-architecture]
---

# React + Vite Guidance

### vite-code-splitting
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Vite supports dynamic imports out of the box.  
**How to detect**: All routes and heavy components imported statically.  
**How to fix**: Use `React.lazy` + `Suspense` or dynamic `import()` for route-level and heavy components.

### vite-image-handling
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: No built-in image optimizer like Next.js.  
**How to detect**: Large unoptimized images in public/.  
**How to fix**: Use a tool like vite-imagetools, or optimize images ahead of time (WebP/AVIF + srcset).

### vite-env-and-base
**Priority**: low  
**Applies to**: frontend  
**Why it matters**: Correct base path and env handling prevents broken assets.  
**How to detect**: Hardcoded absolute paths that break on deploy.  
**How to fix**: Use `import.meta.env` and Vite's base config correctly.

### react-error-boundaries
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: One bad component shouldn't crash the app.  
**How to detect**: No error boundaries around data-fetching or third-party components.  
**How to fix**: Wrap risky trees with error boundaries that show a friendly fallback.
