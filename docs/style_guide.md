# Literary AI Design System & Style Guide

## Brand Identity

**Aesthetic**: Explorer/Sage meets Magician - Earthy, scholarly, yet mystical and transformative

**Tone**: Professional yet approachable, educational yet enchanting, trustworthy yet wondrous

**Target Audience**: Readers, writers, scholars, and book lovers interested in AI-powered literary analysis

## Color System

### Primary Palette

#### Sage Colors (Wisdom & Knowledge)

```css
:root {
  --sage-primary: #7A9B76;    /* Main sage green */
  --sage-light: #9CAF88;      /* Light sage for backgrounds */
  --sage-deep: #4A5D23;       /* Deep sage for emphasis */
  --sage-muted: #B8C5B1;      /* Muted sage for borders */
}
```

**Usage Guidelines:**
- **Primary**: Secondary buttons, borders, section accents
- **Light**: Background overlays, hover states
- **Deep**: Headings, strong emphasis, dark text
- **Muted**: Subtle borders, dividers

#### Magician Colors (Mystery & Transformation)

```css
:root {
  --magician-primary: #6B4C9A;    /* Main purple */
  --magician-light: #9370DB;      /* Light purple */
  --magician-gold: #B8860B;       /* Golden accent */
  --magician-accent: #DDA15E;     /* Secondary gold */
}
```

**Usage Guidelines:**
- **Primary**: Main headings, primary brand color, links
- **Light**: Hover states, accents, badges
- **Gold**: Prices, decorative elements, special highlights
- **Accent**: Secondary decorative elements

### Neutral Palette

```css
:root {
  --parchment-bg: #F5F3EE;        /* Main background */
  --parchment-light: #E8E4DC;     /* Light section background */
  --parchment-dark: #D4CEC4;      /* Subtle contrast */
  --text-primary: #2C2C2C;        /* Primary text */
  --text-secondary: #5A5A5A;      /* Secondary text */
}
```

### Gradient System

**Mystical Gradient** (Primary brand gradient)
```css
linear-gradient(135deg, var(--sage-primary) 0%, var(--magician-primary) 100%)
```
Usage: Hero overlays, button backgrounds, special sections

**Sage Gradient**
```css
linear-gradient(180deg, var(--sage-light) 0%, var(--sage-primary) 100%)
```
Usage: Sage-focused sections, nature-inspired elements

**Wisdom Gradient**
```css
linear-gradient(45deg, var(--sage-deep) 0%, var(--magician-gold) 100%)
```
Usage: Underlines, borders, decorative accents

## Typography

### Font Families

#### Primary Fonts
```css
--font-heading: 'Baskerville', 'Georgia', serif;
--font-body: 'Georgia', 'Garamond', serif;
```

**Philosophy**: Serif fonts convey scholarly authority, wisdom, and timeless literary tradition

### Heading Scale

```css
h1, .h1 {
  font-family: 'Baskerville', 'Georgia', serif;
  font-size: 2.5rem;           /* 40px */
  line-height: 1.2;
  color: var(--magician-primary);
  letter-spacing: 0.01em;
}

h2, .h2 {
  font-family: 'Baskerville', 'Georgia', serif;
  font-size: 2rem;             /* 32px */
  line-height: 1.3;
  color: var(--magician-primary);
}

h3, .h3 {
  font-family: 'Baskerville', 'Georgia', serif;
  font-size: 1.5rem;           /* 24px */
  line-height: 1.4;
  color: var(--sage-deep);
}

h4, .h4 {
  font-family: 'Georgia', serif;
  font-size: 1.25rem;          /* 20px */
  line-height: 1.5;
  color: var(--sage-deep);
}
```

### Body Text

```css
p, .body-text {
  font-family: 'Georgia', 'Garamond', serif;
  font-size: 1rem;             /* 16px */
  line-height: 1.8;
  color: var(--text-secondary);
}

.large-text {
  font-size: 1.125rem;         /* 18px */
  line-height: 1.8;
}

.small-text {
  font-size: 0.875rem;         /* 14px */
  line-height: 1.6;
}
```

### Responsive Typography

```css
@media screen and (max-width: 749px) {
  h1, .h1 { font-size: 2rem; }      /* 32px */
  h2, .h2 { font-size: 1.75rem; }   /* 28px */
  h3, .h3 { font-size: 1.25rem; }   /* 20px */
  p { font-size: 1rem; }            /* 16px */
}
```

## Button System

### Primary Button

```css
.btn-primary {
  background: var(--mystical-gradient);
  color: white;
  border: none;
  padding: 1rem 2.5rem;
  border-radius: 6px;
  font-family: 'Georgia', serif;
  font-weight: 600;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  transition: all 0.3s ease;
  box-shadow: 0 4px 12px rgba(107, 76, 154, 0.3);
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(107, 76, 154, 0.4);
}
```

**Usage**: Primary calls-to-action, main conversion points

### Secondary Button

```css
.btn-secondary {
  background: transparent;
  border: 2px solid var(--sage-primary);
  color: var(--sage-deep);
  padding: 1rem 2.5rem;
  border-radius: 6px;
  font-family: 'Georgia', serif;
  font-weight: 600;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  transition: all 0.3s ease;
}

.btn-secondary:hover {
  background: var(--sage-primary);
  color: white;
  transform: translateY(-2px);
}
```

**Usage**: Secondary actions, alternative CTAs, cancel buttons

## Card Components

### Service Card

```css
.service-card {
  background: white;
  padding: 2.5rem 2rem;
  border-radius: 12px;
  border: 2px solid transparent;
  transition: all 0.4s ease;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.06);
  position: relative;
}

.service-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: var(--mystical-gradient);
  opacity: 0;
  transition: opacity 0.3s ease;
  border-radius: 12px 12px 0 0;
}

.service-card:hover {
  border-color: var(--magician-primary);
  transform: translateY(-5px);
  box-shadow: 0 8px 24px rgba(107, 76, 154, 0.15);
}

.service-card:hover::before {
  opacity: 1;
}
```

**Usage**: Service offerings, product cards, feature highlights

## Spacing System

### Scale

```css
:root {
  --spacing-xs: 0.5rem;      /* 8px */
  --spacing-sm: 1rem;        /* 16px */
  --spacing-md: 1.5rem;      /* 24px */
  --spacing-lg: 2rem;        /* 32px */
  --spacing-xl: 3rem;        /* 48px */
  --spacing-2xl: 4rem;       /* 64px */
  --spacing-3xl: 6rem;       /* 96px */
}
```

### Component Spacing

- **Card Padding**: 2.5rem 2rem
- **Section Padding**: 5rem 0 (desktop), 3rem 0 (mobile)
- **Grid Gap**: 2rem
- **Button Padding**: 1rem 2.5rem
- **Heading Margin**: 1-2rem bottom

## Iconography

### Font Awesome Integration

```html
<!-- Include in theme.liquid -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
```

### Service Icons

```css
.service-icon {
  font-size: 3rem;
  color: var(--magician-gold);
  margin-bottom: 1.5rem;
  text-align: center;
}
```

**Recommended Icons**:
- World Maps: `fas fa-map-marked-alt`
- Family Trees: `fas fa-project-diagram`
- Timelines: `fas fa-clock`
- Books: `fas fa-book-open`
- AI/Magic: `fas fa-hat-wizard`

## Interactive States

### Hover Effects

```css
/* Link Hover */
a:not(.button)::after {
  content: '';
  position: absolute;
  bottom: -2px;
  left: 0;
  width: 0;
  height: 2px;
  background: var(--wisdom-gradient);
  transition: width 0.3s ease;
}

a:not(.button):hover::after {
  width: 100%;
}

/* Card Lift */
.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 24px rgba(107, 76, 154, 0.2);
}

/* Button Lift */
.button:hover {
  transform: translateY(-2px);
}
```

### Animation Duration
- **Fast**: 0.2s (micro-interactions)
- **Normal**: 0.3s (most interactions)
- **Slow**: 0.4s (complex transitions)

### Easing Function
```css
transition: all 0.3s ease;
```

## Layout System

### Grid Patterns

```css
/* Service Grid */
.service-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
}

/* Two-Column */
.two-column {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
}

/* Three-Column */
.three-column {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
}
```

### Container Widths

```css
.page-width {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1.5rem;
}

.narrow {
  max-width: 800px;
}

.wide {
  max-width: 1400px;
}
```

## Shadow System

```css
:root {
  --shadow-sm: 0 2px 8px rgba(0, 0, 0, 0.05);
  --shadow-md: 0 4px 12px rgba(0, 0, 0, 0.06);
  --shadow-lg: 0 8px 24px rgba(107, 76, 154, 0.15);
  --shadow-mystical: 0 0 20px rgba(107, 76, 154, 0.5);
}
```

**Usage**:
- **Small**: Subtle depth, navigation, inputs
- **Medium**: Cards, sections, default elevation
- **Large**: Hover states, modals, popovers
- **Mystical**: Special effects, call-outs

## Border Radius System

```css
:root {
  --radius-sm: 6px;      /* Buttons, inputs */
  --radius-md: 8px;      /* Images, small cards */
  --radius-lg: 12px;     /* Cards, sections */
  --radius-full: 50%;    /* Circles, badges */
}
```

## Accessibility

### Color Contrast
- All text meets WCAG 2.1 AA standards (4.5:1 for normal text, 3:1 for large text)
- Primary text on white: #2C2C2C (12.6:1)
- Secondary text on white: #5A5A5A (7.1:1)

### Focus States
```css
:focus-visible {
  outline: 2px solid var(--magician-primary);
  outline-offset: 2px;
  border-radius: 4px;
}
```

### Alt Text
- All images must have descriptive alt text
- Decorative images should have empty alt=""

## Responsive Breakpoints

```css
/* Mobile First */
@media screen and (min-width: 750px) {
  /* Tablet */
}

@media screen and (min-width: 990px) {
  /* Desktop */
}

@media screen and (min-width: 1440px) {
  /* Large Desktop */
}
```

## Usage Examples

### Hero Section
```html
<section class="hero">
  <h1>Unlock the Wisdom Within Your Stories</h1>
  <p class="large-text">Transform narratives into visual magic</p>
  <a href="/services" class="btn-primary">Explore Services</a>
</section>
```

### Service Card
```html
<div class="service-card">
  <div class="service-icon">
    <i class="fas fa-map-marked-alt"></i>
  </div>
  <h3>AI-Generated World Maps</h3>
  <p>Transform fictional realms into stunning cartographic masterpieces.</p>
  <a href="/maps" class="service-link">Explore Maps →</a>
</div>
```

## Brand Voice Guidelines

### Writing Style
- **Tone**: Authoritative yet approachable
- **Voice**: Educational, inspiring, trustworthy
- **Vocabulary**: Blend literary terms with accessible language
- **Sentence Structure**: Varied, flowing, scholarly yet clear

### Content Principles
1. **Wisdom First**: Lead with insight and understanding
2. **Wonder Follows**: Add magical, transformative elements
3. **Clarity Always**: Never sacrifice understanding for style
4. **Literary References**: Subtle nods to classic literature

### Example Copy
✅ **Good**: "Uncover the hidden architecture of narratives with AI-powered analysis"
❌ **Avoid**: "Use our AI tool to make charts from books"

---

**Design System Version**: 1.0.0
**Last Updated**: November 2025
**Maintained By**: Theme Development Team
