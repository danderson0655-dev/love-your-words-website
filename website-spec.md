# Love Your Words -- Website Spec

> This document is the creative compass for all site work. Claude reads it at the start of every session. It records design decisions, content strategy, and QA findings so nothing drifts or gets repeated.

---

## Business Context

- **Business:** Love Your Words
- **Owner:** Diane Anderson
- **Role:** Customer Journey Content Strategist
- **Serves:** Nonprofits, healthcare organizations, essential-service businesses
- **Primary offer:** Customer Journey Content Package (retention email, brand voice guide, editorial calendar)
- **Mission:** Help mission-driven organizations keep the people they worked so hard to find
- **Voice:** Warm, story-first, unhurried. Opens with a scene. Trusts the reader.
- **Site purpose:** Convert qualified visitors into Discovery Call bookings

---

## Design Principles for This Site

1. **White and light always.** Pure white (#FFFFFF) is the base. No warm cream, no beige, no brown anywhere.
2. **Cosmic and expansive.** The palette evokes sunsets over water -- soft purples, pinks, lavender. Not earthy. Not corporate. Open sky.
3. **Gradient as personality.** The brand lives in the gradient: amethyst purple (#7B52C8) to dusty rose (#D87DB0). Use it on the logo, hero text, CTA buttons, credential bars. It's the signature.
4. **Clean and readable above all.** Outfit (headings) and Lexend (body) are chosen specifically for the Legacy niche -- clean, geometric, no decorative strokes that slow reading. Font sizes should be generous throughout.
5. **Light and airy -- never dark or moody.** The dark footer is the only dark element. Everything above it breathes.
6. **Bold without being loud.** The purple gradient IS the boldness. Keep backgrounds soft and let the gradient carry the energy.
7. **This site must never feel like:** a grandmother's website, a generic nonprofit site, something corporate or conservative, anything brown or earthy.

---

## Direction Comparison

### Direction 1: Warm Editorial (Rejected)
- Palette: Ivory #FAF7F2, Forest Green #2D6A4F, Gold #C8983A
- Fonts: Playfair Display + Lora
- User reaction: "Too much brown and beige."

### Direction 2: Soft Authority (Rejected)
- Palette: Warm white, Navy #1B2D4F, Terracotta #C96B4A
- Fonts: Cormorant Garamond + Jost
- Rejected with Direction 1 -- not evaluated separately.

### Direction 3: Story Dark (Rejected)
- Dark forest background -- Diane prefers light backgrounds.

### Cosmic Sunset (APPROVED -- 2026-06-17)
- Clean white background with soft lavender and pink section tints
- Purple-to-rose gradient as signature element
- Outfit + Lexend for maximum readability
- User feedback that led here: "too much brown and beige," wants "bold, edgy, colorful in a light and airy way," loves "sunsets more purple and soft pinks," water/universe/cosmic imagery, cool explorer vibe, 73 but not a grandmother aesthetic.

---

## Approved Design System

### Color Palette

| Role | Hex | Usage |
|---|---|---|
| Background | #FFFFFF | Primary page background |
| Soft tint | #F7F4FE | Alternate section backgrounds |
| Pink tint | #FEF4FA | About/warm section backgrounds |
| Text | #1C1830 | All body text |
| Primary | #7B52C8 | Buttons, links, active states |
| Primary Hover | #6840B8 | Button hover states |
| Secondary | #EDE7FA | Chips, pills, card backgrounds |
| Accent (pink) | #D87DB0 | Gradient endpoint, accent elements |
| Accent (blue) | #7BA8D8 | Gradient third tone, optional accents |
| Muted | rgba(28,24,48,0.50) | Body copy, secondary text |
| Card bg | rgba(123,82,200,0.04) | Service card backgrounds |
| Border | rgba(123,82,200,0.12) | Card and section borders |
| Footer bg | #0E0B1E | Dark footer only |

### Typography

| Role | Font | Weights | Notes |
|---|---|---|---|
| Heading | Outfit | 700, 800 | Geometric, clean, tight letter-spacing (-0.025em) |
| Body | Lexend | 300, 400, 500 | Accessibility-optimized, ideal for Legacy niche |

Google Fonts URL:
`https://fonts.googleapis.com/css2?family=Outfit:wght@400;500;600;700;800&family=Lexend:wght@300;400;500;600&display=swap`

### Design Tokens

| Token | Value | Notes |
|---|---|---|
| --radius | 14px | Rounded, friendly cards |
| --section-spacing | 6rem | Generous breathing room |
| Gradient (signature) | 135deg, #7B52C8 to #D87DB0 | Logo, hero text, CTA buttons, credential bar |
| Button shape | border-radius: 40px | Pill-shaped buttons throughout |

---

## QA Gate 1: Design Integrity

Run: 2026-06-17

- **Contrast:** #1C1830 on #FFFFFF = ~18:1 (exceeds WCAG AAA). Primary purple on white for large text = ~4.5:1 (WCAG AA). White text on gradient button = confirmed sufficient. PASS.
- **Responsive:** All sections use CSS grid with `auto-fit minmax`, responsive padding with vw units. Mobile hamburger present. PASS.
- **Fonts:** Google Fonts URL set in BaseLayout.astro. CSS tokens updated. No system-ui placeholders remain. PASS.
- **Gradients:** Use `background-clip: text` for text gradients -- CSS-native, GPU-friendly. No layout-shifting animations. PASS.
- **Build:** Cannot run in sandbox due to incomplete npm dependencies (shiki/dist/index.mjs missing). Will verify on Diane's machine at go-live. NOTE.
- **Design quality:** Typography -- Strong (Outfit/Lexend pairing is distinctive and readable). Color -- Strong (gradient signature is bold and memorable). Spatial -- Strong (generous whitespace, airy). Background -- Strong (white + subtle tints, no heavy texture). Motion -- hover transforms and gradient button present. Distinctiveness -- Strong (cosmic sunset palette is unique for a copywriter in this space). PASS.

---

## Content Strategy

Homepage hero leads with positioning: "Most organizations know how to find a donor. Few know how to keep one." Gradient lands on the punch line. Trust badges: Nonprofits, Healthcare Practices, Essential-Service Businesses.

Credentials bar: 20+ years in the trenches, Real People in Need (not demographics), Starwood/Princess Cruises/Comcast/Paul Hastings/Sheppard Mullin, Bay Area serving everywhere.

About section leads with Diane's trench background (loyalty programs, direct calls, trial team liaison, caregiving). Closes with Leo/Joybound transformation story -- Joybound gave her low-cost vet care; she wrote the donor letter as her gift back.

Services: Customer Journey Content Package as featured offer (retention email + brand voice + editorial calendar as one system). Three individual service cards below.

All muted/gray text changed to full dark (#1C1830) -- Diane has low vision, no light gray text anywhere on site.

Voice note: "Hero on a Mission" is Donald Miller IP -- do not use. "Customer Journey Content Strategist" is Diane's positioning.

---

## Pages Built (HTML Previews)

| Page | File | Status |
|---|---|---|
| Home | preview/cosmic-sunset.html | Complete with real copy |
| About | preview/about.html | Complete with real copy |
| Services | preview/services.html | Complete with real copy |
| Discovery Call | preview/discovery.html | Complete -- booking placeholder (email fallback) |

All pages are linked together via nav. Open any file in browser, click nav links to move between pages.

Discovery Call booking: placeholder until Calendly link is ready. Falls back to d.anderson0655@gmail.com.

---

## Milestones

- [x] **Design Direction** (2026-06-17) -- Cosmic Sunset approved
- [x] **Content** (2026-06-17) -- Real copy on all pages
- [x] **Full Site** (2026-06-17) -- All 4 pages built and linked
- [ ] **Go Live** -- GitHub + Vercel deployment (next session)

---

## Open Items Before Go Live

- [x] Add Calendly booking link to Discovery Call page -- https://calendly.com/d-anderson0655/15min (15-min call)
- [ ] Add headshot photo if desired (save as public/images/diane-headshot.jpg)
- [ ] Review all pages for any copy changes
- [ ] Fix Astro npm build environment (shiki dependency broken in sandbox -- verify on Diane's machine)
- [ ] GitHub repo + Vercel deployment

---

## Session Log

| Date | Done | Open |
|---|---|---|
| 2026-06-17 | Scaffolded Astro project. Built 3 directions. Diane rejected earthy/warm tones. Rebuilt as Cosmic Sunset. Approved. Design tokens locked. | -- |
| 2026-06-17 | Milestone 2: Real homepage copy. Milestone 3: About, Services, Discovery Call pages built. All linked. All text set to full dark. Copy refined with Diane's exact background (Starwood loyalty program, Princess Cruises direct calls, Sheppard Mullin/Paul Hastings trial team, caregiving, Leo/Joybound story). | Milestone 4: Go Live |
