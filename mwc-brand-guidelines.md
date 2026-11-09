# Men's Wellness Centers Brand Guidelines

Version: 2.0 (Nov 8, 2026)
Date: November 8, 2026
Status: Current. Published by Men's Wellness Centers. Living document; check the version history for changes.
Reference: the live website https://menswellnesscenters.com (Next.js build on Vercel, project `mwc-web-next`). This is the single source for color, type, components, imagery, voice and terminology.
Logo only: https://mwcbrand.com/logo. Nothing else from mwcbrand.com applies.
Machine-readable version: `brand.json`. Short LLM summary: `mwc-brand-llms.txt`.

Source key used in this document:

- `[S:tokens]` = site stylesheet `/_next/static/immutable/chunks/3hoi8t9pp9k0e.css` (global `:root` tokens, `.mwc-button`, `.mwc-card`, `.mwc-eyebrow`, header, footer)
- `[S:hero]` = `/_next/static/immutable/chunks/2by02y4iijdyv.css` (home hero and stats)
- `[S:all]` = all 15 site stylesheets loaded across 21 fetched pages (frequency counts)
- `[P:/path/]` = live page text on menswellnesscenters.com
- `[L:logo]` = https://mwcbrand.com/logo

---

## 1. Brand basics

| Item | Use |
|---|---|
| Name | Men's Wellness Centers (short form MWC after first use) |
| What we are | Three in-person men's health clinics in Virginia |
| Core services | Testosterone therapy (TRT), ED treatment, medical weight loss |
| Clinics | Richmond (Glen Allen address), Newport News, Virginia Beach |
| People we serve | Members (never patients, clients or customers in marketing copy) |
| Leadership | Eric O'Brien, President (never "founder") [P:/about-us/] |
| Medical leadership | Dr. Kristen Holtz, D.O., Physician Medical Director [P:/about-us/] |
| Trust line used on site | "10,000+ Men Served Since 2015 · LegitScript Certified" [P:/ all pages, top bar] |
| Booking | Site CTAs open the on-site appointment request, which hands off to book.menswellnesscenters.com |

---

## 2. Logo (from mwcbrand.com, the only element taken from it)

Source: [L:logo]. The site uses the same marks (`/media/Text_Logo_white.webp` in the header, `Primary_Logo_blue.webp` in structured data) [P:/].

**Marks**

- Primary wordmark: lowercase "men's" in a heavy rounded display face over tracked uppercase "WELLNESS CENTERS". Custom drawn.
- "m" bug: the lowercase rounded "m" alone. For favicons, app icons, social avatars, embroidery and any space under 96 px wide.

**Files (download from mwcbrand.com/logo)**

| File | Use |
|---|---|
| `wordmark_navy.svg`, `print_wordmark_navy_on_trans_4000x920.png` | Default, on white or light surfaces |
| `wordmark_white.svg`, `print_wordmark_white_on_trans_4000x920.png` | On navy or photo surfaces (site header and footer use white) |
| `wordmark_black.svg` | One-color print only |
| `m_icon_navy.svg`, `m_1024_navy_on_transparent.png` | Bug on light |
| `m_icon_white.svg`, `m_1024_white_on_transparent.png` | Bug on dark |
| `m_icon_black.svg` | One-color print only |
| `MWC-print-vectors.zip` | All 6 print SVGs |

Logo navy fill is `#0B1029`, the same as the site's `--mwc-primary-navy` [L:logo SVG fill, S:tokens].

**Rules**

- Clear space: at least the cap height of the lowercase "m" on all sides.
- Minimum size: wordmark 120 px (1.25 in) wide; bug 16 px (0.2 in).
- Colors: navy, white or black only. Navy on white is the default; white on navy for dark surfaces. On the website the header and footer use the white wordmark on navy.
- On the site: header logo 180 px wide, footer logo 240 px wide [S:tokens `.mwc-header__logo img`, `.mwc-footer__brand img`].
- Never retype the name in any font and call it the logo. Never recolor, rotate, skew, stretch, add effects, gradients or CSS filters.

---

## 3. Color

All values are from the live site CSS. Counts are hex occurrences across all site stylesheets [S:all].

### Core palette

| Token | Hex | Role on the site | Source |
|---|---|---|---|
| Primary Navy | `#0B1029` | Main text color on light backgrounds, footer background, solid navy sections, logo color. Most used non-white color (139 uses). | `--mwc-primary-navy` [S:tokens] |
| Page Navy | `#080D1F` | Header background, home hero and stats band, dark section backgrounds, "ink" text token. | `--mwc-page-navy`, aliased as `--mwc-navy`, `--mwc-ink`, `--mwc-text` [S:tokens] |
| Raised Navy | `#161B3A` | Raised panels and cards on dark sections. | `--mwc-raised-navy`, alias `--mwc-navy-light` [S:tokens] |
| Accent Orange | `#E8670A` | Primary buttons, eyebrows, icons, check marks, nav hover, play button, link accents (86 uses). | `--mwc-accent`, alias `--mwc-orange` [S:tokens] |
| White | `#FFFFFF` | Default page and card background, text on navy (267 uses). | `--background` [S:tokens] |

### Supporting neutrals

| Token | Hex | Role | Source |
|---|---|---|---|
| Cream | `#F5F3F0` | Warm section background (inner page heroes). | `--mwc-cream`, alias `--mwc-warm` [S:tokens, S:hero] |
| Off-White | `#F9FBFF` | Cool alternate section background. | `--mwc-off-white`, alias `--mwc-pale` [S:tokens] |
| Location Gray | `#F5F6F8` | Location page panels. | `--mwc-location-gray` [S:tokens] |
| Light Border | `#D9DEF0` | Card borders, dividers, dropdown borders. | `--mwc-light-border`, alias `--mwc-border` [S:tokens] |
| Muted Text | `#5D6878` | Secondary text and hero lead copy on light. | `--mwc-muted` [S:tokens] |
| Footer Gray | `#9CA3AF` | Footer link and blurb text on navy. | `.mwc-footer__links a` [S:tokens] |

### Accessible orange variants (used on the site for text and focus)

| Token | Hex | Role | Source |
|---|---|---|---|
| Orange Dark | `#BF5200` | Focus outlines, outline-button hover border. | location page CSS `css_0p4hqzqjg21px.css`, `css_3o1ahlv92wdv4.css` |
| Orange Text | `#A94700` | Orange text links on white (5.85:1 on white). | same |

### Contrast (WCAG 2.x, calculated)

| Pair | Ratio | Guidance |
|---|---|---|
| White on Primary Navy | 18.7:1 | Pass all sizes |
| Primary Navy on Cream | 16.9:1 | Pass all sizes |
| White on Orange `#E8670A` | 3.29:1 | Large text only (19 px bold and up, as the site's main buttons are). Do not use for small button labels. |
| Orange on Page Navy | 5.86:1 | Pass. Good for eyebrows and accents on dark. |
| Muted `#5D6878` on white | 5.65:1 | Pass for body |
| Orange Text `#A94700` on white | 5.85:1 | Use this, not `#E8670A`, for small orange text on white |

### Color rules

- Light pages are the norm: white and cream sections with navy text. Navy is used for the header, home hero, stats band, CTA bands and footer.
- Orange is the action color. Use it for the main CTA, eyebrows, icons and small accents. Do not set body copy in orange.
- No gradients appear in the site's core components. Shadows are soft and navy tinted.

---

## 4. Typography

Source: [S:tokens] `@font-face` and `--font-poppins`; `--default-font-family: var(--font-poppins)`.

| Item | Value |
|---|---|
| Family | **Poppins** for everything (headings, body, buttons, nav, labels). Fallback: `"Poppins Fallback", Arial, sans-serif`. |
| Weights loaded | 400, 500, 600, 700, 800 |
| Weight usage on site | 700 most common (228 rules), then 600 (53), 500 (40), 400 (14) [S:all] |
| Body | 16 px, line height 1.6, weight 400 (`--mwc-body-size`, `--mwc-body-leading`) |
| H1 | 44 px desktop (`--mwc-h1-size`), 30 px mobile, weight 500, line height 1.12 to 1.15, letter spacing -0.022em to -0.035em [S:hero] |
| H2 | 40 px (`--mwc-h2-size`), weight 700, line height 1.12, letter spacing -0.022em; 30 px on mobile |
| H3 | 16 to 23 px, weight 700, line height 1.25 to 1.3 |
| Eyebrow | 12 px, weight 600, UPPERCASE, letter spacing 0.14em, orange (`.mwc-eyebrow`) |
| Stats label | 12 px, weight 600, UPPERCASE, letter spacing 1.68px |
| Footer headings | 12 px, weight 700, UPPERCASE, letter spacing 0.12em |
| Nav links | 16 px, weight 500, white on navy, orange on hover |
| Hero lead | 18 px, weight 400 to 500, line height 1.55 to 1.6 |

**Case and style**

- Headlines are **sentence case** in the new components: "A full hour, face to face", "Your labs, explained", "Care you can understand." [P:/, P:/about-us/].
- H1 uses a lighter weight (500) than H2 (700). Keep that contrast.
- UPPERCASE is reserved for small tracked labels (eyebrows, stat labels, footer headings). Do not set headlines in all caps.
- No italics for emphasis; use weight.

---

## 5. Layout and spacing

Source: [S:tokens].

| Token | Value |
|---|---|
| Content width | 1240 px (`--mwc-layout-width`); some sections 1200 px |
| Reading width | 860 px (`--mwc-layout-reading`) |
| Page gutter | 20 px each side (`width: min(100% - 40px, 1240px)`) |
| Section padding | `clamp(64px, 7vw, 104px)` (`.mwc-section`); layout token 3rem mobile, 4rem desktop |
| Grid gap | 1.5rem (`--mwc-layout-gap`) |
| Card padding | 1.5rem mobile, 1.75rem desktop (`--mwc-layout-card`) |
| Base spacing unit | 0.25rem (`--spacing`) |
| Header height | 70 px minimum, sticky, navy |

---

## 6. Components

### Buttons

Primary button `.mwc-button` [S:tokens]:

- Background `#E8670A`, 2 px border in the same orange, text white.
- Shape: full pill, `border-radius: 999px`.
- Text: 19 px, weight 700, line height 1.3. Minimum height 48 px. Padding 11 px 22 px.
- Optional arrow icon after the label.
- Hover: lifts 1 px (`translateY(-1px)`). The hover token currently equals the base orange.
- Transition 0.2 s on color and transform. No pulsing or bouncing.

Variants:

- `.mwc-button--outline`: transparent background, orange text and border; fills orange with white text on hover.
- `.mwc-button--light`: transparent, white text and border, for navy sections; hover fills white with navy text.
- Header phone pill `.mwc-header__phone`: white text, 1 px white 52% border, 999 px radius, 14 px weight 500, phone icon.

Rule: main CTAs are orange pills with 19 px bold labels. Keep labels at 19 px bold on orange to meet large-text contrast. Form submit buttons on some pages use 4 to 8 px radius; new work should use the pill.

### Cards

`.mwc-card` [S:tokens]: white background, 1 px `#D9DEF0` border, 12 px radius (`--mwc-radius-card`), shadow `0 1px 4px #12196114`.

### Other component tokens

| Element | Value | Source |
|---|---|---|
| CTA glow shadow | `0 8px 28px #E8670A6B` | `--mwc-cta-shadow` |
| Dropdown menu | white, 8 px radius, `0 8px 24px #080D1F1F` | `.mwc-nav-group__menu` |
| Hero image | 8 px radius on home; 1.25rem radius on inner heroes | [S:hero] |
| Radius scale in use | 999 px (pills), 16 px, 12 px (cards), 8 px (images, menus), 50% (avatars, play button) | [S:all] |
| Step numbers | "01", "02", "03" with a small uppercase label, then an H3 | [P:/, P:/about-us/] |
| Check list | orange check icons, 600 weight short lines | [S:hero] `.homeChecks` |
| Stats band | navy, 4 columns, big number plus tracked uppercase label | [S:hero] |
| Video play | 80 px orange circle, white triangle, "PLAY VIDEO" tag | [S:hero] |

---

## 7. Imagery

Described from images on the live site (not copied) [P:/ and inner pages].

- **Real clinic and care team first.** Provider headshots and in-clinic portraits, a real blood draw in the clinic, the Richmond waiting room, clinic exteriors.
- **Real men in everyday Virginia life.** A smiling man at an outdoor cafe (home hero), running on the Virginia Beach oceanfront, exercising outdoors, on a sailboat, on a trail.
- **Local places.** Richmond skyline at sunset, City Center at Oyster Point in Newport News at dusk, Virginia Beach oceanfront.
- **Couples** appear on some legacy pages, relaxed and warm.
- Tone: natural light, candid, confident, healthy, not clinical cliche.
- Treatment: rounded corners (8 px or 1.25rem), full color, no heavy filters.
- Trust badges shown: LegitScript, CLIA, HIPAA.

Rules:

- Use real MWC clinic and team photos where possible. Stock is acceptable for lifestyle scenes only.
- No member photos, member stories or identifiable members without written consent and a signed release.
- No before and after images, no shirtless "transformation" shots, no product, needle or vial close-ups.
- Every image needs descriptive alt text (the site does this well on newer images; several older images have empty alt text).

---

## 8. Voice and tone

The site sounds like a calm, competent clinician explaining things clearly to a grown man. Plain, specific, careful.

**Traits**

1. **Clear and plain.** Short sentences. Everyday words. "Your labs, explained." [P:/]
2. **Process-first.** Explain what happens and in what order. "Spend 60 minutes with your provider discussing your health history and goals. Lab work is drawn on site during the same visit." [P:/]
3. **Clinically careful.** Treatment only when appropriate, every time. "Treatment is offered only when medically appropriate." [P:/]
4. **Respectful and private.** "Private, in-person visit." "No referral needed." [P:/]
5. **Transparent.** "If treatment is appropriate, you review the options and pricing before you commit." [P:/]
6. **Local.** Name the city and the clinic. "Get in-person care for low testosterone, erectile dysfunction (ED), and medical weight loss in Richmond, Newport News, or Virginia Beach." [P:/]

**Headline patterns used on the site**

| Pattern | Examples from the site |
|---|---|
| Short noun phrase with a comma | "A full hour, face to face" · "Your labs, explained" [P:/] |
| Plain promise of clarity | "Care you can understand." · "An evaluation before a treatment plan." [P:/about-us/] |
| Two-beat with a period | "Men's health care. Meet the people behind it." [P:/about-us/] |
| Direct "your" framing | "Your first visit and follow-up" · "Your Virginia Beach medical team" |
| Local SEO pattern | "Men's Health Clinic in Virginia Beach" · "TRT in Richmond, VA" |
| Question headings for FAQs | "What does the first visit cost?" · "Do I need a referral?" |

Avoid the legacy patterns still on older pages: ALL CAPS headings ("BOOK YOUR VISIT"), hype ("Real-World, Proven Results"), and long Title Case headings with a subhead jammed into the H2.

**Tone sliders**

- Confident, never pushy.
- Warm, never cute.
- Direct, never macho.
- Expert, never jargon heavy.

---

## 9. Terminology

| Say | Do not say |
|---|---|
| members | patients, clients, customers, users |
| clinic, clinics | office, facility, practice |
| provider (licensed provider, your provider) | "doctor" for NPs and PAs; "physician" unless the person is an MD or DO |
| first visit, appointment, in-person visit | consult, consultation (legacy), call, video visit |
| 60-minute, in-person first visit | 15-minute call, telehealth |
| just $60 (first visit) | free, no-cost, complimentary, $0 |
| evaluation, lab work, on-site labs | "test kit", "screening" claims |
| Testosterone therapy (TRT), Testosterone Replacement Therapy (TRT) | named medications |
| ED treatment, ED care, erectile dysfunction care | named medications |
| Medical weight loss, weight management | named medications or brand names, pound-loss numbers |
| treatment when medically appropriate | guaranteed, cure, fix, best, #1 |
| self-pay pricing, HSA and FSA cards accepted | "covered by insurance" |
| Eric O'Brien, President | founder |
| men, man | guys |

Service names to use in nav and headings (match the site): "Testosterone Therapy (TRT)", "ED Treatment", "Medical Weight Loss", "Testosterone testing".

---

## 10. Claims and compliance

These rules apply to every surface, whether or not the site currently follows them.

1. **Price.** The first visit is **just $60** for a 60-minute, in-person visit with a licensed provider. Never call it free or no-cost. Treatment is priced separately and reviewed before the member commits.
2. **No drug names.** Do not name medications (generic or brand) in marketing, ads, social, email or SMS. Use service names.
3. **No PHI.** Never publish or store protected health information. Use only aggregate, de-identified data. No small numbers that could identify a person.
4. **No guarantees or cure claims.** No "guaranteed", "cure", "proven results", pound-loss numbers or timelines. Results vary.
5. **Substantiation.** Any outcome, speed or comparison claim ("same-day", "most men see a provider within days", "10,000+ men served") needs current proof on file before use.
6. **Eligibility language.** Always pair treatment with "when medically appropriate" or "if your provider recommends it".
7. **Testimonials and member stories.** Only with written consent. Member photos and likeness only with a signed release. Show "Individual experiences. Results vary." with any review.
8. **Credentials.** Describe each clinician accurately (D.O., MD, NP, PA). Do not call the whole team "physicians".
9. **Messaging.** Honor DND and STOP. Texts only 9am to 8pm ET. Keep the SMS consent language shown on the site's form.
10. **No em dashes** in any copy. Use a period, comma or colon.
11. **Disclaimers.** Keep the site footer disclaimers on landing pages: informational only, not a substitute for an in-person evaluation, no guarantees, results vary.

---

## 11. CTAs

| Priority | Label (as on site) | Where | Destination |
|---|---|---|---|
| 1 | **Book My Appointment** | Header, heroes, section ends, clinic cards (135 uses across 21 pages) | On-site appointment request, then book.menswellnesscenters.com |
| 2 | **Call Now** | Hero secondary, mobile sticky bar | tel:+18663444955 |
| 3 | **See available times** | Appointment form submit | Hands off to book.menswellnesscenters.com/schedule |
| Mobile sticky | **Book Visit** | Mobile sticky bar | Appointment request |
| Content links | "Explore TRT", "Explore ED care", "Explore weight loss", "Meet our medical team" | Service cards, about | Inner pages |

Rules:

- One primary CTA per section: "Book My Appointment" as an orange pill.
- Secondary CTA is the phone, as an outline or light pill.
- Price line to pair with CTAs: "Your first visit is just $60: a full hour, in person, with on-site labs." (Approved price rule; not yet on the site.)
- Avoid "Get started", "Learn more", "Submit", "Click here". Retire "Book a Consultation" in favor of "Book My Appointment".

**Phone numbers (exactly as on the site)**

| Line | Number | Use |
|---|---|---|
| Main CTA line | **866-344-4955** | Header, "Call Now", hero, booking block. Use this on all brand-level CTAs. Verify before each new use. |
| Richmond | 804-346-4636 | Richmond clinic only |
| Newport News | 757-806-6263 | Newport News clinic only |
| Virginia Beach | 757-612-4428 | Virginia Beach clinic only |

---

## 12. Locations (exactly as on the site)

| Clinic | Address | Phone | Page |
|---|---|---|---|
| Richmond | 4050 Innslake Dr, Suite 360, Glen Allen, VA 23060-3323 | 804-346-4636 | /locations/richmond/ |
| Newport News | 827 Diligence Drive, Suite 206, Newport News, VA 23606-4268 | 757-806-6263 | /locations/newport-news/ |
| Virginia Beach | 996 First Colonial Rd, Virginia Beach, VA 23454-3175 | 757-612-4428 | /locations/virginia-beach/ |

City order used on the site: Richmond · Newport News · Virginia Beach. Hours: use each location page; do not restate hours in long-lived assets.

---

## 13. Examples

**Hero (web)**

> Eyebrow: TRT, ED CARE & MEDICAL WEIGHT LOSS
> H1: In-person men's health care in Virginia
> Lead: Get in-person care for low testosterone, ED and medical weight loss in Richmond, Newport News or Virginia Beach. Your first visit is just $60.
> Buttons: [Book My Appointment] [Call Now]
> Checks: Private, in-person visit. · On-site blood work when appropriate. · No referral needed.

**Social caption**

> A full hour, face to face. Your first visit at Men's Wellness Centers is just $60: 60 minutes with a licensed provider and on-site labs. Treatment only when medically appropriate. Book at book.menswellnesscenters.com

**SMS (9am to 8pm ET, consented members only)**

> Men's Wellness Centers: your first visit is just $60 for a full hour in person. Book: book.menswellnesscenters.com Reply STOP to opt out.

**Do and don't**

| Do | Don't |
|---|---|
| "Your labs, explained." | "Get your T levels fixed fast!" |
| "Treatment is offered only when medically appropriate." | "Guaranteed results." |
| "What members say" | "What patients say" |
| "Your first visit is just $60." | "Your first visit is free." |
| "Book My Appointment" | "Click here" |

---

## 14. Change log

- 2.0 (Nov 8, 2026): rebuilt from the live Next.js site. Replaces all mwcbrand.com guidance except the logo.
