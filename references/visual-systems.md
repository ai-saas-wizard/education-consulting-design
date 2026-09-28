# Visual systems — measured from the references

Measured 28 September 2026 from the saved 1265×712 captures and each site's public CSS. **CSS** values come from the site's stylesheet. **Measured** values are sampled pixels from the captures. Several Aligned frames caught a scroll fade-in, so their text looks paler than it really is. Use the CSS values, not the pale pixels.

These tokens are the design. Copy the chosen system's block into the handoff, then apply only the changes the owner approved. Keep one system per site.

**What you may take:** fonts, weights, type scale, color roles, spacing, radii, component shapes, section compositions and image treatment. **What you must never take:** logos or wordmarks, brand names, photographs, testimonials, copy, numbers, prices, badges or product artwork.

---

## A. Aligned — soft-minimal coaching

Frames: [contact sheet](screenshots/aligned-contact-sheet.jpg). Section-to-frame mapping is in the [atlas](reference-atlas.md#aligned--soft-minimal-coaching).

### Tokens

| Role | Value | Source |
|---|---|---|
| Page background | `#F6F3EE` | CSS `--background` |
| Alternate section band | `#ECE7DF` | CSS `--card`; sections alternate with the page background |
| Headings and text | `#2C2825` | CSS `--foreground` |
| Body copy | `#2C2825` at 70% opacity | CSS `text-foreground/70` |
| Eyebrows, nav, stat labels | `#2C2825` at 60% opacity | CSS |
| Hairlines, dividers | `#DAD6CE` (header rule ≈ `#E2DFDA`) | CSS `--border` / measured |
| Main pill button | fill `#C6BBAD`, label `#2B2823` | CSS |
| Large pill on dark photo | fill `#E8DDD0`, label `#2C2825` | CSS |
| Secondary pill | fill `#9B8B7D`, label `#16120D` | CSS `--primary` |
| Dark sections and photo veils | `#151310` (88% over the final collage); hero veil black at 40% | CSS |
| Text on dark | `#FBF9F5` | CSS |
| Corners | photos, cards and video 16px (video 24px on desktop); buttons fully rounded | CSS |
| Video shadow | `0 24px 70px rgba(43,40,35,0.18)` | CSS |

### Type

Load `Inter Tight` (300, 400, 500, 600, 700) and `DM Sans` (300, 400, 500, 600) from Google Fonts.

| Element | Specification |
|---|---|
| Section heading | Inter Tight 300, 36px mobile → 60px at ≥1024px → 72px at ≥1280px; line-height 0.95; letter-spacing −0.025em. Two lines: the first light, the last phrase in 500. Examples: "Built for women / **who lead**", "Coaching that fits / **your life**", "Everything you need / **to succeed**". Never italic. |
| Hero brand words | Inter Tight 700 uppercase, 48px → 128px, line-height 0.9, white over the photo |
| Stat numbers | Inter Tight 300, 48px → 60px |
| Card, step and FAQ titles | Inter Tight 500, 20–30px |
| Step numerals | Inter Tight 300, 60px or larger, heading color at 30% opacity |
| Body | DM Sans 400, 18px, line-height 1.625 |
| Eyebrow | DM Sans 500, 12px, uppercase, letter-spacing 0.3em, 60% opacity |
| Nav and stat labels | DM Sans 400, 14px, uppercase, letter-spacing 0.025em, 60% opacity |
| Buttons | DM Sans 500, 14px (nav) or 16px (large), letter-spacing 0.025em; padding 10×24px (nav), 16×40px or 20×48px (large) |

### Layout

- Section padding: 64px mobile, 160px desktop. Alternate `#F6F3EE` and `#ECE7DF` bands.
- Container: about 1200px; full-bleed grids and stat rows up to 1400px; horizontal padding 24px mobile, 48px desktop.
- Splits: two columns, 96px gap, vertically centered. Section intros are centered: eyebrow → heading → optional body.
- Header: fixed, about 95px tall, page background with a 1px bottom rule. Logo on the left, uppercase nav in the center, pill button on the right.
- Hover: pills lift 2px and gain a soft shadow. There are no other decorative effects.

### Imagery

Bright studio photography on pale seamless backgrounds, with people in neutral or black clothing and warm, desaturated grading. The page palette is neutral, so the photographs carry the color. Photo cards use a dark gradient at the bottom behind white text. Portrait crops are 3:4, testimonial videos 9:16 and the explainer video 16:9.

### Section recipes

| Section | Frames | Recipe |
|---|---|---|
| Hero | 01 | Full-bleed collage of four vertical photo panels under a veil. "WELCOME TO" in thin tracked caps, giant white brand words split around the foreground people, and a tracked uppercase tagline at the bottom. **Without a real photo shoot, or when the owner skips it, open with the explainer section instead. Don't invent hero art.** |
| Explainer and stats | 02, 03 | Centered eyebrow and two-line heading above a wide 16:9 rounded video with a poster, captions and a soft shadow. Below it, three stats: light numbers with small uppercase labels, then a hairline. Stats must be verified numbers. Without proof, use truthful offer facts (steps, modules, sessions, access) in the same style. Never use invented results. |
| Audience split | 04, 05 | Rounded portrait on the left. On the right: eyebrow, two-line heading, two or three short paragraphs and a pill. |
| Video testimonials | 06, 07 | Row of 9:16 rounded video cards, each with a centered round play button. |
| Transformations | 08–11 | Four-across evidence cards on the alternate band. Only with authorized, relevant client evidence. |
| Differentiators | 14, 15 | Centered heading, then three tall photo cards with a bottom gradient and a white title and text. |
| Founder story | 16, 17 | Narrative column with a portrait and a pull quote. |
| Team | 18–20 | Three then two columns: 3:4 portrait, name, tracked role label, short bio and a "read more" link. |
| Philosophy | 21, 22 | Large photo on the left. On the right: eyebrow and a three-line heading ending in 500. |
| Included | 23–25 | Six image-backed cards in three columns, each with a title and one line of text. |
| Process | 26 | Three columns. Pale giant numerals 01/02/03 joined by thin lines, then a 500-weight title and centered body. |
| FAQ | 27, 28 | Centered intro, then rows about 800px wide: a 20–24px question, a chevron and hairline dividers. |
| Final CTA | 29, 30 | Dark photo collage under the veil, a giant light heading ("Ready to start?") and one light pill. |
| Offer or pricing card | not captured; from the live site's campaign page CSS | A centered white card with 16px corners and a large soft shadow on the alternate band, 32–40px padding. Price in Inter Tight 300. Checklist items use 6px `#C6BBAD` dot bullets. One pill button, with terms in small DM Sans below. Label it extrapolated in the handoff. |
| Footer | 30 | Centered logo, results disclaimer, copyright and underlined legal links on the page background. |

**Without photography.** The system still works when the owner has no photo shoot:

1. Open with the explainer section (02, 03): header, centered eyebrow, two-line heading, one supporting line and the pill, then a large 16:9 video (or a labeled video slot) and the stats row.
2. Lean on the type-led recipes: process (26), stats (03), FAQ (27, 28), and the alternate-band section intros.
3. Use a labeled 3:4 founder-portrait slot for the story.
4. Close with a plain dark `#151310` final CTA band instead of the collage.

Never fill the photo slots with illustrations.

### Not in this system

- Serif, script or italic headings. The only script is the brand's own logo.
- Any accent color: no green, terracotta, blue or gold. The palette is taupes and warm neutrals only.
- Uppercase section headings. Only the hero brand words are uppercase.
- Icons in circles, icon card grids, illustrations, diagrams, or interface mockups standing in for photography.
- Bordered boxes on the page background, heavy shadows, gradients other than photo veils.

---

## B. Launchpad — dark product-led academy

Frames: [contact sheet](screenshots/launchpad-contact-sheet.jpg). Section-to-frame mapping is in the [atlas](reference-atlas.md#digital-launchpad--product-led-academy).

### Tokens

| Role | Value | Source |
|---|---|---|
| Page background | `#131212` (renders ≈ `#121212`) | CSS / measured |
| Card surface | `#171717` small cards; `#232121` large panels | measured / CSS |
| Raised controls | `#333030` (chevron buttons, tabs) | CSS |
| Card border | 1px, white at about 6% (≈ `#1D1D1D`); warm-tinted rows ≈ `#311D16` | measured |
| Accent | `#FB440A` (renders ≈ `#E55429` in text) | CSS / measured |
| Main button | vertical gradient `#FF4704` → `#AF1919`, white label | CSS |
| Card tint | `linear-gradient(216deg, transparent, rgba(250,66,10,0.15))` | CSS |
| Ambient glow | large radial orange blooms at corners and behind hero, inclusion and pricing blocks (renders ≈ `#511F0E` at peak) | measured |
| Headings | `#FFFFFF` | measured |
| Body | white at about 85% on panels (≈ `#E2DEDD`); secondary ≈ `#ABAAAA`; notes ≈ `#939393` | measured |
| Highlighted phrases | text on an orange marker (≈ `#C4401B`) | measured, frame 02 |
| Corners | 24px panels and pricing card; 16px list rows; 12px small cards; 6–8px buttons | CSS / measured |

### Type

Load `Oswald` (500, 600, 700) and `Poppins` (400, 500, 600, 700) from Google Fonts.

| Element | Specification |
|---|---|
| Section heading and H1 | Oswald 700 uppercase, about 56px at the 1265px capture (source CSS goes to 90–110px on large screens); line-height 1.0–1.1; letter-spacing −0.01 to −0.03em. The accent line or word is in `#FB440A`. |
| Card and row titles | Oswald 600–700 uppercase, 20–24px, white |
| Category labels | Poppins 700 uppercase, 14–15px, accent color |
| Eyebrow | Oswald 500 uppercase, 16px, warm gray (≈ `#CDBEBA`) |
| Stats | Oswald 700, 28–32px numbers; Poppins 14px labels; 1px `#222` vertical dividers |
| Body | Poppins 400, 16–18px, line-height 1.5–1.6 |
| Buttons | Poppins 600 uppercase, 16px, padding about 16×32px; hero button about 345×56px |

### Layout

- Header: logo centered and nothing else, about 70px tall, with a 1px bottom line that glows orange in the middle.
- Container about 1150px. Section spacing 120–160px. Section headings centered.
- Hero: split roughly 45/55. On the left: eyebrow, two-line H1 (white, then accent), 18px body, a wide gradient button with a small note under it, and a two-stat row. On the right: the real product dashboard in a dark rounded frame over the glow.

### Imagery

Real product interface screenshots, instructor portraits with course-branded thumbnails, and glossy 3D achievement badges. Every visual shows the actual product or its people.

### Section recipes

| Section | Frames | Recipe |
|---|---|---|
| Hero | 01 | As described in Layout. |
| Positioning bridge | 02 | Centered 20–22px Poppins paragraph with two or three phrases on an orange marker. |
| Audience | 03 | Four equal dark cards, each with a small icon badge, an orange Oswald title and centered body. |
| Comparison | 04 | Two cards with a central separator. The recommended option is filled with the gradient. |
| Inclusions | 05–07 | Asymmetric bento panels (2/3 + 1/3) with orange titles, body and product imagery on an inner glow. |
| Sample lessons | 08, 09 | Carousel of lesson cards with arrow controls. |
| Curriculum | 10–14 | Full-width rows: portrait or course thumbnail, Oswald title plus orange category, two-line summary, instructor and duration, and a module count with a square chevron expander on the right. |
| Results | 15, 16 | Dense evidence grid plus the main button. Use only real, contextualized evidence. |
| Milestones | 17–19 | Rows with giant Oswald numerals fading from orange to transparent, title and body in the middle, badge and "1ST MONTH" label on the right, hairline separators. |
| Outcome summary | 20, 21 | Central emblem with benefit text around it, then the button. |
| Pricing | 22, 23 | One centered card (24–32px corners) on a glow: Oswald price, billing line, divider, two-column checklist, gradient button, redirect note and payment marks. |
| Video reviews, FAQ, close | 24–27 | Review slider, topic tabs over question rows, then a big centered outcome heading and button. |
| Footer | 28 | Minimal legal and contact row plus copyright. |

### Not in this system

- Light page backgrounds, pastel colors, or a second accent family. Only orange and red.
- Serif, italic, or light or thin heading weights.
- Pill-shaped main buttons.
- Clip-art, illustrations, stock icons as hero art, or made-up interfaces presented as the real product.
- Flat gray cards without the warm tint or glow.

---

## C. IELTS — expert education (hero frame only)

Frames: [hero](screenshots/ielts-hero.png) and [diagnostic](screenshots/ielts-diagnostic.png). Only the hero was captured. For other sections, keep these tokens with clean centered layouts and label those parts as extrapolated.

| Role | Value | Source |
|---|---|---|
| Header | white; nav in near-black uppercase bold, about 17px; orange rounded button on the right | measured |
| Hero band | navy `#1A2744` (renders ≈ `#252A42`), centered, max text width 800px | CSS / measured |
| Accent | orange `#F26522` (renders ≈ `#E36D35`): button, second headline line, eyebrow text | CSS / measured |
| Eyebrow pill | accent text on `rgba(242,101,34,0.15)`, 20px corners, 13px 600 uppercase, letter-spacing 1.5px | CSS |
| Headline | as captured: bold uppercase sans about 34px, line 1 white, line 2 orange. The live site has since switched to DM Serif Display 52px; follow the capture unless the owner prefers the current look. | measured / CSS |
| Subhead | 21px, white at 80%, key phrases bold | CSS |
| Button | 19px 700, padding 18×44px, 8px corners, shadow `0 4px 14px rgba(242,101,34,0.35)` | CSS |
| Proof row | DM Serif Display 32px white numbers; 15px uppercase labels in white at 55%, letter-spacing 0.8px; 48px gaps | CSS |
| Section titles | DM Serif Display 38px, navy, centered; 20px subtitles in `#2D3748` | CSS |
| Body | DM Sans or Inter 400 | CSS |

Not in this system: a full dark page (only the hero band is navy), photographic collage heroes, condensed type, or neon and glow effects.

---

## Metabolic Makeover — structural reference

Use it for method sequencing, engagement duration and fit criteria. Only its [hero](screenshots/mma-hero.png) was captured: a light header, a charcoal `#3A3D44` split panel beside a large photograph, Helvetica Neue light/medium uppercase headline, and steel-blue `#8495A9` buttons. Offer it as a look only if the owner asks for it, and say that one frame exists.

---

## Generic-output check

Run this on the token block, the preview and the handoff. Remove anything the chosen system does not do unless the owner asked for it:

- A serif display headline, or an italic accent word in a second color.
- Accent colors that are not in the token table (terracotta, sage, forest green, gold, purple).
- Eyebrow labels with a short leading rule, or numbered "01 / LABEL" tags on every card.
- Hero art built as an illustrated card, diagram, "canvas", quadrant grid, icon cluster, or invented app window, instead of the reference's photography or real product interface.
- Icon-card grids where the reference uses photos, rows or numbered steps.
- Decorative gradient blobs, glassmorphism, grain textures, or tilted cards.
- Hatched, striped or gradient placeholder fills. A placeholder is a flat block in a surface color with a small label.
- Status banners ("private preview", "demo mode") inside the designed page. Put such labels in the page title or a small corner tag.
- Fonts that are not in the token block, including "safer" substitutes.
