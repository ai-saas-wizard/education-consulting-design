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

Load `Inter Tight` (300, 400, 500, 600, 700, and 700 italic) and `DM Sans` (300, 400, 500, 600) from Google Fonts: `family=Inter+Tight:ital,wght@0,300;0,400;0,500;0,600;0,700;1,700&family=DM+Sans:wght@300;400;500;600`. The live site loads no italic face and lets the browser slant the bold; load the real one.

| Element | Specification |
|---|---|
| Section heading | Inter Tight 300, 36px mobile → 60px at ≥1024px → 72px at ≥1280px; line-height 0.95; letter-spacing −0.025em. Two lines: the first light, the last phrase in 500. Examples: "Built for women / **who lead**", "Coaching that fits / **your life**", "Everything you need / **to succeed**". Upright. Aligned's only italic heading text is one key phrase in the explainer (video) heading, in 700 italic, same font and color; see the VSL-first hero. |
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

### Funnel blocks in this system

Behavior and content rules are in [conversion blocks](conversion-blocks.md). This is how the blocks look here. **CSS** values below come from the saved live-site code (featured-video and trust sections, 28 September 2026).

#### VSL-first hero (Aligned)

Model frames: [02](screenshots/aligned-02.png), [03](screenshots/aligned-03.png).

| Part | Specification | Source |
|---|---|---|
| Header | The system header: logo left, one pill right with the main CTA label. No center navigation on a video-first page. | tokens |
| Section | Page background `#F6F3EE`. Top padding 64px, 96px at ≥1024px. Side padding 24px, 48px at ≥1024px. | CSS |
| Qualifier | The eyebrow style, centered. | tokens |
| Headline | Inter Tight 300, 24px → 36px at ≥768px → 48px at ≥1024px; line-height 1.25; letter-spacing −0.025em; centered; max width 896px; 32px below it (48px at ≥1024px). One key phrase in 700 italic, same font and color (the live site's `font-bold italic`). | CSS |
| Support line | DM Sans 400, 18px, line-height 1.625, at 70%, centered. | tokens |
| Player | 16:9, max width 1024px, black behind the video, corners 16px (24px at ≥1024px), shadow `0 24px 70px rgba(43,40,35,0.18)`. | CSS |
| Play button | 80px circle (96px at ≥1024px), fill `#C6BBAD`, icon `#2B2823` at 32px (40px), centered; grows 5% on hover. | CSS |
| Duration and speed chip | Pill in `#2B2823` at 80%, 12px text in white at 90%, 12px from the bottom-right corner (20px at ≥1024px). | CSS |
| CTA | The large main pill, centered under the player, then microcopy in DM Sans 400 14px at 70% (60% fails contrast; see the contrast check). | tokens |
| Statistics | Top padding 64px (96px at ≥1024px), bottom 80px, 1px `#DAD6CE` rule below. Max width 1400px. Three columns with 48px gaps at ≥768px, one column below. Numbers Inter Tight 300, 48px → 60px; labels DM Sans 14px uppercase, letter-spacing 0.025em, at 60%. | CSS |
| Design-only slot | The player's size and corners, flat `#ECE7DF`, no shadow, no play button. Label centered in the eyebrow style. | skill rule |
| No video yet (live site) | Qualifier → headline → support line → CTA and microcopy → statistics, same spacing. | skill rule |
| Video beside the headline | The audience-split composition (04, 05) mirrored: copy left, 16:9 player right with the player treatment above, 96px gap. | recipes |

#### Tier comparison (Aligned)

Not captured; extrapolated from the offer card above. Two offer cards side by side on the `#ECE7DF` band, 48px apart, stacked 48px apart on phones in the same order. Price in Inter Tight 300 with the recurrence beside it in DM Sans 400 14px at 70%. Inclusions with the 6px `#C6BBAD` dot bullets. Each card has its own main pill and the refund line in small DM Sans below. Mark the recommended tier with an eyebrow-style label above its name. No other emphasis: no accent color, no badge, no border. Label this extrapolated in the handoff.

#### Forms, quiz and checkout (Aligned)

Not captured (the live application is a third-party form); extrapolated from the tokens. Quiz options are white rows with 16px corners, a 1px `#DAD6CE` border, DM Sans 400 18px text and at least 56px height; the selected row takes the main-pill colors (`#C6BBAD` fill, `#2B2823` text). Text fields are white pills with a 1px `#DAD6CE` border and 16px DM Sans text, with DM Sans 500 14px labels. Focus is a 2px `#2B2823` outline 3px outside the element (CSS, campaign button). Progress is DM Sans 14px uppercase at 70%, such as "2 OF 5 · YOUR GOALS". Errors are written text with an icon, in the text color; there is no red in this system. The checkout order summary is the offer card.

### Not in this system

- Serif or script headings, and italic headings apart from the explainer heading's one bold-italic key phrase (same font and color). The only script is the brand's own logo.
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

### Funnel blocks in this system

Behavior and content rules are in [conversion blocks](conversion-blocks.md). **Measured** values below are sampled from the 1265×712 captures.

#### VSL-first hero (Launchpad)

Model frames: [01](screenshots/launchpad-01.png) for the hero and its frame treatment, [24](screenshots/launchpad-24.png) for a centered video panel and benefit-line thumbnails.

| Part | Specification | Source |
|---|---|---|
| Header | The system header: logo centered, about 70px tall, 1px bottom line glowing orange in the middle. No button. | measured |
| Background | `#131212` with the ambient orange glow behind the player (≈ `#511F0E` at its peak). | CSS / measured |
| Qualifier | The eyebrow: Oswald 500 uppercase 16px, ≈ `#CDBEBA`, centered. | measured |
| Headline | Oswald 700 uppercase, about 56px at the 1265px capture, line-height 1.0–1.1, letter-spacing −0.01 to −0.03em. First line white, second line `#FB440A`. Centered. | measured / CSS |
| Support line | Poppins 400, 18px, white at about 85%, centered. | measured |
| Player | 16:9, about 794px wide at the 1265px capture (the width of the centered review panel in frame 24), 24px corners, 1px border in white at about 6%, sitting on the glow. | measured |
| Poster | One benefit phrase in bold white type with its key words on the orange marker (≈ `#C4401B`), like the review thumbnails in frame 24. | measured |
| Play control | Not captured as a custom control; frame 24 shows the video host's own button. Use the host's visible controls, or a round button in the main-button gradient, labeled extrapolated. | extrapolated |
| CTA | The main gradient button (`#FF4704` → `#AF1919`, white Poppins 600 uppercase 16px, about 345×56px, 6–8px corners), centered under the player, with the small note under it in Poppins about 14px, ≈ `#ABAAAA`. | measured |
| Statistics | Oswald 700 28–32px numbers, Poppins 14px labels, 1px `#222` vertical dividers between items, centered. | measured |
| Design-only slot | The player's size, corners and border, flat `#232121`, no glow behind it. Label centered in the eyebrow style. | skill rule |
| No video yet (live site) | Qualifier → headline → support line → button and note → statistics, centered. With a real product screenshot, use the original split hero instead. | recipes |
| Video beside the headline | The hero's own split: copy on the left (about 45%), the player in the dashboard's dark rounded frame on the right (about 55%). | recipes |
| Phones | Not captured. Keep the order above; player at full content width; button full width; headline in two short lines. | extrapolated |

#### Tier comparison (Launchpad)

Frame [04](screenshots/launchpad-04.png)'s two-card composition, without its "VS" badge: that badge compares against an outside alternative, not between the owner's own tiers. Two equal cards, about 504px each at the 1265px capture, 24px corners. The standard tier has the page color (`#121212`) with a 1–2px warm border (≈ `#663A31`). The recommended tier is filled with the vertical gradient ≈ `#8D2F16` → ≈ `#4E1A0F` (measured) and carries the main gradient button. Each card follows the pricing card ([22](screenshots/launchpad-22.png), [23](screenshots/launchpad-23.png)): Oswald 700 price with the recurrence on the billing line under it, a divider, the checklist, and one button. Stacked on phones in the same order.

#### Forms, quiz and checkout (Launchpad)

Measured from the provider checkout capture ([checkout](screenshots/launchpad-checkout.png)): a centered column about 380px wide on ≈ `#0B0B0D`; white, fully rounded inputs about 37px tall; bold white labels about 15px, with an asterisk for required fields; a two-step progress indicator of two white circles joined by a line. Quiz options (extrapolated): small cards in `#171717` with 12px corners, a 1px border in white at about 6%, Poppins 16–18px text and at least 48px height; the selected option gets a 1px `#FB440A` border and the card tint. The order summary is the pricing card.

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

The captured headline's sans family isn't named in the saved CSS. Set it in the body sans at 700–800, so the page keeps two font families.

### More values from the saved homepage CSS

Taken from the live homepage's stylesheet saved on 28 September 2026. Only the hero was captured as a screenshot, so these sections have no model frame.

| Role | Value |
|---|---|
| Off-white section band | `#F8F7F4` |
| Hairlines and card borders | `#ECEAE5` |
| Body text | `#2D3748`; secondary `#718096` |
| Raised navy | `#243356` |
| Orange hover | `#D9551A`; the button lifts 1px, shadow `0 6px 20px rgba(242,101,34,0.4)` |
| Secondary button | Navy fill, white 17px 600, padding 14×32px, 8px corners |
| Text link button | `#718096` 15px 500, 1px underline at 40% opacity |
| Video card | White, 12px corners, 1px `#ECEAE5` border, 16:9 embed; lifts 3px on hover. Grid up to 960px, three columns, 24px gaps; one column at ≤768px. |
| Section padding | 70px 40px; 50px 24px at ≤768px; 40px 20px at ≤480px |
| Hero at smaller widths | Padding 60px 24px 50px at ≤768px, 48px 20px 40px at ≤480px. Subhead 21px → 18px → 17px. Main button 19px → 17px (16×36px padding) → 16px (14×28px) full width. Proof numbers 32px → 26px → 24px; gaps 48px → 24px → stacked 16px apart. Eyebrow 13px → 11px with 5×12px padding at ≤480px. |
| Success state only | `#22C55E` |

### Funnel blocks in this system

Behavior and content rules are in [conversion blocks](conversion-blocks.md).

#### VSL-first hero (IELTS)

Model frame: [hero](screenshots/ielts-hero.png). The player sits inside the captured hero band.

| Part | Specification | Source |
|---|---|---|
| Header | White; logo left; the orange rounded button on the right carries the main CTA label. Remove the other nav items on a video-first page. | measured |
| Band | Navy `#1A2744`, centered, padding 80px 40px 70px (smaller widths above), inner width 800px. | CSS |
| Qualifier | The eyebrow pill: orange text on `rgba(242,101,34,0.15)`, 13px 600 uppercase, letter-spacing 1.5px, padding 6×16px, 20px corners. | CSS |
| Headline | As captured: bold uppercase sans about 34px, first line white, second line orange. If the owner prefers the current live look: DM Serif Display 52px (32px, 26px on smaller screens), line-height 1.15, key phrase in orange. | measured / CSS |
| Support line | 21px, white at 80%, max width 620px, line-height 1.7, key phrases in bold white. | CSS |
| Player | 16:9 at the band's 800px inner width, 12px corners (the site's video-card radius). No glow and no border: this system has no glow effects. | CSS |
| CTA | The main button (19px 700, 18×44px padding, 8px corners, shadow `0 4px 14px rgba(242,101,34,0.35)`), 36px below the player (the subhead-to-button spacing), then microcopy at 15px in white at 55%, sentence case. | CSS |
| Statistics | The proof row: 40px above it; DM Serif Display 32px white numbers; 15px uppercase labels in white at 55%, letter-spacing 0.8px; 48px gaps. | CSS |
| Design-only slot | The player's size and corners, flat `#243356`. Label in 15px uppercase white at 55%. | skill rule |
| No video yet (live site) | Exactly the captured hero: eyebrow → headline → subhead → button → proof row. | measured |
| Video below the first screen | A section on white or `#F8F7F4`: section title (DM Serif Display 38px navy, centered), a 20px subtitle in `#2D3748`, then the player as a video card (white, 12px corners, 1px `#ECEAE5` border) up to 800px wide, then the main button. | CSS |
| Video beside the headline | Not in this system; the hero is centered. Use the centerpiece or below the first screen. | rule |

#### Tier comparison (IELTS)

Extrapolated from the CSS. On the `#F8F7F4` band, two white cards in the video-card treatment (12px corners, 1px `#ECEAE5` border), side by side up to 960px wide with a 24px gap, stacked at ≤768px. Tier name and price in DM Serif Display navy, with the recurrence beside the price in 15px `#2D3748`. Inclusions in 17px `#2D3748`. The recommended tier carries the eyebrow pill above its name and the orange main button; the other tier uses the navy secondary button.

#### Forms, quiz and checkout (IELTS)

Extrapolated from the CSS. White inputs with a 1px `#ECEAE5` border and 8px corners (the button radius), 17px `#2D3748` text, 15px 600 navy labels. Quiz options are white rows in the video-card treatment, at least 48px tall; the selected option takes a 2px navy border. The main button submits. Success states may use `#22C55E` together with a written label.

Not in this system: a full dark page (only the hero band is navy), photographic collage heroes, condensed type, or neon and glow effects.

---

## Metabolic Makeover — structural reference

Use it for method sequencing, engagement duration and fit criteria. Only its [hero](screenshots/mma-hero.png) was captured: a light header, a charcoal `#3A3D44` split panel beside a large photograph, Helvetica Neue light/medium uppercase headline, and steel-blue `#8495A9` buttons. Offer it as a look only if the owner asks for it, and say that one frame exists.

---

## Contrast check

The measured values reproduce the references faithfully, and a few of them fall below WCAG AA at the sizes they're used. Check every text color at its size: 4.5:1 for text under 24px (or under about 19px bold), 3:1 for larger text. When a measured pair fails, keep the rest of the system and list an accessibility override in the handoff's override table with the reason "contrast". Known cases (computed 29 September 2026):

| System | Pair | Contrast | Passing override |
|---|---|---|---|
| Aligned | Eyebrows, nav and stat labels: `#2C2825` at 60% on `#F6F3EE` / `#ECE7DF` | 3.9:1 / 3.8:1 | `#2C2825` at 70%, the body value: 5.2:1 / 5.0:1 |
| IELTS | White on the orange button `#F26522` | 3.2:1 | Keep button labels at 19px 700 or larger at every width, so they count as large text |
| IELTS | Orange eyebrow text on its tinted pill over navy | 4.0:1 | Orange text without the pill tint: 4.7:1 |
| IELTS | `#718096` text on white / `#F8F7F4` | 4.0:1 / 3.8:1 | `#2D3748` for text under 24px |
| Launchpad | White on the lightest point of the button gradient (`#FF4704`) | 3.4:1 | Button labels at 19px 700 or larger, so they count as large text |

## Generic-output check

Run this on the token block, the preview and the handoff. Remove anything the chosen system does not do unless the owner asked for it:

- A serif display headline, or an italic accent word in a second color.
- Accent colors that are not in the token table (terracotta, sage, forest green, gold, purple).
- Eyebrow labels with a short leading rule, or numbered "01 / LABEL" tags on every card.
- Hero art built as an illustrated card, diagram, "canvas", quadrant grid, icon cluster, or invented app window, instead of the reference's photography or real product interface.
- Icon-card grids where the reference uses photos, rows or numbered steps.
- Decorative gradient blobs, glassmorphism, grain textures, or tilted cards.
- Hatched, striped or gradient placeholder fills. A placeholder is a flat block in a surface color with a small label, and that color must differ from the band it sits on (on Aligned's `#ECE7DF` band, use `#F6F3EE`), or the slot looks like empty space.
- Status banners or developer notes ("private preview", "demo mode", "DEMO ONLY", "temporary video", "this placeholder proves the layout") inside the designed page. Put such labels in the page title or a small corner tag.
- "[DRAFT]" tags inside the copy. Write draft copy as it would read, mark it `draft` in the handoff's section table, and say "draft copy" in the preview's corner tag. A missing fact still shows as a marked slot, such as "[price — owner to confirm]".
- Fonts that are not in the token block, including "safer" substitutes.
- A second palette, font family or component style taken from the owner's old site or an inspiration without a row in the handoff's override table. One base system, plus listed overrides, and nothing else.
- A play button, duration or controls on the slot for a video that doesn't exist yet, or an old or unrelated video in the player. (A recorded video still waiting for its poster keeps its real duration; see [video states](conversion-blocks.md#video-states).)
- Crossed-out prices, "save" badges, countdowns or seat counters without evidence in the funnel plan.
- Counters that start at 0, and numbers without a source.
