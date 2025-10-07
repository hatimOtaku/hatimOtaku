# Design Guidelines: Ibn Tofail University CS Club Website

## Design Approach: Modern Tech-Inspired with Blue Theme
**Approach**: Reference-based, drawing inspiration from Linear, Stripe, and GitHub for a contemporary computer science aesthetic
**Rationale**: CS clubs demand a modern, tech-forward identity that balances visual appeal with information clarity

## Core Design Elements

### A. Color Palette

**Primary Colors (Blue Theme):**
- Primary Blue: 217 91% 60% (vibrant tech blue)
- Deep Blue: 222 47% 11% (backgrounds, dark mode base)
- Light Blue: 210 100% 97% (subtle backgrounds)

**Supporting Colors:**
- Accent Cyan: 187 85% 55% (interactive elements, highlights)
- Success Green: 142 71% 45% (achievements, success states)
- Neutral Gray: 217 10% 50% (secondary text)
- Pure White/Black: For contrast and text

**Gradient Applications:**
- Hero background: Linear gradient from Deep Blue to Primary Blue (45deg)
- Card hovers: Subtle blue-to-cyan gradient overlays
- Section dividers: Gradient borders using primary colors

### B. Typography

**Font Stack (Google Fonts):**
- Headings: 'Space Grotesk' - Modern, geometric, tech-forward (weights: 500, 600, 700)
- Body: 'Inter' - Clean, highly legible (weights: 400, 500, 600)
- Code/Tech Elements: 'JetBrains Mono' - For enrollment IDs, member badges

**Scale:**
- H1 (Hero): text-6xl (3.75rem) md:text-7xl lg:text-8xl font-bold
- H2 (Section): text-4xl md:text-5xl font-semibold
- H3 (Cards): text-2xl md:text-3xl font-medium
- Body: text-base md:text-lg
- Small: text-sm

### C. Layout System

**Spacing Primitives**: Consistent use of Tailwind units: 2, 4, 6, 8, 12, 16, 20, 24, 32
- Component padding: p-6 to p-8
- Section spacing: py-16 md:py-24 lg:py-32
- Grid gaps: gap-6 md:gap-8
- Container max-width: max-w-7xl for main content

**Grid Systems:**
- Members: grid-cols-1 md:grid-cols-2 lg:grid-cols-3 (profile cards)
- Formations: grid-cols-1 lg:grid-cols-2 (course + enrollment form side-by-side)
- Achievements: Single column timeline with alternating left/right content
- News: grid-cols-1 md:grid-cols-2 lg:grid-cols-3 (article cards)

### D. Component Library

**Navigation:**
- Sticky header with glass-morphism effect (backdrop-blur-md bg-deep-blue/90)
- Logo on left, nav links centered/right
- Mobile: Hamburger menu with slide-in drawer animation
- Active state: Border-bottom accent with Primary Blue

**Hero Section:**
- Full viewport height (min-h-screen) with animated gradient background
- Centered content: Club name, tagline, dual CTAs (Join Club, View Achievements)
- Floating geometric shapes with parallax movement on scroll
- Large hero image: Tech-themed illustration or CS club group photo (70% opacity overlay)

**Member Cards:**
- Rounded corners (rounded-xl), subtle shadow (shadow-lg)
- Profile image at top, name, role, tech stack badges
- Hover: Lift effect (translate-y-1), enhanced shadow, reveal social links
- Background: Card bg with blue gradient border on hover

**Formation/Enrollment:**
- Two-column desktop layout: Course details left, enrollment form right
- Form: Modern input fields with floating labels, blue focus rings
- Validation states with inline feedback
- Submit button: Primary blue with cyan hover gradient

**Achievement Timeline:**
- Vertical timeline with animated reveal on scroll
- Alternating left/right content blocks
- Icons for achievement types (hackathon trophy, certificate, project badge)
- Date labels on timeline axis, content cards with blue accent borders

**News Cards:**
- Image thumbnail top, title, excerpt, read more link
- Published date and category badge
- Hover: Image zoom effect (scale-105), blue overlay

**Footer:**
- Three-column layout: About, Quick Links, Contact Info
- University logo and CS club branding
- Social media icons with hover animations
- Newsletter signup form with inline button

### E. Animations & Interactions

**Scroll-Triggered Animations (Framer Motion):**
- Fade-in-up for section content (opacity 0→1, y: 20→0)
- Stagger children animations for grids (delay: 0.1s between items)
- Scale-in for cards (scale 0.95→1)
- Draw-in for timeline connectors (scaleY 0→1)

**Background Animation:**
- Parallax floating geometric shapes (triangles, circles, hexagons in blue shades)
- Shapes move at different speeds relative to scroll (transform: translateY)
- Subtle gradient shift on scroll progress
- Particle grid effect in hero section

**Micro-interactions:**
- Button ripple effect on click
- Input field glow on focus (blue shadow)
- Card tilt on hover (subtle 3D rotation)
- Navigation link underline slide animation

**Performance Note:** Limit complex animations to hero and key interaction points; use CSS transforms for smooth 60fps performance

## Images

**Hero Section:**
- Large hero image: CS club members collaborating on code, or futuristic tech workspace illustration
- Placement: Full-width background with 60% blue gradient overlay
- Style: Modern, vibrant, conveys innovation and teamwork

**Members Section:**
- Individual profile photos for each member
- Consistent circular frames (rounded-full)
- Professional headshots or casual club environment shots

**Achievements Section:**
- Trophy/medal icons for accomplishments
- Event photos (hackathons, workshops)
- Certificate/award graphics

**News Section:**
- Article thumbnail images
- Event photos, workshop screenshots
- Consistent 16:9 aspect ratio

## Accessibility & Responsive

- WCAG AA contrast ratios maintained with blue theme
- Focus states: 2px blue ring (ring-2 ring-primary-blue)
- Mobile-first responsive breakpoints (sm:, md:, lg:, xl:)
- Touch targets minimum 44x44px
- Semantic HTML throughout

This design creates a modern, engaging CS club website that balances tech-forward aesthetics with functional clarity, using the blue theme strategically across all touchpoints.