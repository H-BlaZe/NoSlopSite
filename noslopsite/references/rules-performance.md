---
description: "Performance rules for Core Web Vitals, images, fonts, loading strategies, and optimization."
connections: [rules-architecture, rules-seo]
---

# Performance Rules

### perf-core-web-vitals
**Priority**: critical  
**Applies to**: frontend  
**Why it matters**: LCP, INP, and CLS directly affect user experience and SEO.  
**How to detect**: Slow LCP, layout shifts, or sluggish interactions.  
**How to fix**: Measure with Lighthouse or Web Vitals. Optimize images, fonts, and JS.

### perf-image-optimization
**Priority**: critical  
**Applies to**: frontend  
**Why it matters**: Images are usually the biggest payload.  
**How to detect**: Large unoptimized images, no WebP/AVIF, missing srcset.  
**How to fix**: Use modern formats, responsive images with srcset/sizes, lazy load below-fold.

### perf-font-loading
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Fonts cause layout shift and delay text rendering.  
**How to detect**: FOIT/FOUT, missing font-display, no preloading.  
**How to fix**: Use `font-display: swap` or `optional`, preload critical fonts, subset if possible.

### perf-lazy-loading
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Don't load everything upfront.  
**How to detect**: All images and components load immediately.  
**How to fix**: Lazy load images (`loading="lazy"`), code-split routes and heavy components.

### perf-code-splitting
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Large JS bundles hurt INP and initial load.  
**How to detect**: Single large bundle or no dynamic imports.  
**How to fix**: Use route-based code splitting and dynamic `import()` for heavy features.

### perf-critical-css
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Render-blocking CSS delays LCP.  
**How to detect**: Large CSS files blocking first paint.  
**How to fix**: Inline critical CSS, defer non-critical.

### perf-resource-hints
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Preconnect and preload improve perceived performance.  
**How to detect**: No `<link rel="preconnect">` or preload for critical resources.  
**How to fix**: Preconnect to font/CDN origins, preload hero images and critical fonts.

### perf-no-layout-shift
**Priority**: critical  
**Applies to**: frontend  
**Why it matters**: CLS is a Core Web Vital.  
**How to detect**: Content jumping when images/fonts load.  
**How to fix**: Set explicit dimensions on images/videos, reserve space for dynamic content.

### perf-third-party-scripts
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Third-party scripts are a common performance killer.  
**How to detect**: Many analytics, chat, or marketing scripts.  
**How to fix**: Audit and remove unnecessary ones. Load non-critical scripts deferred or after interaction.

### perf-caching-headers
**Priority**: medium  
**Applies to**: full-stack  
**Why it matters**: Proper caching reduces repeat load times.  
**How to detect**: No Cache-Control headers on static assets.  
**How to fix**: Set long-lived cache headers for hashed assets, shorter for HTML.
