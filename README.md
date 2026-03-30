# Elite Frontend 🎨

**Stop building AI slop. Start building websites that actually look good.**

A 7-level framework for building professional, non-generic websites with AI coding agents. Works with Claude Code, Cursor, Windsurf, OpenClaw, or any AI coding tool.

<p align="center">
  <img src="assets/levels-overview.png" alt="7 Levels Overview" width="700">
</p>

## The Problem

You tell your AI agent "build me a landing page" and get:
- Purple gradient backgrounds 💀
- Generic SaaS template layout
- Three feature cards with emoji icons
- Zero personality, zero taste

**This isn't the AI's fault — it's a taste articulation problem.** You can't describe what you don't know the words for.

## The Solution: 7 Levels

Each level builds on the last. You don't skip levels — you progress through them.

| Level | Name | What You Do | What Changes |
|-------|------|-------------|-------------|
| **1** | Foundation | Use plan mode, define goals, write descriptive prompts | You stop getting random output |
| **2** | Design Intelligence | Load UI/UX skills, apply color theory + typography rules | Output looks *designed* (but still templated) |
| **3** | Visual Director | Screenshot real sites you admire, feed as references | Agent mimics styles, not just follows rules |
| **4** | The Cloner | Extract actual HTML/CSS/JS from sites, learn HOW they work | **Biggest unlock** — you learn the vocabulary |
| **5** | Custom Assets | Generate original art, add motion, build custom components | Your site has personality and character |
| **6** | Visual Iteration | Use Stitch/Figma/Paper.design for rapid visual tinkering | You iterate visually, not just through text |
| **7** | The Frontier | Custom WebGL, Three.js, shaders, 3D experiences | The big leagues (aspirational) |

## Quick Start

### Claude Code
```bash
# Install as a skill
cp -r elite-frontend ~/.claude/skills/elite-frontend

# Or clone directly
git clone https://github.com/YajatNS/elite-frontend.git ~/.claude/skills/elite-frontend
```

Then in Claude Code:
```
Use the elite-frontend skill to build a landing page for [your project]
```

### OpenClaw
Copy to your skills directory:
```bash
cp -r elite-frontend ~/workspace/skills/elite-frontend
```

### Cursor / Windsurf / Any Agent
Copy `SKILL.md` into your project's `.cursor/rules/` or equivalent rules directory. The framework is pure markdown — works anywhere.

## What's Inside

```
elite-frontend/
├── SKILL.md                    # The complete framework (the skill itself)
├── README.md                   # You're here
├── references/
│   ├── site-teardown.md        # Step-by-step guide to cloning sites (Level 4)
│   ├── anti-patterns.md        # What to avoid, by industry
│   ├── micro-interactions.md   # Premium effects that make sites feel polished
│   └── inspiration-sources.md  # Where to find design inspiration
├── examples/
│   ├── level-1-raw.png         # What Level 1 output looks like
│   ├── level-2-skills.png      # With design skills applied
│   ├── level-4-cloned.png      # After source code cloning
│   └── level-5-custom.png      # With custom assets
└── LICENSE
```

## The Key Insight

> **AI doesn't lack taste — YOU lack the vocabulary to articulate taste.**

Each level builds your design vocabulary:
- Level 1: You learn what questions to ask
- Level 2: You learn color theory, typography, spacing
- Level 3: You learn to see what "good" looks like
- Level 4: You learn HOW the good stuff is built
- Level 5: You learn to create your own style
- Level 6: You learn to iterate visually
- Level 7: You push the frontier

## Pre-Delivery Checklist

Every site built with this framework passes these checks:

- [ ] No purple/blue AI gradients (unless intentionally chosen)
- [ ] No emojis as icons — SVG icon library used (Heroicons, Lucide)
- [ ] `cursor: pointer` on all clickable elements
- [ ] Hover states with smooth transitions (150-300ms)
- [ ] Text contrast ≥ 4.5:1 (WCAG AA)
- [ ] Focus states visible for keyboard navigation
- [ ] `prefers-reduced-motion` respected
- [ ] Responsive: 375px, 768px, 1024px, 1440px
- [ ] Loading animations / skeleton states
- [ ] Typography: max 2-3 fonts, proper hierarchy
- [ ] Color: consistent palette, 60-30-10 rule
- [ ] Mobile: video backgrounds → still images
- [ ] Images optimized + lazy loaded
- [ ] Favicon and meta tags set

## Inspiration Sources

| Source | Best For | URL |
|--------|----------|-----|
| Awwwards | Award-winning creative sites | [awwwards.com](https://www.awwwards.com) |
| Godly | Infinite scroll of great designs | [godly.website](https://godly.website) |
| Dribbble | Search by industry/style | [dribbble.com](https://dribbble.com) |
| Pinterest | Surprisingly good SaaS inspo | [pinterest.com](https://pinterest.com) |
| 21st.dev | Component-level inspiration | [21st.dev](https://21st.dev) |
| CodePen | Interactive demos | [codepen.io](https://codepen.io) |
| Google Fonts | Typography pairing | [fonts.google.com](https://fonts.google.com) |

## Credits

Framework based on [Chase AI's "7 Levels of Building Elite Websites with Claude Code"](https://www.youtube.com/watch?v=1PXFAFMgdns), distilled and adapted into a reusable skill.

## License

MIT — use it, fork it, make beautiful things.
