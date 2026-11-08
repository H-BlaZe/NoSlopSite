---
description: "Next.js App Router specific polish and performance guidance."
connections: [rules-performance, rules-seo, rules-architecture]
---

# Next.js Guidance

### nextjs-image-component
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: The built-in Image component handles optimization, srcset, and layout shift.  
**How to detect**: Using `<img>` instead of `next/image` for content images.  
**How to fix**: Switch to `next/image` with proper `width`/`height` or `fill` + sizes. Set priority on LCP images.

### nextjs-font-optimization
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: `next/font` avoids layout shift and external requests.  
**How to detect**: Google Fonts linked via `<link>` or external CSS.  
**How to fix**: Use `next/font/google` or `next/font/local` with proper subsets and display settings.

### nextjs-metadata
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: App Router has a built-in Metadata API.  
**How to detect**: Manual `<title>` and meta tags instead of the Metadata export.  
**How to fix**: Use `export const metadata` or `generateMetadata` for titles, descriptions, and Open Graph.

### nextjs-loading-and-error
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: `loading.tsx` and `error.tsx` give consistent states.  
**How to detect**: No loading.tsx or error boundaries at route level.  
**How to fix**: Add `loading.tsx` with skeletons and `error.tsx` with recovery UI.

### nextjs-dynamic-imports
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Heavy components should be code-split.  
**How to detect**: Large client components loaded on every page.  
**How to fix**: Use `next/dynamic` with `ssr: false` where appropriate for non-critical UI.
