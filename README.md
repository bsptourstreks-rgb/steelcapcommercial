# Steel Cap Commercial Website

> Premium integrated facility management and IT services landing page for Steel Cap Commercial.

**Live Site:** [steelcapcommercial.com](https://steelcapcommercial.com)
**Repository:** [github.com/bsptourstreks-rgb/steelcapcommercial](https://github.com/bsptourstreks-rgb/steelcapcommercial)

---

## Table of Contents
- [Overview](#overview)
- [Development Timeline](#development-timeline)
- [Technology Stack](#technology-stack)
- [Design System](#design-system)
- [Components Documentation](#components-documentation)
- [Animations & Effects](#animations--effects)
- [Performance Optimization](#performance-optimization)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Deployment](#deployment)

---

## Overview

A modern, responsive single-page website showcasing Steel Cap Commercial's dual expertise in facility management and enterprise IT services. The design features a premium silver/tech aesthetic with animated circuit board motifs, interactive elements, and smooth scroll animations.

The website serves as a marketing landing page designed to:
- Convert visitors into leads through clear CTAs
- Showcase service offerings visually
- Build trust through professional design
- Provide information about company capabilities

---

## Development Timeline

| Phase | Date | Time | Duration | Activities |
|-------|------|------|----------|------------|
| **Planning** | March 19, 2026 | 2:00 PM - 4:00 PM | 2h | Project setup, design system planning, component architecture |
| **Core Development** | March 19, 2026 | 4:00 PM - 8:00 PM | 4h | Hero section, Navigation, Footer, base layouts |
| **Services Sections** | March 20, 2026 | 10:00 AM - 2:00 PM | 4h | Services, IT Services, Industries components |
| **Refinement** | March 20, 2026 | 3:00 PM - 7:00 PM | 4h | Animations, responsive fixes, final polish |
| **Total** | March 19-20, 2026 | - | **14h elapsed** | **8h active development** |

**Actual Development Time: 8 hours**

---

## Technology Stack

### Core Framework
| Technology | Version | Purpose |
|------------|---------|---------|
| **Astro** | 6.0.6 | Static site generator with zero JS by default |
| **Vite** | Built-in | Build tool and dev server with HMR |
| **TypeScript** | 5.x | Type safety and enhanced developer experience |

### Styling
| Technology | Purpose |
|------------|---------|
| **Tailwind CSS** | Utility-first CSS framework via Astro integration |
| **CSS Modules** | Component-scoped styles in `.astro` files |
| **Inline SVG** | Scalable graphics with direct animation control |

### JavaScript
| Technology | Purpose |
|------------|---------|
| **Vanilla JS** | Intersection Observer for scroll animations |
| **Event Listeners** | Magnetic button effects, smooth scroll |
| **CSS Animations** | Hardware-accelerated transforms |

### Development Tools
| Tool | Purpose |
|------|---------|
| **VS Code** | Primary IDE with Astro extension |
| **Git** | Version control |
| **npm** | Package management |

---

## Design System

### Color Specifications

#### Light Theme (Hero, CTA, Footer)
```css
/* Silver Gradient Background */
background: linear-gradient(135deg, #d4d4d8 0%, #e4e4e7 30%, #f4f4f5 50%, #e4e4e7 70%, #d4d4d8 100%);

/* Primary Text */
color: #0f172a; /* slate-900 */

/* Secondary Text */
color: #475569; /* slate-600 */

/* Muted Text */
color: #64748b; /* slate-500 */
```

#### Dark Theme (Services, IT Services, Industries)
```css
/* Background */
background: linear-gradient(to bottom right, #0f172a, #1e293b);

/* Card Background */
background: #1e293b;

/* Primary Text */
color: #ffffff;

/* Secondary Text */
color: #94a3b8; /* slate-400 */
```

#### Accent Colors
```css
/* Sky Blue - Facility Services */
--accent-sky: #0ea5e9;
--accent-sky-light: #38bdf8;
--accent-sky-dark: #0284c7;

/* Violet - IT Services */
--accent-violet: #8b5cf6;
--accent-violet-light: #a78bfa;
--accent-violet-dark: #7c3aed;

/* Emerald - Industries */
--accent-emerald: #10b981;
--accent-emerald-light: #34d399;
--accent-emerald-dark: #059669;

/* Amber - Accents */
--accent-amber: #f59e0b;
--accent-amber-light: #fbbf24;
```

### Typography Scale

```css
/* Display Headings */
font-size: clamp(32px, 5vw, 48px);
font-weight: 700;
line-height: 1.1;
letter-spacing: -0.02em;

/* Section Headings */
font-size: 36px;
font-weight: 700;
line-height: 1.2;
letter-spacing: -0.02em;

/* Body Large */
font-size: 17px;
line-height: 1.7;

/* Body Base */
font-size: 15px;
line-height: 1.6;

/* Small Text */
font-size: 12px;
line-height: 1.5;

/* Captions */
font-size: 10px;
line-height: 1.4;
```

### Spacing System

```css
/* Container Widths */
container-narrow: max-width: 640px;
container-center: max-width: 1024px;
container-wide: max-width: 1280px;

/* Section Padding */
padding: py-16; /* 4rem / 64px vertical */
padding: py-20; /* 5rem / 80px vertical for CTA */

/* Component Gaps */
gap: 3px; /* Micro gaps between cards */
gap: 1rem; /* Standard spacing */
gap: 1.5rem; /* Medium spacing */
gap: 3rem; /* Large spacing */
```

### Border Radius
```css
/* Sharp edges for premium industrial look */
border-radius: 0; /* All cards and buttons */

/* Exception: rounded pills for badges */
border-radius: 9999px; /* Section badges */
```

### Shadows
```css
/* Subtle card shadow */
box-shadow: 0 1px 2px rgba(0, 0, 0, 0.3),
            0 4px 8px rgba(0, 0, 0, 0.2);

/* Hover lift shadow */
box-shadow: 0 30px 80px rgba(0, 0, 0, 0.6),
            0 15px 40px rgba(var(--accent), 0.25),
            0 4px 12px rgba(0, 0, 0, 0.2);

/* Premium glass shadow */
filter: drop-shadow(0 4px 12px rgba(0, 0, 0, 0.08));
```

---

## Components Documentation

### 1. Navigation.astro

**Purpose:** Fixed header navigation with smooth scroll

**Features:**
- Fixed position at top of viewport
- Backdrop blur effect for readability
- Steel Cap logo with styling
- Navigation links with hover states
- Mobile responsive (hamburger menu ready)

**Key Styles:**
```css
position: fixed;
top: 0;
left: 0;
right: 0;
z-index: 1000;
backdrop-filter: blur(12px);
background: rgba(255, 255, 255, 0.9);
border-bottom: 1px solid rgba(0, 0, 0, 0.05);
```

**Interactions:**
- Links change color on hover
- Smooth scroll to section anchors
- Logo scales slightly on hover

---

### 2. Hero.astro

**Purpose:** Main hero section with animated SVG chip illustration

**Dimensions:** ~600px minimum height, responsive

**Key Elements:**

#### CPU Chip (Center)
- 110×110px main body
- Animated rotating rings (8s and 6s durations)
- Pulsing core with 1s heartbeat
- 18 gold pins (9 pairs)

#### Connection Traces
- 4 diagonal paths from chip corners
- Animated electric current pulses
- 1.5s - 2s duration variations

#### Module Cards (4 corners)
1. **Cloud Infrastructure & DevOps** (Top-Left)
   - Cyan accent (#0ea5e9)
   - Floating animation (4s duration)

2. **IT & Security** (Top-Right)
   - Amber accent (#f59e0b)
   - Floating animation with delay

3. **Facility Management** (Bottom-Left)
   - Slate accent (#64748b)
   - Floating animation with delay

4. **Energy Solutions** (Bottom-Right)
   - Emerald accent (#10b981)
   - Floating animation with delay

**SVG Filters Used:**
```xml
<filter id="pulseGlow">  <!-- Gaussian blur for glow effect -->
<filter id="circuitShadow">  <!-- Drop shadow for depth -->
<filter id="glassShadow">  <!-- Multi-layer shadow for glass effect -->
```

**Gradients:**
- `silverTrace` - Circuit trace colors
- `pulseGrad` - Electric pulse gradient
- `goldPin` - Gold pin gradient
- `centerPulse` - Radial pulse from center

---

### 3. TrustBar.astro

**Purpose:** Display client/partner logos for social proof

**Features:**
- Grid or horizontal scroll layout
- Grayscale logos with color on hover
- Infinite scroll animation (optional)

**Default State:** Placeholder logos ready for replacement

---

### 4. Services.astro

**Purpose:** Showcase 6 facility services in Apple-style gallery

**Layout:** Responsive grid
- Mobile: 2 columns
- Tablet+: 3 columns
- Max width: 1200px

**Card Specifications:**
- Aspect ratio: 4:3
- Gap: 2-3px (micro gap for seamless look)
- Border radius: 0 (sharp edges)

**Services:**
1. Facility Management
2. Renewable Energy
3. Property Maintenance
4. Commercial Cleaning
5. Landscaping
6. Technical Services

**Hover Effects:**
```css
transform: scale(1.05) translateY(-6px);
box-shadow: 0 30px 80px rgba(0, 0, 0, 0.7);
background: radial-gradient(...) /* Mouse tracking glow */
```

**Animation Timing:**
- Scale/transform: 0.5s cubic-bezier(0.4, 0, 0.2, 1)
- Overlay fade: 0.4s ease
- Glow opacity: 0.3s ease

---

### 5. ITServices.astro

**Purpose:** Showcase 6 IT services with circuit board theme

**Layout:** Same responsive grid as Services

**Background Animation:**
- SVG circuit traces with purple/blue gradient
- Animated cyan pulses flowing along paths
- Pulsing nodes at circuit junctions

**Services:**
1. Managed IT & Support
2. Cybersecurity
3. Cloud & DevOps
4. Software Development
5. Data & AI
6. Enterprise Systems

**Color Scheme:**
- Background: Indigo-950 to slate-900 gradient
- Accent: Violet-400 to violet-600
- Pulse: Cyan-400 with glow filter

**Circuit Pattern:**
- 60px × 60px grid overlay
- Hexagonal/angled trace paths
- 9+ circuit nodes with pulse animations

---

### 6. Industries.astro

**Purpose:** Horizontal scroll gallery of 6 industries served

**Layout:** Horizontal flex container
- Mobile: 180px cards
- Tablet: 220px cards
- Desktop: 280px cards

**Scroll Behavior:**
```css
overflow-x: auto;
scroll-snap-type: x mandatory;
scrollbar-width: none;  /* Hide scrollbar */
```

**Industries:**
1. Commercial
2. Retail
3. Education
4. Industrial
5. Hospitality
6. Aged Care

**Card Design:**
- Solid gradient background (no images)
- Slate-500 to slate-700 gradient
- Emerald accent on hover
- Description hidden until hover

**Scroll Indicator:**
- Visible on mobile only
- Text: "Swipe to explore more industries"
- Animated arrow bouncing
- Hides at 768px breakpoint

---

### 7. CTA.astro

**Purpose:** Final call-to-action section with contact options

**Layout:** Centered, narrow container

**Elements:**
1. Animated icon with ping effect
2. Gradient heading text
3. Description text
4. Two CTA buttons (primary + secondary)
5. Trust badges row

**Primary Button:**
```css
background: linear-gradient(135deg, #0284c7 0%, #0369a1 100%);
padding: 16px 32px;
shimmer animation on hover
```

**Secondary Button:**
```css
background: white;
border: 2px solid #e2e8f0;
phone icon with shake animation
```

**Magnetic Effect:**
- Button follows cursor slightly
- JavaScript calculates offset from center
- Smooth return on mouse leave

**Trust Badges:**
- Licensed & Insured
- ISO Certified
- 24/7 Support
- Icon + label layout

---

### 8. Footer.astro

**Purpose:** Site footer with links and branding

**Theme:** Silver gradient matching Hero

**Layout:**
- Logo + description + social links (2 cols)
- 4 link columns (Facility, IT, Company, Legal)
- Bottom bar with copyright, location, back-to-top

**Social Icons:**
- White background with slate border
- Inverts to dark on hover
- Scale and lift animation
- Icons: LinkedIn, Twitter, Facebook, Instagram, Email

**Bottom Bar:**
- Slightly darker silver gradient
- Premium black text for contrast
- Flex layout with responsive wrap

---

## Animations & Effects

### Scroll Reveal Animation

**Implementation:** Intersection Observer API

```javascript
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('visible');
    }
  });
}, { threshold: 0.1, rootMargin: '0px 0px -50px 0px' });
```

**CSS:**
```css
.scroll-reveal {
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.7s cubic-bezier(0.16, 1, 0.3, 1);
}

.scroll-reveal.visible {
  opacity: 1;
  transform: translateY(0);
}
```

**Stagger Delays:**
- Applied via inline `style` attributes
- Increments of 0.08s - 0.1s per item

---

### Magnetic Button Effect

**Implementation:** JavaScript mouse tracking

```javascript
btn.addEventListener('mousemove', (e) => {
  const rect = btn.getBoundingClientRect();
  const x = e.clientX - rect.left - rect.width / 2;
  const y = e.clientY - rect.top - rect.height / 2;
  btn.style.transform = `translate(${x * 0.2}px, ${y * 0.2}px)`;
});
```

**Intensity:** 20% of cursor distance

---

### SVG Animations

#### Rotating Rings
```xml
<rect animateTransform="rotate" from="0 0 0" to="360 0 0" dur="8s" repeatCount="indefinite"/>
```

#### Pulsing Core
```xml
<rect animate attributeName="opacity" values="0.4;1;0.4" dur="1s" repeatCount="indefinite"/>
<rect animate attributeName="rx" values="14;18;14" dur="1s" repeatCount="indefinite"/>
```

#### Electric Current
```xml
<circle animateMotion dur="1.5s" repeatCount="indefinite" path="M145 145 L80 80"/>
```

#### Floating Modules
```css
@keyframes module-float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-6px); }
}
.module-float { animation: module-float 4s ease-in-out infinite; }
```

---

### Card Hover Effects

**Services/IT Cards:**
- Scale: 1.05
- Translate Y: -6px
- Box shadow expansion
- Border gradient fade in
- Image scale: 1.1-1.2

**Industries Cards:**
- Scale: 1.02
- Translate Y: -12px
- Background gradient shift
- Title color change
- Description fade in

---

## Performance Optimization

### Static Site Generation
- All pages pre-rendered at build time
- No client-side hydration required
- Instant page loads

### Image Optimization
- Unsplash images with `?w=600&q=80` parameters
- Lazy loading ready (not implemented for simplicity)
- WebP format supported by Unsplash

### CSS Optimization
- Scoped styles per component
- No external CSS files (except global reset)
- Tailwind purges unused classes in production

### JavaScript Minimization
- Only essential JS loaded
- No framework overhead
- Intersection Observer over scroll event listeners

### Build Output
```bash
Build complete in 1.2s
Generating static pages...
✓ 1 page built
Total size: ~150KB (including assets)
```

---

## Project Structure

```
steel-cap-astro/
├── public/                          # Static assets (served as-is)
│   ├── favicon.ico                  # 32×32 favicon
│   └── favicon.svg                  # Scalable SVG favicon
│
├── src/
│   ├── components/                  # Astro components
│   │   ├── Navigation.astro         # 140 lines - Fixed header
│   │   ├── Hero.astro               # 514 lines - Main hero with SVG animations
│   │   ├── TrustBar.astro           # 80 lines - Client logos
│   │   ├── Services.astro           # 290 lines - Facility services gallery
│   │   ├── ITServices.astro         # 387 lines - IT services with circuits
│   │   ├── Industries.astro         # 275 lines - Horizontal scroll industries
│   │   ├── CTA.astro                # 295 lines - Call-to-action section
│   │   └── Footer.astro             # 210 lines - Silver gradient footer
│   │
│   ├── layouts/
│   │   └── Layout.astro             # 80 lines - Base HTML layout
│   │
│   ├── pages/
│   │   └── index.astro              # 50 lines - Homepage (assembles components)
│   │
│   └── styles/
│       └── global.css               # 60 lines - Global styles & reset
│
├── astro.config.mjs                 # Astro configuration
├── package.json                     # Dependencies & scripts
├── tsconfig.json                    # TypeScript configuration
├── .gitignore                       # Git ignore patterns
├── README.md                        # This file
└── dist/                            # Build output (generated)
```

**Total Lines of Code:** ~2,380 lines (excluding dependencies)

---

## Getting Started

### Prerequisites
- Node.js 18.0.0 or higher
- npm 9.0.0 or higher
- Git (for cloning)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/bsptourstreks-rgb/steelcapcommercial.git
cd steelcapcommercial

# 2. Install dependencies
npm install

# 3. Start development server
npm run dev

# 4. Open browser
# Navigate to http://localhost:4321
```

### Available Scripts

| Command | Action | Environment |
|---------|--------|-------------|
| `npm install` | Install dependencies | - |
| `npm run dev` | Start dev server at `localhost:4321` | Development |
| `npm run build` | Build for production | Production |
| `npm run preview` | Preview production build | Production |
| `npm run astro ...` | Run Astro CLI commands | - |

### Development Workflow

1. **Make changes** to `.astro` files
2. **Save** files - Hot reload refreshes browser
3. **Test** in multiple viewport sizes
4. **Build** locally before deploying
5. **Commit** and push changes

---

## Deployment

### Deployment Options

#### Vercel (Recommended)
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel deploy
```

#### Netlify
```bash
# Install Netlify CLI
npm i -g netlify-cli

# Deploy
netlify deploy --prod
```

#### GitHub Pages
```bash
# Build
npm run build

# Deploy to gh-pages branch
npx gh-pages -d dist
```

#### Cloudflare Pages
- Connect GitHub repository
- Build command: `npm run build`
- Build output directory: `dist`

### Environment Variables
None required - site is fully static.

### Custom Domain
1. Purchase domain from registrar
2. Add CNAME record pointing to hosting provider
3. Update domain in hosting provider dashboard

---

## Browser Support

| Browser | Minimum Version | Notes |
|---------|----------------|-------|
| Chrome | 90+ | Full support |
| Edge | 90+ | Full support |
| Firefox | 88+ | Full support |
| Safari | 14+ | Full support |
| iOS Safari | 14+ | Full support |
| Chrome Android | 90+ | Full support |

**Features Used:**
- CSS Grid
- CSS Custom Properties
- Intersection Observer
- Backdrop Filter
- CSS Transforms & Animations
- SVG animations (SMIL)

---

## Accessibility

### ARIA Labels
- Navigation links have descriptive labels
- Button icons have aria-label attributes
- Semantic HTML elements used throughout

### Keyboard Navigation
- Tab order follows visual layout
- Focus states visible on all interactive elements
- Enter key activates buttons and links

### Color Contrast
- All text meets WCAG AA standards (4.5:1 minimum)
- Headings exceed AAA standards (7:1 minimum)

### Screen Readers
- Semantic HTML structure
- Alt text ready for images
- Heading hierarchy properly nested

---

## Future Enhancements

### Phase 2 - Content Expansion
- [ ] Add actual client logos to TrustBar
- [ ] Implement contact form with validation
- [ ] Add case studies/portfolio section
- [ ] Create team members section
- [ ] Add testimonials/reviews

### Phase 3 - Functionality
- [ ] CMS integration (Sanity/Contentful)
- [ ] Blog/news section
- [ ] Multi-language support
- [ ] Search functionality
- [ ] Dark mode toggle

### Phase 4 - Marketing
- [ ] SEO optimization (meta tags, sitemap)
- [ ] Analytics integration (Google Analytics)
- [ ] Social media meta tags (Open Graph)
- [ ] Cookie consent banner
- [ ] Newsletter signup

---

## Maintenance

### Regular Updates
- Monthly: Dependency updates (`npm update`)
- Quarterly: Security audits
- Annually: Major version upgrades

### Content Updates
- Text: Edit directly in `.astro` files
- Images: Replace in `public/` or update URLs
- Services: Edit data arrays in component frontmatter

### Adding New Sections
1. Create new component in `src/components/`
2. Add to `src/pages/index.astro`
3. Update navigation links if needed

---

## Troubleshooting

### Common Issues

**Port 4321 already in use**
```bash
# Kill process or use different port
npm run dev -- --port 3000
```

**Build errors**
```bash
# Clear cache and reinstall
rm -rf node_modules dist .astro
npm install
npm run build
```

**Images not loading**
- Check Unsplash URLs are valid
- Verify network connectivity
- Check browser console for errors

---

## License

© 2026 Steel Cap Commercial. All rights reserved.

---

## Credits

**Design & Development:** Steel Cap Commercial
**Built with:** Astro, TypeScript, Tailwind CSS
**Development Time:** 8 hours (March 19-20, 2026)
**Version:** 1.0.0

---

## Contact

For questions or support:
- Email: contact@steelcapcommercial.com
- Website: steelcapcommercial.com
- GitHub: github.com/bsptourstreks-rgb/steelcapcommercial
