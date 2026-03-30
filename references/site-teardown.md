# Site Teardown Guide

How to deconstruct any website and learn from its source code.

## Step-by-Step Process

### 1. Find a Site You Admire
Browse Awwwards, Godly, Dribbble, or Pinterest. Pick something that makes you go "how did they do THAT?"

### 2. View the Source HTML
- **Mac:** `Cmd + Option + U`
- **Windows/Linux:** `Ctrl + U`
- **Alternative:** Right-click → "View Page Source"

Copy the entire HTML. It'll typically be 500-2,000+ lines.

### 3. Identify CSS and JS Files
Scroll to the bottom of the HTML. You'll find `<link>` tags (CSS) and `<script>` tags (JS):

```html
<!-- These are usually at the bottom -->
<link rel="stylesheet" href="/css/main.abc123.css">
<script src="/js/app.def456.js"></script>
```

### 4. Feed Everything to Your Agent

```
Here's the full HTML for [website-name]:

[paste HTML]

Now fetch and analyze the CSS and JS files linked at the bottom.
Don't summarize — I need the actual code to understand the techniques.

After analyzing, explain:
1. How the background effect works
2. What creates the scroll animations
3. How the typography is set up
4. What makes the hover interactions feel smooth
5. Any other noteworthy techniques
```

### 5. Ask Targeted Questions

Once the agent has the code, drill into specifics:

```
How did they create the glassmorphism effect on the cards?
What CSS makes the text fade in on scroll?
How is the gradient background animated?
What's the font stack and sizing system?
How does the navigation hide/show on scroll?
```

### 6. Apply to Your Design

```
Now apply that same [technique] to our [section].
Keep our color palette but use their approach for [specific effect].
```

## What to Look For

### In the CSS:
- `backdrop-filter: blur()` — glassmorphism
- `@keyframes` — custom animations
- `transition` properties — hover/interaction timing
- `grid` / `flexbox` layouts — how sections are structured
- Custom properties (`--var-name`) — design system tokens
- `mix-blend-mode` — creative overlay effects

### In the JS:
- Intersection Observer — scroll-triggered animations
- GSAP / Framer Motion — animation libraries
- Three.js / WebGL — 3D effects
- Lenis / Locomotive — smooth scrolling
- Event listeners on `scroll`, `mousemove` — interactive effects

### In the HTML:
- Section structure and nesting depth
- SVG usage (inline vs referenced)
- `<picture>` elements with responsive images
- Semantic tags (`<header>`, `<main>`, `<section>`, `<footer>`)
- Data attributes for animation triggers
