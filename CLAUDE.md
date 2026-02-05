# CLAUDE.md - The Chapel Event Venue Website

## Project Overview

This is a static HTML/CSS website for **The Chapel**, a premier event venue located at 610 S Dakota Ave, Sioux Falls, SD 57104. The venue hosts weddings, corporate events, and family gatherings.

**Website:** www.sfchapel.com
**Phone:** (605) 376-1847

## Technology Stack

- **HTML5** - Semantic markup with accessibility features
- **CSS3** - External stylesheet with CSS custom properties (variables)
- **No build tools** - Pure static files, no bundlers or preprocessors
- **No JavaScript** - Currently a JS-free static site
- **No package manager** - No npm, yarn, or dependencies

## Project Structure

```
sf-chap/
├── CLAUDE.md           # This file - AI assistant guide
├── README.md           # Basic project readme
├── styles.css          # Single stylesheet with all styles
├── index.html          # Homepage
├── events.html         # Host Your Event overview
├── venue.html          # Venue Features page
├── packages.html       # Packages & Pricing
├── about.html          # About The Chapel
├── contact.html        # Contact forms (tour & booking)
├── weddings.html       # Wedding-specific information
├── corporate.html      # Corporate events information
├── family.html         # Family gatherings information
├── privacy.html        # Privacy Policy
└── terms.html          # Terms & Conditions
```

## Page Architecture

Every HTML page follows this consistent structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>[Page Title] | The Chapel</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="description" content="[SEO description]">
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <a href="#main-content" class="skip-link">Skip to main content</a>

  <header role="banner">...</header>
  <nav role="navigation" aria-label="Main navigation">...</nav>
  <main id="main-content" role="main">...</main>
  <footer role="contentinfo">...</footer>
</body>
</html>
```

## CSS Architecture

### CSS Variables (Custom Properties)

All theming uses CSS variables defined in `:root`. The color scheme is:
- **Arctic White, Slate, Gold, Natural Wood Tones, Charcoal**

Key variables:
```css
--color-primary: #4A5B6F;     /* Darker slate */
--color-accent: #B8941F;       /* Darker gold */
--color-dark: #2C3639;         /* Charcoal */
--color-text: #2C3639;         /* Text color */
--color-background: #F5F1E8;   /* Warm cream */
--color-card: #FAFBFC;         /* Arctic white */
--color-white: #FFFFFF;        /* Pure white */
```

### Key CSS Classes

| Class | Purpose |
|-------|---------|
| `.hero` | Hero section with centered content |
| `.grid` | Flexbox grid for card layouts |
| `.event-card` | Card with gold left border accent |
| `.testimonial-card` | Card for quotes/testimonials |
| `.cta` | Primary call-to-action button |
| `.cta-primary` | Primary header CTA |
| `.cta-secondary` | Secondary/outline button |
| `.cta-section` | Full-width CTA banner section |
| `.faq-list` / `.faq-item` | FAQ styling |
| `.link-primary` | Styled internal link |
| `.link-primary-bold` | Bold styled link |

## Accessibility Standards (WCAG 2.1 Level AA)

This site implements comprehensive accessibility features:

### Required Elements
- Skip link: `<a href="#main-content" class="skip-link">Skip to main content</a>`
- ARIA landmarks: `role="banner"`, `role="navigation"`, `role="main"`, `role="contentinfo"`
- Current page indicator: `aria-current="page"` on active nav link
- Labeled regions: `aria-label` and `aria-labelledby` on sections
- Form accessibility: `aria-required="true"`, proper `<label>` associations

### Focus Management
- Visible focus indicators: 3px solid outline
- Focus-visible for keyboard-only focus
- Minimum touch target: 44x44px

### Color Contrast
- All colors meet WCAG AA 4.5:1 contrast ratio
- Text uses `--color-text: #2C3639` on light backgrounds

## Navigation Structure

Main navigation links (in order):
1. Home (`index.html`)
2. Host Your Event (`events.html`)
3. Venue Features (`venue.html`)
4. Packages & Pricing (`packages.html`)
5. About (`about.html`)
6. Contact (`contact.html`)

Secondary pages (linked from main pages):
- `weddings.html` - Wedding details
- `corporate.html` - Corporate event details
- `family.html` - Family gathering details

Footer pages:
- `privacy.html` - Privacy Policy
- `terms.html` - Terms & Conditions

## Business Information (Keep Consistent)

When editing content, maintain these exact details:

- **Venue Name:** The Chapel
- **Tagline:** Sioux Falls' Premier Event Venue
- **Address:** 610 S Dakota Ave, Sioux Falls, SD 57104
- **Phone:** (605) 376-1847
- **Website:** www.sfchapel.com
- **Email:** contact@sfchapel.com
- **Copyright Year:** 2026

## Content Guidelines

### Tone & Voice
- Professional yet warm and welcoming
- Focus on creating "unforgettable moments" and "memories"
- Emphasize historic elegance combined with modern amenities
- Highlight personalized service and attention to detail

### Event Types (Three Main Categories)
1. **Weddings** - Ceremonies, receptions, intimate to grand celebrations
2. **Corporate Events** - Conferences, retreats, meetings, team-building
3. **Family Gatherings** - Reunions, birthdays, anniversaries, parties

### Pricing (Reference Only)
- Wedding packages: $3,500 - $10,000+
- Corporate packages: $1,200 - $6,000+
- Family packages: $800 - $3,500+

## Development Workflow

### Making Changes

1. **Edit HTML files directly** - No compilation needed
2. **CSS changes** - All styles in `styles.css`
3. **Test locally** - Open HTML files in browser
4. **Check responsiveness** - Mobile breakpoint at 600px
5. **Validate accessibility** - Ensure ARIA labels, focus states

### Common Tasks

**Add a new page:**
1. Copy an existing HTML file as template
2. Update `<title>` and `<meta name="description">`
3. Update `aria-current="page"` in navigation
4. Follow the standard page structure

**Modify navigation:**
- Update `<nav>` in ALL HTML files (12 total)
- Maintain `aria-current="page"` on correct link per page

**Update colors/theming:**
- Modify CSS variables in `:root` section of `styles.css`
- Ensure WCAG AA contrast compliance

**Add new section:**
- Use semantic HTML (`<section>` with `aria-labelledby`)
- Apply existing CSS classes (`.grid`, `.event-card`, etc.)

## Testing Checklist

Before committing changes:

- [ ] All HTML pages load without errors
- [ ] Navigation works on all pages
- [ ] `aria-current="page"` is set correctly
- [ ] Forms have proper labels and required attributes
- [ ] Images have alt text (when added)
- [ ] Links are not broken
- [ ] Mobile responsive (test at 600px width)
- [ ] Color contrast meets WCAG AA
- [ ] Skip link works and is visible on focus

## Git Workflow

- Main branch contains production-ready code
- Feature branches for significant changes
- Commit messages should be descriptive
- No build step required before committing

## File Naming Conventions

- Lowercase filenames
- Hyphens for multi-word names (e.g., `privacy.html`)
- Single `styles.css` for all styles
- No JavaScript files currently

## Important Notes for AI Assistants

1. **Accessibility is mandatory** - Never remove ARIA attributes or skip links
2. **Consistency is key** - All pages must follow the same structure
3. **No frameworks** - Keep it pure HTML/CSS
4. **Update all pages** - Navigation changes require editing all 12 HTML files
5. **Preserve business info** - Keep phone, address, and branding exact
6. **Test contrast** - Color changes must maintain WCAG AA compliance
7. **Mobile-first consideration** - CSS includes responsive breakpoint at 600px

## Common Patterns

### Section with Grid Cards
```html
<section aria-labelledby="section-heading">
  <h2 id="section-heading">Section Title</h2>
  <div class="grid">
    <div class="event-card">
      <h3>Card Title</h3>
      <p>Card content...</p>
    </div>
    <!-- More cards -->
  </div>
</section>
```

### CTA Section
```html
<section aria-labelledby="cta-heading" class="cta-section">
  <h2 id="cta-heading">Call to Action Title</h2>
  <p>Description text...</p>
  <div class="cta-buttons">
    <a href="contact.html#tour" class="cta">Primary CTA</a>
    <a href="contact.html#book" class="cta cta-secondary-large">Secondary CTA</a>
  </div>
</section>
```

### FAQ Item
```html
<div class="faq-list">
  <div class="faq-item">
    <h3>Question?</h3>
    <p>Answer text...</p>
  </div>
</div>
```
