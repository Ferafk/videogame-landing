# Portfolio Astro Performance Guidelines

## Objective
Achieve 100 in web performance metrics. Static site, minimal JS, fast loading.

## Architecture
- Atomic design: atoms, molecules, organisms, templates, pages in src/components/
- Centralize all data in src/data/*.ts - no hardcoded arrays/text in components
- No repeated HTML - use components and slots
- Max 6 props per component
- Prefer slots over excessive props

## Performance
- Static output only
- Avoid client-side JS unless absolutely necessary
- Use native CSS where possible
- Lazy load images
- Use webp/avif
- Prefetch only on viewport
- Inline critical CSS
- No render-blocking resources

## Code
- Early returns, optional chaining (?.), nullish coalescing (??)
- Event delegation for dynamic elements
- DRY principle
- No comments unless logic is complex
- No icons/emojis/special characters
- Use CSS variables
- Prefer Tailwind utilities
- Avoid arbitrary Tailwind values when possible

## Data Structure
Create src/data/ with:
- site-config.ts
- projects.ts
- skills.ts
- social.ts

## Component Rules
- Each component must have Props interface
- No inline styles
- Split by single responsibility
- Use semantic HTML
- Minimize DOM nodes

## Build
- Check bundle size
- Keep islands minimal
- Purge unused CSS
