---
name: elite-frontend
description: >
  7-level framework for building professional, non-generic websites and landing pages with AI coding agents.
  Use when: (1) building a website, landing page, or web app frontend, (2) user says design looks "generic" or "like AI slop",
  (3) redesigning or improving an existing frontend, (4) user asks to "make it look more professional" or "level up the design",
  (5) any frontend/UI work where visual quality matters. Provides systematic progression from raw prompts through
  design skills, visual references, source code cloning, custom assets, and visual iteration tools.
  Includes pre-delivery checklist, anti-patterns by industry, micro-interaction catalog, and inspiration sources.
---

# Elite Frontend — 7-Level Website Building System

## Quick Reference: The Levels

| Level | Name | Core Action |
|-------|------|-------------|
| 1 | Foundation | Plan mode → define goal, stack, descriptive prompts |
| 2 | Design Intelligence | Load design knowledge → color, typography, anti-patterns |
| 3 | Visual Director | Screenshot sites you admire → feed as references |
| 4 | The Cloner | Extract HTML/CSS/JS source → learn HOW sites are built |
| 5 | Custom Assets | Generate original art, motion, custom components |
| 6 | Visual Iteration | Use Stitch/Figma/Pencil.dev for rapid visual tinkering |
| 7 | The Frontier | Custom WebGL, Three.js, shaders, 3D (aspirational) |

Always start at Level 1 and progress upward. Each level compounds on the previous.

## Level 1: Foundation

Before writing ANY code:

1. **Define the ONE outcome** — signup, purchase, demo request, waitlist
2. **Choose tech stack** — Next.js, Astro, HTML+Tailwind, etc.
3. **Use plan mode** — ask clarifying questions about style, layout, sections
4. **Write descriptive prompts** — not "make a landing page" but "dark-themed hero section with bold tagline, subtle gradient, asymmetric layout, CTA above the fold"

## Level 2: Design Intelligence

Apply design knowledge before building. See [references/anti-patterns.md](references/anti-patterns.md) for industry-specific rules.

Key rules:
- **Typography:** Max 2-3 fonts. Pair display font (headings) + body font (text). Browse Google Fonts.
- **Color:** Pick primary, secondary, accent. 60-30-10 rule. WCAG AA contrast (4.5:1 minimum).
- **Anti-patterns:** No purple AI gradients. No emojis as icons (use Heroicons/Lucide SVGs). No centered-everything.

## Level 3: Visual Director

Stop telling, start showing. Screenshot 3-5 sites you admire from inspiration sources, feed to agent:

```
I want our site to match this visual style. Here are screenshots for reference.
```

Combine references from multiple sites — hero from Site A, cards from Site B.

**Ceiling:** Screenshots get ~50% there due to visual→code translation loss.

See [references/inspiration-sources.md](references/inspiration-sources.md) for where to find inspiration.

## Level 4: The Cloner (Biggest Unlock)

Go beneath the surface. Extract actual source code from sites you admire:

1. `Cmd+Opt+U` (Mac) or `Ctrl+U` (Windows) → copy full HTML
2. Tell agent to fetch linked CSS/JS files (full content, not summarized)
3. Ask "how did they do X?" for each effect you like
4. Apply those techniques to YOUR design

See [references/site-teardown.md](references/site-teardown.md) for the complete process.

## Level 5: Custom Assets

Make it yours:
- **Custom hero art** — MidJourney/DALL-E for visual storytelling tied to your product
- **Motion** — Subtle video backgrounds (15s loops) via Kling/VO. Mobile: serve still image.
- **Components** — Browse 21st.dev, CodePen, Aceternity UI. Copy, then customize.
- **Micro-interactions** — Loading animations, counters, hover effects, tickers, scroll reveals

See [references/micro-interactions.md](references/micro-interactions.md) for the full catalog.

## Level 6: Visual Iteration

Use external visual tools for rapid design iteration:
- **Stitch** (Google) — free visual canvas with AI redesigns
- **Paper.design** — visual web design editor
- **Pencil.dev** — real-time visual editing in VS Code/Cursor
- **Figma** — wireframing and layout exploration

Workflow: Design in visual tool → screenshot → bring to agent → implement → iterate.

Also: tell the agent to web search for best practices on specific effects.

## Level 7: The Frontier

Custom WebGL, Three.js shaders, 3D web experiences. Check Awwwards "Site of the Day" for examples. Currently team-level work, not solo AI builds.

## Pre-Delivery Checklist

Before shipping any frontend:

```
[ ] No unintentional purple/blue AI gradients
[ ] No emojis as icons — using SVG icon library
[ ] cursor-pointer on all clickable elements
[ ] Hover states with smooth transitions (150-300ms)
[ ] Text contrast ≥ 4.5:1 (WCAG AA)
[ ] Focus states visible for keyboard navigation
[ ] prefers-reduced-motion respected
[ ] Responsive: 375px, 768px, 1024px, 1440px
[ ] Loading animations / skeleton states
[ ] Typography: max 2-3 fonts, proper hierarchy
[ ] Color: consistent palette, 60-30-10 rule
[ ] Mobile: video backgrounds → still images
[ ] Images optimized + lazy loaded
[ ] Favicon and meta tags set
```

## Design Vocabulary

| Term | Meaning |
|------|---------|
| Glassmorphism | Frosted glass effect (blur + transparency) |
| Bento grid | Asymmetric card layout (Apple style) |
| Hero section | First visible area, above the fold |
| CTA | Call to action button |
| Negative space | Intentional empty space |
| Parallax | Background moves slower than foreground on scroll |
| Marquee/Ticker | Horizontally scrolling text strip |
| Skeleton loading | Gray placeholders while content loads |
| 60-30-10 | 60% dominant color, 30% secondary, 10% accent |
