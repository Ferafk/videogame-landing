# Portfolio Astro Performance Guidelines

## Objective
Achieve 100 in web performance metrics. Static site, minimal JS, fast loading.

## Architecture
- Atomic design: atoms, molecules, organisms, templates, pages in src/components/
- Centralize all data in src/data/*.ts - no hardcoded arrays/text in components
- No repeated HTML - use components and slots
- Max 6 props per component
- Prefer slots over excessive props

## Design System
- Mobile first: write base styles for small screens, use min-width breakpoints to scale
- Single source of truth: all colors, fonts, font sizes, weights, spacing, radii, shadows must live as CSS variables
- Variables only: never hardcode hex, rgb, font-family names or fixed px for tokens in components
- Minimal palette: define semantic tokens only (bg, surface, text-primary, text-secondary, accent, border)
- Minimal scale: limit font sizes, weights and spacing to a small curated scale
- Use CSS variables with @theme inline to map to Tailwind
- Keep visual coherence across breakpoints
- Ensure functionality and layout remain intact on mobile, tablet and desktop
- Use relative units (rem, em, %) and clamp() when fluid scaling is needed

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
- Use CSS variables for all design tokens
- Prefer Tailwind utilities backed by CSS variables
- Avoid arbitrary Tailwind values - extend theme instead
- Use rem/em for scalable sizing

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
- Responsive with mobile-first breakpoints

## Build
- Check bundle size
- Keep islands minimal
- Purge unused CSS
