# Premium Micro-Interactions

Small details that make a website feel polished and intentional. Each one is subtle on its own — together they create a premium feel.

## Page Load

### Staggered Text Reveal
Text elements fade in with slight delays between them. Hero title first, then subtitle, then CTA.
```
Delay: 100-200ms between elements
Duration: 400-600ms per element
Easing: ease-out or cubic-bezier(0.33, 1, 0.68, 1)
```

### Skeleton Loading
Gray placeholder shapes that match content layout. Shows while real content loads.

### Progress Bar
Thin bar at very top of viewport showing scroll progress through the page.

## Scroll Effects

### Scroll-Triggered Reveals
Elements animate in as they enter viewport. Use Intersection Observer, not scroll events.
```
Common patterns:
- Fade up (translateY: 20px → 0, opacity: 0 → 1)
- Fade in (opacity only)
- Scale in (scale: 0.95 → 1)
- Slide from side (for alternating content)
```

### Parallax Layers
Background moves slower than foreground. Keep it subtle — max 20% speed difference.

### Counter Animations
Numbers count up from 0 to target value when scrolled into view.
```
"10M+" → starts at 0, counts to 10,000,000+
Duration: 1.5-2.5s
Easing: ease-out (fast start, slow finish)
```

### Marquee / Ticker
Horizontally scrolling text strip. Great as section dividers.
```
Speed: 30-60px/second
Content: logos, taglines, or keywords
Pause on hover (accessibility)
```

## Hover Effects

### Button Glow
Subtle glow or shadow expansion on hover.
```css
transition: box-shadow 200ms ease;
/* Hover: */ box-shadow: 0 0 20px rgba(primary, 0.3);
```

### Card Lift
Cards subtly rise and gain shadow depth on hover.
```css
transition: transform 200ms ease, box-shadow 200ms ease;
/* Hover: */ transform: translateY(-4px);
```

### Text Underline Animation
Underline grows from left to right (or center outward) on hover.

### Image Zoom
Images scale up slightly (1.02-1.05x) on hover within their container (overflow hidden).

### Lighting Sweep
A diagonal shine/glint passes across text or cards on hover.

## Navigation

### Scroll-Aware Navbar
- Transparent on top → solid background after scrolling
- Shrinks slightly after scrolling (reduce padding)
- Hides on scroll down, shows on scroll up

### Active Section Indicator
Dot or underline moves to indicate which section is in view.

## Cursors

### Custom Cursor
Replace default cursor with a branded dot or ring. The ring expands on hovering interactive elements.

### Magnetic Elements
Buttons/links subtly pull toward the cursor when nearby (use sparingly).

## Transitions Between Sections

### Color Shifts
Background color transitions smoothly between sections as you scroll.

### Gradient Borders
Thin animated gradient lines separating sections.

### SVG Dividers
Wavy or angled SVG shapes between sections instead of hard lines.

## Implementation Notes

- **Always respect `prefers-reduced-motion`** — disable animations for users who set this
- **Performance:** Use `transform` and `opacity` for animations (GPU-accelerated). Avoid animating `width`, `height`, `top`, `left`.
- **Timing:** 150-300ms for hover effects, 400-800ms for scroll reveals
- **Easing:** `ease-out` for entrances, `ease-in` for exits, `ease-in-out` for loops
