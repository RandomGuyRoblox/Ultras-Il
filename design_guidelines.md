# Gaming Store Design Guidelines

## Design Approach
**Reference-Based: Gaming Platform Aesthetic**
Drawing inspiration from Steam, Epic Games Store, and modern gaming platforms. Focus on immersive, high-energy visuals with bold typography and sleek interfaces that appeal to gaming audiences.

## Typography System
- **Primary Font**: Rajdhani (Google Fonts) - Angular, futuristic gaming feel
- **Secondary Font**: Inter (Google Fonts) - Clean readability for body text
- **Hierarchy**: 
  - Hero headlines: 6xl-8xl, extrabold, uppercase
  - Section titles: 4xl-5xl, bold
  - Product names: 2xl-3xl, semibold
  - Body text: base-lg, regular-medium
  - UI elements: sm-base, medium

## Layout System
**Spacing Primitives**: Use Tailwind units of 3, 4, 6, 8, 12, 16
- Consistent section padding: py-16 to py-24 (desktop), py-8 to py-12 (mobile)
- Component gaps: gap-6 to gap-8
- Card padding: p-6 to p-8

## Page Structure

### Homepage
1. **Immersive Hero** (80vh)
   - Full-width video background or large hero image with parallax effect
   - Overlaid headline + subheadline + dual CTAs ("Browse Games" + "Join Discord")
   - Background blur treatment on buttons (backdrop-blur-md)
   - Animated scanline or grid overlay for tech feel

2. **Featured Games Grid** 
   - 3-column grid (lg), 2-column (md), 1-column (mobile)
   - Large product cards with hover lift animations
   - Each card: game artwork, title, price, genre tags, "Add to Cart" CTA

3. **New Releases Carousel**
   - Horizontal scrolling showcase
   - 4-5 visible items with smooth scroll behavior
   - Quick-view modal trigger on click

4. **Discord Community Integration**
   - Split section: left side Discord embed/stats widget, right side benefits/CTA
   - Live member count, online status
   - "Join Server" prominent button

5. **Popular Categories**
   - 4-column icon grid showcasing game genres
   - Each with icon, category name, game count

6. **Footer**
   - 4-column layout: Quick Links, Support, Community (Discord, Social), Newsletter signup
   - Payment method logos (PayPal, KashKash)
   - Legal links

### Gallery Page
- Masonry grid layout (Isotope-style)
- Filterable by game, genre, media type (screenshots, artwork, videos)
- Lightbox expansion on click
- Infinite scroll or load more pagination

### Product Detail
- Split layout: Left 60% (image gallery carousel), Right 40% (product info, price, add to cart)
- Tabbed content below: Description, System Requirements, Reviews
- Related games grid at bottom

### Checkout Flow
**Cart Page**:
- Line items list with thumbnails, quantity controls, remove option
- Running total sidebar with discount code input
- Continue shopping vs. proceed to checkout CTAs

**Payment Page**:
- Multi-step progress indicator (Cart > Shipping > Payment > Confirm)
- Payment method selection cards (PayPal logo + KashKash logo)
- Guest checkout vs. account creation toggle
- Order summary sidebar (sticky on desktop)

## Component Library

### Navigation
- Fixed header with logo left, main nav center, cart/account right
- Search bar integration with autocomplete dropdown
- Mobile: hamburger menu with full-screen overlay

### Product Cards
- Aspect ratio 3:4 for consistency
- Hover state: scale transform, overlay gradient reveal with quick actions
- Price badge, platform icons, wishlist heart icon

### Buttons
- Primary: Large, rounded-lg, uppercase text, semibold
- Secondary: Outline style with hover fill
- Icon buttons: Square with icon centering
- Disabled state: reduced opacity

### Forms
- Floating labels pattern
- Full-width inputs with border focus states
- Checkbox/radio with custom styled controls
- Validation messaging inline

### Modals/Overlays
- Centered overlay with backdrop blur
- Quick view product modals for gallery
- Cart slide-out drawer from right

## Images Section

**Hero Image**: 
Full-width 1920x1080 dynamic gaming montage featuring popular game characters/scenes in action poses. High-energy, dramatic lighting. Place as background of hero section with subtle zoom animation on load.

**Product Images**: 
Each game requires 4-5 images minimum:
- Box art/key art (primary)
- 3-4 gameplay screenshots
Aspect ratio 16:9, high resolution. Place in product cards and detail page gallery.

**Category Icons**:
Use SVG icons from gaming icon set for genre categories (controller, sword, racing wheel, etc.). Place in category grid section.

**Gallery Assets**:
Mix of game screenshots, concept art, promotional artwork. Varied aspect ratios for masonry effect. Minimum 30+ images for gallery page.

**Discord Integration**:
Discord logo and server preview image. Place in community section.

**Footer Images**:
Payment provider logos (PayPal, KashKash), social media icons.

---

**Critical**: This design emphasizes immersive visuals, bold typography hierarchy, and seamless gaming-focused UX. Every interaction should feel premium and purposeful, matching the energy of modern gaming platforms.