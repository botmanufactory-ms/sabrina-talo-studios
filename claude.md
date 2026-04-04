# SABRINA TALO STUDIOS — Website Rebuild Project Briefing

> **Project:** New website for Sabrina Talo Studios  
> **Type:** Interior styling studio — private homes & holiday rentals  
> **Location:** Bangalow, Australia  
> **URL (reference):** sabrinatalostudios.com.au  

---

## 0. Claude Skills & Build Instructions

> **CRITICAL:** When building any frontend component, page, or artifact for this project, Claude **MUST** use the following skills:

### Required Skills

1. **`frontend-design`** (`/mnt/skills/public/frontend-design/SKILL.md`)
   - **ALWAYS** read this skill before writing any HTML, CSS, React, or UI code.
   - Follow its guidelines for typography, color, motion, spatial composition, and visual details.
   - Commit to the editorial-minimalist aesthetic defined in this briefing — no generic AI slop.

2. **`ui-ux-pro-max`** (Custom Skill — if available in `/mnt/skills/user/` or `/mnt/skills/private/`)
   - If this skill is present in the project, **ALWAYS** read it before any UI/UX work.
   - Apply its interaction design patterns, responsive behavior rules, and quality standards.
   - If not found, fall back to `frontend-design` and the UX patterns defined in Section 7 of this briefing.

### Skill Usage Protocol

For **every** frontend task in this project:

```
1. Read /mnt/skills/public/frontend-design/SKILL.md
2. Read /mnt/skills/user/ui-ux-pro-max/SKILL.md (if exists)
3. Cross-reference with this briefing's Design System (Section 2) and UI/UX Patterns (Section 7)
4. Only then begin implementation
```

### Design Non-Negotiables (enforced by skills)

- **Zero border-radius** on everything — buttons, inputs, cards, images
- **Pragmatica Extended** for display/h1, **Aktiv Grotesk** for headings, **Open Sans** for body
- **Photography-first** layout — images carry the emotion
- **Scroll-triggered animations** — subtle, refined, `ease-out` timing
- **No generic aesthetics** — no Inter/Roboto, no purple gradients, no rounded pastel cards
- **Sharp, editorial, magazine-quality** execution at all times

---

## 1. Brand Identity

### Brand Name
**SABRINA TALO STUDIOS** (often abbreviated as **ST Studios** or **STS**)

### Tagline
**LIVE BEAUTIFULLY.**

### Brand Promise
_"Styling real homes for real people — spaces that feel like you."_

### Logo
- **Primary Logo:** `LOGOS SABRINA TALO STUDIOS` — clean wordmark, all-caps
- **Logo URL:** `https://images.squarespace-cdn.com/content/v1/67b40b2bbc94e21d977c1464/73346424-6104-4b8f-9aea-b6eedb07b1ed/LOGOS++SABRINA+TALO+STUDIOS.png?format=1500w`
- **Secondary Mark:** `https://images.squarespace-cdn.com/content/v1/67b40b2bbc94e21d977c1464/6622728c-6405-4a03-8c45-2f0a544c20d7/LOGOS++SABRINA+TALO+STUDIOS+%281%29.png`
- **Favicon:** `https://images.squarespace-cdn.com/content/v1/67b40b2bbc94e21d977c1464/1eebe2cb-5a38-4a2b-a4df-4ed24da384f2/favicon.ico?format=100w`
- **Logo links to:** `/` (homepage)
- **Alt text:** `SABRINA TALO STUDIOS`

---

## 2. Design System & Brand Kit

### Color Palette

| Token              | Value       | Usage                                      |
|--------------------|-------------|---------------------------------------------|
| `--color-primary`  | `#000000`   | Primary brand color, links, CTA borders     |
| `--color-accent`   | `#000000`   | Accent elements                             |
| `--color-bg`       | `#28282A`   | Dark background sections                    |
| `--color-text`     | `#28282A`   | Body text on light backgrounds              |
| `--color-surface`  | `#FFFFFF`   | Input backgrounds, cards, light surfaces    |
| `--color-muted`    | `#F5F5F3`   | Secondary button fills, subtle backgrounds  |
| `--color-border`   | `#232325`   | Input borders, dividers                     |

> **Scheme:** Light-dominant with dark `#28282A` accents. Black-and-white is the core identity. Warmth comes from photography, not from color.

### Typography

| Role      | Font Family            | Fallback Stack          | Size Reference  |
|-----------|------------------------|--------------------------|-----------------|
| Display   | **Pragmatica Extended** | `pragmatica-extended`   | `h1: 205.1px`  |
| Heading   | **Aktiv Grotesk**      | `sans-serif`            | `h2: 62.08px`  |
| Body      | **Open Sans**          | `sans-serif`            | `body: 15.08px` |

**Rules:**
- `h1` uses Pragmatica Extended — oversized, editorial, impactful
- `h2–h4` use Aktiv Grotesk — clean, geometric, modern
- Body/paragraph text uses Open Sans — readable, friendly
- All type is intentional: huge display type for hero moments, restrained body copy
- Font loading via Adobe Fonts / Typekit (Pragmatica Extended, Aktiv Grotesk) + Google Fonts (Open Sans)

### Spacing & Shape

| Property        | Value  |
|-----------------|--------|
| Base unit       | `4px`  |
| Border radius   | `0px`  |

> **Everything is sharp-edged.** Zero border-radius on all components — buttons, inputs, cards, images. This is a deliberate brutalist-minimal aesthetic choice. Do not soften corners.

### Components

#### Primary Button
```css
.btn-primary {
  background: transparent;
  color: #000000;
  border: 1px solid #000000;
  border-radius: 0;
  box-shadow: none;
  text-transform: uppercase;
  letter-spacing: 0.1em;
}
```
> Ghost/outline style. Transparent fill, black border. Hover state should invert (filled black, white text).

#### Secondary Button
```css
.btn-secondary {
  background: #F5F5F3;
  color: #000000;
  border: 1px solid #F5F5F3;
  border-radius: 0;
  box-shadow: none;
}
```

#### Input Fields
```css
.input {
  background: #FFFFFF;
  color: #000000;
  border: 1px solid #232325;
  border-radius: 0;
  box-shadow: none;
}
```

---

## 3. Design Direction & Aesthetic

### Tone
- **Professional** but warm and approachable
- **Medium energy** — not loud, not sleepy
- Editorial quality with a residential, lived-in feeling
- Think: Australian design magazine meets down-to-earth stylist

### Aesthetic Mandate

> **This website must feel like a curated interior — not a tech product.**

Key principles:
1. **Editorial minimalism** — Large imagery, generous whitespace, oversized typography
2. **Sharp geometry** — Zero radius, clean lines, grid-based but with asymmetric moments
3. **Photography-first** — Images carry the emotion; design stays out of the way
4. **Texture through contrast** — Dark `#28282A` sections against white, large type against small body copy
5. **Subtle motion** — Scroll-triggered reveals, parallax on hero images, smooth fade-ins. Never flashy.
6. **No AI slop** — No gradient blobs, no rounded pastel cards, no generic SaaS aesthetic

### Visual References (inferred from current site)
- Full-bleed hero images with overlaid text
- Horizontal scrolling carousel for brand values
- Alternating image/text blocks with `View fullsize` functionality
- Dark footer with newsletter signup
- Sticky/minimal navigation

---

## 4. Site Architecture

### Navigation (Primary)

| Label          | Path              | Notes                         |
|----------------|-------------------|-------------------------------|
| Projects       | `/projects`       | Portfolio showcase (was `/bangalowproject`) |
| Holiday Homes  | `/holiday-homes`  | Service page — holiday rental styling |
| Private Homes  | `/private-homes`  | Service page — residential styling |
| About STS      | `/about`          | Brand story & bio             |
| Contact        | `/contact`        | Contact form / CTA            |

### Footer Structure
- **Left column:** Brand mark + tagline "LIVE BEAUTIFULLY."
- **Center column:** Location info ("Find us in Bangalow"), hours (Mon–Fri, 9am–5pm)
- **Sitemap links:** Services, Gallery, About Us
- **Social links:** [Facebook](https://www.facebook.com/profile.php?id=61574074654975), [Instagram](https://www.instagram.com/sabrinatalostudios/)
- **Newsletter signup:** Email input + "Sign Up" button
- **Privacy note:** "We respect your privacy."

---

## 5. Page-by-Page Content Blueprint

### 5.1 Homepage

**Hero Section**
- Full-bleed interior photograph (warm, real home)
- Overlay text: _"Styling real homes for real people — spaces that feel like you."_
- No CTA button in hero — let the image breathe

**Introduction Block**
- Large quote-style heading: _"Good styling shapes how you feel in a space. I create homes that feel personal, lived-in, and inviting — whether it's your own sanctuary or a holiday stay people can't wait to come back to."_
- Body text about ST Studios' approach: curated new + vintage, budget-conscious, personal
- CTA: `LEARN MORE` → `/about`

**Brand Values Carousel**
Horizontal scroll or marquee with 5 rotating statements:
1. "I work with what you already have and make it feel fresh again"
2. "I mix new pieces with second-hand finds so your home feels lived-in, not staged"
3. "I keep styling realistic, affordable and true to how you actually live"
4. "I listen first, then shape the space around your personality and routines"
5. "I focus on comfort, warmth and character — not perfection"

> Each accompanied by the secondary brand mark icon.

**Holiday Homes Block**
- Large image + heading "Holiday Homes Styling"
- Body: Airbnb/vacation rental styling services, guest experience focus, budget-friendly
- CTA: `HOLIDAY HOMES STYLING` → `/holiday-homes`

**Private Homes Block**
- Large image + heading "Private Homes"
- Body: Personal home styling, own or rent, personality-driven
- CTA: `HOME STYLING SERVICES` → `/private-homes`

**About Preview Block**
- Large image + heading "About"
- Body: Sabrina's story — born from love of creating real spaces, vintage + new, understanding how you live
- CTA: `WORK WITH ME` → `/contact`

**Footer**
- Full footer with newsletter, sitemap, social, hours

### 5.2 Projects (Portfolio)
- Grid or masonry layout of styled projects
- Each project = large image + project name + brief description
- Click-through to individual project galleries
- Full-screen image viewing capability

### 5.3 Holiday Homes
- Service description focused on vacation rental styling
- Benefits: elevated guest experience, increased bookings, property appeal
- Process overview
- Before/after or gallery
- CTA to contact

### 5.4 Private Homes
- Service description for residential styling
- Emphasis: personality-driven, budget-friendly, mixing curated + vintage
- Process overview
- Gallery / testimonials
- CTA to contact

### 5.5 About STS
- Sabrina's bio and studio story
- Philosophy: warmth, personality, story behind every piece
- Approach: understand → shape → deliver
- Studio location (Bangalow)
- Photo of Sabrina / studio

### 5.6 Contact
- Contact form (name, email, message)
- Location info: Bangalow
- Hours: Monday–Friday, 9am–5pm
- Social links
- Optional: embedded map

---

## 6. Technical Requirements

### Stack Recommendation
- **Framework:** Next.js (App Router) or Astro for static-first performance
- **Styling:** Tailwind CSS with custom design tokens matching brand kit
- **Fonts:** Adobe Fonts (Pragmatica Extended, Aktiv Grotesk) + Google Fonts (Open Sans)
- **CMS:** Headless CMS (Sanity / Contentful) for project portfolio management
- **Hosting:** Netlify or Vercel
- **Forms:** Netlify Forms or Resend for contact/newsletter
- **Analytics:** Plausible or simple GA4
- **Images:** Next/Image or Astro Image with lazy loading, WebP/AVIF

### Performance Targets
- Lighthouse Performance: > 90
- LCP: < 2.5s
- CLS: < 0.1
- Mobile-first responsive design

### SEO Essentials
- Semantic HTML5 throughout
- Open Graph meta tags (use brand OG image)
- Structured data (LocalBusiness schema for Bangalow location)
- Alt text on all images
- Sitemap.xml + robots.txt

### Accessibility
- WCAG 2.1 AA minimum
- Skip-to-content link
- Keyboard navigable
- Sufficient contrast ratios (note: black on white meets AA)
- Focus states on all interactive elements

---

## 7. UI/UX Interaction Patterns

### Navigation
- **Desktop:** Horizontal nav bar, logo left, links right. Sticky on scroll with subtle background blur.
- **Mobile:** Hamburger menu → full-screen overlay with large nav links
- Smooth scroll behavior between sections on homepage

### Scroll Animations
- Hero image: subtle parallax or scale-on-scroll
- Content blocks: staggered fade-up on scroll-into-view (IntersectionObserver)
- Brand values: horizontal auto-scroll marquee or snap-scroll carousel
- Images: reveal with a subtle clip-path or opacity transition

### Hover States
- Nav links: underline slide-in from left
- Buttons: primary → fill inversion (transparent → black bg, white text)
- Project cards: slight scale + overlay with project name
- Images: subtle zoom on hover (contained within frame)

### Transitions
- Page transitions: smooth fade or slide (if SPA)
- All transitions: `ease-out`, 300–500ms
- No bounce, no elastic — keep it refined

---

## 8. Image Assets (from current site)

| Description                        | URL |
|------------------------------------|-----|
| Hero interior shot                 | `beac1b6e-bea6-46ca-9071-806005c5cb36/EA4A7CD1-064C-4129-BC17-D876B121644C.JPG` |
| Introduction lifestyle image       | `3f058d06-4305-41bd-955a-05a50d110dd3/IMG_9013.JPG` |
| Holiday Homes feature image        | `fb6f064b-dbe0-435e-be87-89962a20361c/IMG_8890.JPG` |
| Private Homes feature image        | `f8f4d3b3-377f-4ee7-aba2-f5e6b2bcdc57/IMG_8791.png` |
| About section image                | `28f3c5ea-0369-40f8-b262-68bd7f6d1c71/41ABE711-9AEE-44CE-BF73-110BF729DAFB.JPG` |

> All images hosted on Squarespace CDN — will need to be downloaded and re-hosted for new site. Base URL: `https://images.squarespace-cdn.com/content/v1/67b40b2bbc94e21d977c1464/`

---

## 9. Target Audience

- **Primary:** Homeowners and renters looking for interior styling in the Byron Bay / Bangalow region
- **Secondary:** Holiday home / Airbnb owners wanting to elevate their rental property
- **Tertiary:** Design-aware individuals browsing for inspiration

**Audience traits:**
- Value authenticity over perfection
- Budget-conscious but design-aware
- Prefer lived-in warmth over sterile showroom aesthetics
- Likely found via Instagram, word of mouth, or local search

---

## 10. Brand Voice & Copy Guidelines

### Tone of Voice
- **Warm** but professional — like a knowledgeable friend, not a salesperson
- **First person** ("I create…", "I work with…") — Sabrina speaks directly
- **Down-to-earth** — no jargon, no interior design buzzwords
- **Confident** but never pretentious

### Copy Patterns (from existing content)
- Short, punchy headlines in uppercase
- Longer, conversational body paragraphs
- Frequent use of dashes (—) for rhythm
- Key phrases: "real homes," "real people," "lived-in," "personal," "grounded," "warmth," "character," "budget-friendly," "curated," "vintage finds," "second-hand"

### Words to USE
`warmth` · `character` · `personal` · `curated` · `lived-in` · `grounded` · `inviting` · `real` · `fresh` · `thoughtful` · `balanced` · `uniquely yours`

### Words to AVOID
`luxury` · `bespoke` · `exclusive` · `opulent` · `premium` · `cutting-edge` · `sleek` · `state-of-the-art`

---

## 11. Implementation Priorities

### Phase 1 — MVP Launch
1. Homepage (full content as described above)
2. About page
3. Contact page with working form
4. Basic responsive navigation
5. Newsletter signup integration
6. SEO fundamentals

### Phase 2 — Portfolio & Services
1. Projects page with gallery grid
2. Individual project detail pages
3. Holiday Homes service page
4. Private Homes service page
5. Image optimization pass

### Phase 3 — Polish & Growth
1. Blog / Journal section (for SEO & content marketing)
2. Testimonials integration
3. Instagram feed embed
4. Advanced animations and scroll effects
5. CMS integration for self-service content updates

---

## 12. Quality Checklist

Before shipping any page, verify:

- [ ] Typography hierarchy matches brand kit (Pragmatica Extended → Aktiv Grotesk → Open Sans)
- [ ] All border-radius is `0px` — no rounded corners anywhere
- [ ] Primary buttons are ghost/outline style (transparent + black border)
- [ ] Photography is full-bleed and high-quality
- [ ] Dark sections use `#28282A`, not pure black
- [ ] Mobile navigation works flawlessly
- [ ] All images have descriptive alt text
- [ ] Page loads under 3 seconds on 4G
- [ ] Footer includes newsletter, social links, hours, sitemap
- [ ] Forms are accessible and functional
- [ ] No generic AI aesthetic — every element feels intentionally designed
- [ ] Scroll animations are subtle and refined, not playful or bouncy
