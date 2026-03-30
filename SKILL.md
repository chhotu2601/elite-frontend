# Elite Frontend Design — 7-Level Website Building System

A systematic approach to building professional, non-generic websites with AI coding agents. Based on the proven framework from Chase AI, adapted for OpenClaw.

## When to Use This Skill

Trigger on any of:
- "Build me a website / landing page / web app"
- "Make this look more professional"
- "This looks too generic / like AI slop"
- "Redesign the frontend"
- "Level up the design"
- Any frontend/UI work where quality matters

## The 7-Level Framework

### Level 1: Foundation (Always Start Here)

Before writing ANY code, establish the basics:

1. **Define the goal** — What is the ONE outcome this page drives? (signup, purchase, demo, waitlist)
2. **Choose a tech stack** — Next.js, Astro, plain HTML+Tailwind, etc.
3. **Use plan mode** — Ask clarifying questions about style, layout, sections
4. **Write descriptive prompts** — Not "make a landing page" but "create a dark-themed hero section with a bold tagline, subtle gradient background, asymmetric layout with the CTA above the fold"

**Anti-patterns to avoid at Level 1:**
- Purple/blue AI gradients (the #1 tell of AI-generated design)
- Generic SaaS templates (hero + 3 feature cards + pricing + footer)
- Emojis as icons (use SVG icon libraries: Heroicons, Lucide, Phosphor)
- Centered everything (use asymmetric layouts)
- Stock photo vibes

### Level 2: Design Intelligence

Load design knowledge before building:

1. **Check the toolbox** — `memory/toolbox.md` for available design tools
2. **Use ui-ux-pro-max data** — Industry-specific color palettes, typography pairings, layout patterns
3. **Apply anti-pattern rules:**
   - Banking/finance → NO neon, NO playful fonts
   - Wellness/spa → NO dark mode, NO harsh colors
   - Developer tools → OK with dark mode, monospace accents
   - E-commerce → Social proof above fold, trust signals
4. **Typography matters** — Browse Google Fonts. Pair a display font (headings) with a body font (text). Never use more than 2-3 fonts.
5. **Color theory** — Pick a primary, secondary, accent. Use 60-30-10 rule. Test contrast ratios (WCAG AA minimum: 4.5:1).

### Level 3: Visual Direction

Stop telling, start showing:

1. **Find inspiration** from these sources:
   - **Awwwards** (awwwards.com) — Award-winning sites, creative bent
   - **Godly** (godly.website) — Infinite scroll of great designs
   - **Dribbble** (dribbble.com) — Search by industry/style
   - **Pinterest** — Surprisingly good for "SaaS landing page", "portfolio design", etc.
   - **21st.dev** — Component-level inspiration (buttons, cards, navs)
   - **CodePen** — Interactive component demos
   - **Monae** — UI component library

2. **Screenshot what you like** — Take 3-5 screenshots of sites/sections you admire
3. **Feed to the agent** — "I want our site to match this visual style. Here are screenshots for reference."
4. **Combine references** — Take the hero from Site A, the cards from Site B, the footer from Site C

**The ceiling:** Screenshots get you ~50% there. The agent translates pixels to code with loss.

### Level 4: Source Code Cloning (The Big Unlock)

Go beneath the surface of sites you admire:

1. **Grab the HTML** — `Ctrl+U` (or `Cmd+Opt+U` on Mac) on any website to view source
2. **Copy the full HTML** — Select all, paste into agent
3. **Fetch CSS and JS** — Tell the agent to examine the linked stylesheets and scripts:
   ```
   Here's the HTML for [website]. Take a look at the CSS and JS files as well.
   Fetch the full content — don't summarize. I need the actual code.
   Use this to understand how they built each effect.
   ```
4. **Ask "how did they do X?"** — This is where education happens:
   - "How does their background gradient work?"
   - "What creates the scroll animation on the hero?"
   - "How did they implement the glassmorphism cards?"
   - "What font stack are they using?"
5. **Clone as template, then customize** — Never ship a clone. Use it as scaffolding.

**Site Teardown Process:**
```
Step 1: View source (Ctrl+U) → copy HTML
Step 2: Identify CSS/JS file URLs at bottom of HTML
Step 3: Agent fetches and analyzes the full CSS/JS
Step 4: Agent explains the techniques used
Step 5: Apply those techniques to YOUR design
```

### Level 5: Custom Assets & Components

Make it yours:

1. **Generate custom hero art** — Use MidJourney, DALL-E, or similar:
   - Think about visual storytelling (what does your app DO?)
   - Create a tagline that ties to the image
   - Request concept art / stylized illustrations, not stock photos
   
2. **Add motion** — Still images → video backgrounds:
   - Use Kling 3.0, VO 3.1, or similar for subtle animation
   - Keep motion SUBTLE (cloud movement, water ripples, parallax)
   - 15-second loops work best
   - Mobile: serve still image instead of video (performance)

3. **Custom components** from 21st.dev, CodePen, Monae:
   - Copy the component code/prompt
   - Modify to match your design system
   - Don't just use defaults — customize colors, animations, sizing

4. **Premium micro-interactions:**
   - Loading animations (text fade-in with slight delay)
   - Counter animations (numbers counting up)
   - Hover effects with smooth transitions (150-300ms)
   - Scroll-triggered reveals
   - Progress indicators
   - Ticker/marquee borders between sections
   - Lighting sweep effects over text

### Level 6: Visual Iteration Tools

Use external visual tools for rapid design iteration:

1. **Stitch** (Google) — Free visual canvas, AI-powered redesigns
2. **Paper.design** — Visual web design editor
3. **Pencil.dev** — Works with VS Code/Cursor for real-time visual editing
4. **Figma** — Industry standard, great for wireframing first

**Workflow:**
```
Design in visual tool → Screenshot → Bring to agent →
"What do you think about this? Let's implement the glassmorphism effect
from this design" → Agent implements → Screenshot result →
Iterate in visual tool → Repeat
```

5. **Web search for best practices:**
   ```
   Search for the best web design practices for [specific effect].
   Come up with ideas to make our website look more premium
   in a subtle fashion.
   ```

### Level 7: The Frontier (Aspirational)

Custom WebGL, Three.js shaders, 3D web experiences. Sites that look like video games.
- Check Awwwards "Site of the Day" for examples
- This is team-level work, not solo AI builds (yet)
- Keep this as inspiration for where the space is heading

## Pre-Delivery Checklist

Before considering any frontend complete:

```
[ ] No purple/blue AI gradients (unless intentionally chosen)
[ ] No emojis as icons — using SVG icon library
[ ] cursor-pointer on ALL clickable elements
[ ] Hover states with smooth transitions (150-300ms)
[ ] Text contrast minimum 4.5:1 (WCAG AA)
[ ] Focus states visible for keyboard navigation
[ ] prefers-reduced-motion respected
[ ] Responsive: tested at 375px, 768px, 1024px, 1440px
[ ] Loading animation / skeleton states
[ ] Typography: max 2-3 fonts, proper hierarchy
[ ] Color: consistent palette, 60-30-10 rule
[ ] Mobile: video backgrounds → still images
[ ] Performance: images optimized, lazy loaded
[ ] Favicon and meta tags set
```

## Quick Reference: Vocabulary

When critiquing or requesting design changes, use these terms:

| Term | Meaning |
|------|---------|
| **Glassmorphism** | Frosted glass effect with blur + transparency |
| **Neumorphism** | Soft shadows creating "pushed in/out" effect |
| **Bento grid** | Asymmetric card grid layout (like Apple) |
| **Hero section** | First thing visible, above the fold |
| **CTA** | Call to action (the main button) |
| **Above the fold** | Visible without scrolling |
| **Negative space** | Intentional empty space |
| **Parallax** | Background moves slower than foreground on scroll |
| **Marquee/Ticker** | Horizontally scrolling text strip |
| **Skeleton loading** | Gray placeholder shapes while content loads |
| **Micro-interaction** | Small animation on user action (hover, click) |
| **60-30-10 rule** | 60% dominant color, 30% secondary, 10% accent |
| **WCAG AA** | Accessibility standard (4.5:1 contrast ratio) |
| **Display font** | Decorative/bold font for headings |
| **Body font** | Clean readable font for paragraphs |

## Inspiration Sources Quick Links

- Awwwards: https://www.awwwards.com
- Godly: https://godly.website
- Dribbble: https://dribbble.com
- 21st.dev: https://21st.dev
- CodePen: https://codepen.io
- Google Fonts: https://fonts.google.com
- Heroicons: https://heroicons.com
- Lucide: https://lucide.dev
