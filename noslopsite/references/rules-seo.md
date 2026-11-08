---
description: "SEO rules including meta tags, structured data, Open Graph, sitemaps, and technical SEO."
connections: [rules-performance]
---

# SEO Rules

### seo-meta-tags
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Title and description affect click-through rates.  
**How to detect**: Missing or duplicate title/description, generic "Home".  
**How to fix**: Unique, descriptive titles (50–60 chars) and meta descriptions (150–160 chars) per page.

### seo-open-graph
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Controls how links look when shared.  
**How to detect**: No og:title, og:description, og:image.  
**How to fix**: Add complete Open Graph and Twitter Card meta tags with proper images (1200×630).

### seo-structured-data
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Enables rich results in search.  
**How to detect**: No JSON-LD for Organization, Product, Article, FAQ, etc.  
**How to fix**: Add appropriate schema.org JSON-LD.

### seo-canonical
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Prevents duplicate content issues.  
**How to detect**: No canonical tags.  
**How to fix**: Add `<link rel="canonical">` pointing to the preferred URL.

### seo-sitemap-robots
**Priority**: medium  
**Applies to**: full-stack  
**Why it matters**: Helps search engines discover and index content.  
**How to detect**: Missing sitemap.xml or robots.txt.  
**How to fix**: Generate and maintain sitemap, configure robots.txt properly.

### seo-semantic-structure
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Helps both SEO and accessibility.  
**How to detect**: Poor heading structure, missing main landmark.  
**How to fix**: Use proper heading hierarchy and semantic landmarks.

### seo-image-alt
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Images can rank and help accessibility.  
**How to detect**: Missing or empty alt on content images.  
**How to fix**: Write descriptive alt text for meaningful images.

### seo-performance
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Page speed is a ranking factor.  
**How to detect**: Poor Core Web Vitals.  
**How to fix**: See performance rules.
