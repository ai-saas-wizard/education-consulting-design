# Brand assets — logo and design elements

Generate every design element the site needs here: logo set, favicon, social share image, `design-tokens.css`, and icons where the chosen system uses them. Nothing is left as a "logo missing" dependency unless the owner declines. Work in the owner's project under `brand/`.

## 1. Investigate before drawing

If the owner has no logo, or wants theirs refined, ask these in the design round of the interview. Offer a recommendation for each:

1. **Name as it should appear:** exact spelling and capitalization, plus any short descriptor ("Business Canvas" or "BusinessCanvas"; "Academy" or none).
2. **Logo type:** wordmark only (recommended for most small education brands), symbol plus wordmark, or monogram.
3. **Meaning:** what the name or offer should suggest, and any symbol ideas they like or hate.
4. **Existing presence:** social avatar, channel art, slides or an old site. Inspect whatever they share and keep anything worth keeping.
5. **Avoid:** competitors' marks, clichés they dislike, colors they won't use.
6. **Uses:** website header, favicon, social avatar, course thumbnails, dark and light backgrounds.

## 2. Three concepts in the chosen system

Write three distinct concepts. Each gets a name, the one idea behind it, its form, typeface and weight, color, and why it fits the reference system. Then ask the owner to pick one, or pick your recommendation if they said "you decide". Build every concept from the token block:

| System | Wordmark direction | Mark direction |
|---|---|---|
| Aligned | Inter Tight 500–600, tracking −0.02em, `#2C2825` on ivory and `#FBF9F5` on dark. Optionally a small DM Sans descriptor in tracked caps. | Optional. A quiet geometric monogram in one weight. Never a script lockup like Aligned's own logo. |
| Launchpad | Oswald 700 uppercase, stacked or single line, white on dark. | A simple solid geometric symbol, with `#FB440A` as the one accent. Never their rocket or swoosh. |
| IELTS | Bold sans wordmark in navy `#1A2744`. | Square monogram tile in navy with the orange accent. |
| Owner's reference | That reference's display face and accent. | Keep it as simple as that reference's own marks. |

The name typed in the site font is a placeholder, not a logo. Every concept needs at least one ownable detail: a custom letter cut, a ligature, a deliberate weight or spacing shift, or a small mark. At least one of the three concepts includes a symbol.

Good logos here share these traits:

- One idea.
- Readable at 16px, and works in a single color.
- Built from the system's fonts and palette.
- Distinctive at a glance.

Avoid:

- Stock clichés: lightbulbs, rockets, graduation caps, globes, brains, swooshes, generic arrows, initials in a circle.
- Gradients, shadows, 3D gloss or hairline strokes that vanish when small.
- Anything resembling the reference brand or a well-known logo.

## 3. Generate

**Every agent: build the final logo as SVG.** Set the wordmark as real type in the system's display font. Build the mark from simple shapes or paths. If Python with `fontTools` is available, convert the wordmark to outlines so the SVG doesn't depend on an installed font. Otherwise embed the Google Font in the SVG for previews and note that production needs outlined text.

**With an image-generation tool** (Codex has one built in; some Claude setups have an image tool or MCP connected, or can run `codex exec` when the Codex CLI is installed and logged in):

- Use it to explore symbol concepts, then view every result.
- Recreate the chosen symbol as clean SVG geometry, or keep the PNG only if it can't be vectorized.
- Never ship model-drawn lettering as the final wordmark. Image models misspell names and drift into serif type.

Prompt template:

```text
Minimal flat vector logo symbol for "<Name>", a <one-line business description>.
Concept: <the one idea>. Style: <solid geometric shapes | single-weight line>,
colors <hex> and <hex> only, on a plain <background hex> background, centered with generous padding.
Four distinct variations in a 2x2 grid, aspect ratio 1:1.
No text, no letters, no gradients, no shadows, no 3D, no mockups, no photographic detail.
```

**Without an image tool** (for example Claude with no image connector):

1. Still deliver the SVG concepts above. Claude draws clean SVG directly.
2. Give the owner the prompt template filled in.
3. Add these steps for the owner:
   1. Open ChatGPT image generation, Ideogram (strongest at lettering) or Recraft (exports SVG).
   2. Paste the prompt and generate a few rounds.
   3. Download the favorite as SVG, or as a transparent PNG at 1024px or more.
   4. Save it as `brand/logo-mark.svg` or `brand/logo-mark.png` and say "added".
4. When the file arrives, build the lockups and derivatives from it.

## 4. Files to deliver

| File | Content |
|---|---|
| `brand/logo.svg` | Primary horizontal lockup on light backgrounds |
| `brand/logo-reversed.svg` | Lockup for dark backgrounds |
| `brand/logo-mark.svg` | Square mark or monogram (the wordmark initial if there is no symbol) |
| `brand/favicon.svg` | Mark simplified for 16–32px; PNG 32, 180 and 512 exports if a converter is available |
| `brand/og-image.html` | 1200×630 social share layout from the tokens: logo, headline, background. Screenshot it to `og-image.png` if possible. |
| `brand/logo-concepts.md` | The three concepts, the owner's pick, generation prompts used, usage rules |
| `design-tokens.css` | Every token as CSS custom properties. `design-preview.html` imports it. |

Usage rules for the handoff: minimum size (wordmark 20px tall; mark 16px), clear space (height of the wordmark's capital), approved colors, and don'ts (no stretching, recoloring, effects or backgrounds behind it).

**Icons:** only where the chosen system uses them (Launchpad audience cards, for example). Name an open-source set such as Lucide, with the icon names, size and stroke weight, or draw simple SVGs in the same stroke style.

**Photography and supporting imagery:**

- Write a shot list for anything the owner should photograph: subject, framing, background, light and ratio, matching the system's image treatment.
- Image generation may create non-person supporting art on request (textures, objects, backgrounds, device frames), labeled as generated.
- Never generate people presented as the founder, team, clients or students, and never generate testimonials, results or before/after images.

## 5. Verify

- Put the logo in the preview header at its real size.
- Screenshot it on light and dark backgrounds, and check it at favicon size.
- Read the name letter by letter.
- Check contrast.
- Compare it with the reference's logo to confirm it is clearly different.

AI-generated marks may not be registrable as trademarks everywhere. If the owner plans to register the logo, recommend a clearance search and a designer's final pass.
