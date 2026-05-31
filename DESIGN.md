# DESIGN.md: Renée Crown Wellness Institute — Science + Love

## Source
- **URL:** https://crowninstitute.colorado.edu/science-love
- **Capture date:** 2026-05-31
- **Platform:** Webflow (site ID: `68c765dc6f6cbe3ff5c38be2`)
- **Design by:** Studio DAD + Perennial Strategy (brand)
- **Awwwards:** Nominee — rated up to 9.0/10 for creativity and content
- **Evidence:** WebFetch page scrape × 3 passes, agent web research, CDN asset enumeration

---

## Design Summary

Clean institutional wellness aesthetic. Minimal UI chrome (black, white, teal) lets warm, human-centered photography carry the emotional weight. The page is structured as a narrative: conviction → evidence → invitation. Typography is modern geometric sans-serif with oversized display headings. Spacing is generous and deliberate — airy, not empty. Animation is restrained (carousel fades, scroll reveals). The overall feel is: academic credibility + human warmth, never corporate.

---

## Design Tokens

### Colors

| Role | Value | Notes |
|------|-------|-------|
| Text primary | `#000000` | All body and heading text |
| Background | `#FFFFFF` | Main page background |
| Background alt | `#F5F5F5`–`#FAFAFA` | Section separators, subtle alternating blocks — **inferred** |
| Accent / CTA | `~#00857D` | Teal used on all buttons and links — **inferred from institution aesthetic; exact hex not extractable from Webflow without CSS access** |
| Accent hover | `~#006B63` | Darker teal on hover — **inferred** |
| Footer background | `~#F0F0F0` | Light gray — **inferred** |
| Border / divider | `~#E0E0E0` | Subtle separators — **inferred** |
| Photography | warm earth tones | Golden hour, natural greens, skin tones — photography carries all chromatic warmth |

**Design philosophy:** UI stays neutral. Color lives in photography. The teal accent is used sparingly (buttons, active links, logo) — never as background fills for large sections.

### Typography

| Element | Style | Size (desktop) | Weight |
|---------|-------|----------------|--------|
| Hero heading (H1) | Geometric sans-serif | `clamp(40px, 5vw, 64px)` | 700–900 |
| Section heading (H2) | Same family | `clamp(28px, 3.5vw, 44px)` | 700 |
| Sub-heading (H3) | Same family | `clamp(20px, 2.5vw, 32px)` | 600 |
| Body copy | Same family, lighter | `16px–18px` | 400 |
| Caption / attribution | Same family | `14px` | 400–500 |
| Button label | Same family | `16px` | 600–700 |

**Font family:** Not extractable from Webflow directly. Visual style matches **geometric humanist sans-serif** — strong candidates: `Inter`, `Avenir Next`, `DM Sans`, `Plus Jakarta Sans`. Use `system-ui, -apple-system, sans-serif` as fallback. If replicating: `Inter` is the safest open-source match.

**Heading style:** All-lowercase or mixed-case (not all-caps). The hero headline uses a period at the end — deliberate, considered tone.

### Spacing and Layout

**Base unit:** `8px`

**Spacing scale:** `8, 16, 24, 32, 40, 48, 64, 80, 96, 128px`

| Element | Value |
|---------|-------|
| Container max-width | `~1200px` (centered) |
| Section vertical padding | `80px–128px` desktop, `48px–64px` mobile |
| Card internal padding | `24px–32px` |
| Grid gap | `24px–32px` |
| Nav height | `~72px` |
| Border radius (cards) | `4px`–`8px` subtle |
| Border radius (buttons) | `4px`–`6px` |
| Box shadow (cards) | `0 2px 8px rgba(0,0,0,0.08)` — **inferred** |

**Grid:** 12-column. Card grids collapse 4-col → 2-col → 1-col across breakpoints.

**Responsive breakpoints (Webflow defaults):**
- Desktop: `1440px+`
- Tablet: `768px–1199px`  
- Mobile: `< 768px`

---

## Components

### Navigation Bar
- Position: **fixed top**, full width
- Background: `#FFFFFF` with subtle bottom shadow on scroll
- Left: CU Boulder logo (institutional) + Crown Institute logo (brand)
- Center-right: Primary nav links (`Science + Love`, `Learn`, `Research`, `News & Events`, `Partner With Us`, `About`)
- Right: Language selector dropdown + `Donate` button (teal, always visible)
- Nav links: black text, hover state changes to teal
- Mobile: hamburger toggle, full-screen slide-out or dropdown

### Hero Section
- **Layout:** Text left or centered, carousel of 4 community photos
- **Heading:** `"Our conviction: Science + love work better together."` — large, bold, black
- **Body:** 2–3 sentence paragraph, 16–18px, lighter weight
- **Images:** Full-bleed carousel (`.webp` format), warm lifestyle photography
- **No text overlay on images** — text and images appear to be in a split or stacked layout, not overlaid
- **Carousel:** Auto-play or manual, Previous/Next arrow buttons, smooth fade transition

**Hero images (from CDN):**
```
thrive-1.webp — adult and child gardening
thrive-2.webp — young adults embracing  
thrive-3.webp — girls in school hallway
thrive-4.webp — girl near garden beds
```

### Carousel (Core Values / Principles)
- **Previous / Next** arrow navigation
- Each slide: heading + body paragraph (no image in slide itself, or small contextual image)
- Smooth fade or slide-left transition
- Pagination dots: **not confirmed** — may use only arrows

### Team Profile Card
- Layout: **vertical** — circular headshot (~150–200px diameter) above name + title + quote + bio
- Grid: 3–4 columns desktop, 2 tablet, 1 mobile
- Photo: circular crop, warm color-graded
- Name: bold, 18–20px
- Title: italic or lighter weight, 14–16px, teal or dark gray
- Quote: larger text (20–24px), italic or normal weight, black
- Bio: 16px, regular weight, gray `#555`

### Buttons

**Primary (Donate, Sign Up, Learn More):**
```css
background: #00857D; /* teal — inferred */
color: #FFFFFF;
padding: 12px 28px;
border-radius: 5px;
font-weight: 600;
font-size: 16px;
border: none;
transition: background 0.2s ease;
```
Hover: `background: #006B63`

**Secondary / text link:**
```css
color: #00857D;
text-decoration: underline; /* or none with hover underline */
font-weight: 500;
```

**Donate button in nav:**
- Same teal style, slightly smaller padding
- Persistent — always in viewport

### Blockquote / Featured Quote
- Full-width section, white background
- Large quote text: `28–36px`, regular or italic weight, black
- Attribution below: name + credentials, 14–16px, lighter weight
- No quotation mark glyphs visible — text stands alone with visual scale

### Sign-Up CTA Section
- Background: white or very light neutral
- Heading: `"The Crown Institute is always growing, learning, and evolving."`
- Body: short paragraph
- Mailchimp embed or button linking to `mailchi.mp/colorado/join-our-mailing-list`
- `Sign Up` button: primary teal style

### Footer
```
[Logo]  [Donate button]

Science + Love | Research | News & Events

Learn:              Partner With Us:     About:
For Kids & Teens    For Donors           Mission, Vision & Values
For Families        For Implementers     Our Team
For Educators       For Young People     Our Work to Date
For CU Students     Families & Educators For Press
                                         Contact

Job Opportunities | Join our Mailing List

[Instagram] [LinkedIn] [YouTube]

© Regents of the University of Colorado
Privacy · Legal & Trademarks · Campus Map
```
- Background: light gray `#F0F0F0` — **inferred**
- Link color: dark gray or black, hover → teal
- 5-column desktop grid, stacks on mobile

---

## Page Patterns

**Section order (top to bottom):**
1. Fixed nav
2. Hero (conviction statement + carousel)
3. Problem framing paragraph ("Kids are struggling…")
4. Core principles carousel (6 principles)
5. Large featured quote (Sona Dimidjian)
6. "We invite you to join us" — team profiles carousel (6 people)
7. Results/evidence CTA ("Evidence, programs, and practices…")
8. Community invite + mailing list sign-up
9. Footer

**Alternating section backgrounds:** White ↔ very light gray/off-white to create visual breathing room without hard dividers.

**No decorative dividers** — section breaks are purely spatial (padding/margin).

**Full-bleed images:** Hero carousel images go edge-to-edge. Team headshots are contained within cards.

---

## Content Style

**Voice:** Warm academic. Long-form sentences. Conviction language ("Our conviction:", "That's why we choose…"). Ends statements with impact ("...we'd simply call… Love.").

**Heading pattern:** Declarative statements, not questions. Periods at end of headlines. Mixed case, never all-caps.

**CTA copy:** Low-pressure ("Sign Up", "Learn More", "Join Us") — never pushy or sales-y.

**Body copy density:** Medium — 2–4 sentences per paragraph. Ample whitespace between blocks.

**Attribution style:** Full name + credentials (PhD, JD) + full title + institution. Signals academic credibility.

---

## Image Assets (Live CDN URLs)

**Site logos:**
- CU Boulder: `https://cdn.prod.website-files.com/68c765dc6f6cbe3ff5c38be2/68f935bd1c85faf73b566838_cu-boulder-logo-text-black.svg`
- Crown Institute: `https://cdn.prod.website-files.com/68c765dc6f6cbe3ff5c38be2/68ccac1252cbf31dded73dfe_crown-logo-main.svg`

**Hero carousel images:**
- `https://cdn.prod.website-files.com/68c765dc6f6cbe3ff5c38be2/690d0509cbf623ae37710a69_thrive-1.webp`
- `https://cdn.prod.website-files.com/68c765dc6f6cbe3ff5c38be2/690d050987f73fceb5a29caf_thrive-2.webp`
- `https://cdn.prod.website-files.com/68c765dc6f6cbe3ff5c38be2/690d050921be1bd84b188801_thrive-3.webp`
- `https://cdn.prod.website-files.com/68c765dc6f6cbe3ff5c38be2/690d050929d254f27e12507c_thrive-4.webp`

**Body / tracking images (from sub-site ID `68d087abd913fc58d655f25f`):**
- `…69768eac…_trackimg-1.webp`
- `…69768edd…_trackimg-2.webp`
- `…69768efd…_trackimg-3.webp`
- Stocksy photo: `…Stocksy_txp5538dae7bqo200_Medium_1501620 copy.webp`
- Matthew Smith Unsplash: `…matthew-smith-Rfflri94rs8-unsplash.webp`

**Headshots:**
- Sona Dimidjian: `…6910f7c4aa9fc599d8c7ffbc_sona-dimidjian.webp`
- Sharon Salzberg: `…69125a9829f004f658293c2b_sharon-salzberg.webp`
- Anahi Collado: `…691259dc9bf139cfbc385f8b_anahi-collado.webp`
- Thupten Jinpa: `…693717a8…_TJ-Zoksang-phto-square….webp`
- Joanna Arch: `…69125a45…_joanna-arch.webp`
- Michele Simpson: `…69125a73…_michele-simpson.webp`
- Julie Arbuckle: `…69125ab3…_Julie-Arbuckle-Headshot-2.webp`

> **Note:** Do not use these images in production — they are third-party assets hosted on the Crown Institute's Webflow CDN. Replace with licensed originals or placeholders.

---

## Agent Build Instructions

To build a product page in this style:

1. **Stack:** Plain HTML/CSS (or React + Tailwind). No Webflow required.

2. **Font:** Load `Inter` from Google Fonts (or system-ui fallback):
   ```html
   <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
   ```

3. **CSS variables:**
   ```css
   :root {
     --color-text: #000000;
     --color-bg: #ffffff;
     --color-bg-alt: #f7f7f5;
     --color-accent: #00857D;
     --color-accent-hover: #006B63;
     --color-muted: #555555;
     --font-base: 'Inter', system-ui, sans-serif;
     --space-xs: 8px;
     --space-sm: 16px;
     --space-md: 32px;
     --space-lg: 64px;
     --space-xl: 128px;
     --container: 1200px;
     --radius: 5px;
   }
   ```

4. **Page structure (semantic HTML):**
   ```
   <header> — fixed nav
   <main>
     <section class="hero"> — conviction statement + image carousel
     <section class="problem"> — problem framing paragraph
     <section class="principles"> — 6-item carousel
     <section class="quote"> — featured blockquote
     <section class="team"> — profile cards carousel
     <section class="cta-links"> — program links
     <section class="signup"> — mailing list
   </main>
   <footer>
   ```

5. **Carousel:** Use `embla-carousel` (lightweight, no jQuery) or CSS scroll-snap. Previous/Next arrows only — no pagination dots needed.

6. **Scroll animations:** Use `IntersectionObserver` with a simple `fade-in` class:
   ```css
   .fade-in { opacity: 0; transform: translateY(20px); transition: opacity 0.5s ease, transform 0.5s ease; }
   .fade-in.visible { opacity: 1; transform: none; }
   ```

7. **Hero layout:** 50/50 split on desktop (text left, carousel right). Stack vertically on mobile (text above, images below).

8. **Profile cards:** CSS Grid, `repeat(auto-fill, minmax(240px, 1fr))`, `gap: 32px`. Circular images via `border-radius: 50%`.

9. **Tone check:** Every headline should end in a period. Avoid marketing superlatives. Lead with conviction, not feature lists.

---

## Rerun Inputs
```yaml
workflow: firecrawl-website-design-clone
source_url: https://crowninstitute.colorado.edu/science-love
target_stack: HTML/CSS or React + Tailwind
output: DESIGN.md
```
