# Education & Consulting Design

An AI agent skill for turning an education, coaching, consulting, or info-product funnel plan into a concrete website design and visitor journey—ready for a website builder.

It defines the layout, visual system, responsive behavior, content slots, and where every action leads. It does not plan the funnel, write video scripts, deploy a website or connect a backend.

It is the design step in a five-skill pipeline:

```text
educational-funnel       → funnel-plan.md (offer, prices, route, every page, follow-up)
vsl-scriptwriter         → the sales-video script (optional)
education-consulting-design → the design (this skill)
website-generation       → the working website
website-security         → the pre-launch safety check
```

It reads `funnel-plan.md` as its source of business facts and never edits it. Without a funnel plan it recommends running `educational-funnel` first, and can continue with a few business questions if the owner prefers.

[Read the skill](SKILL.md) · [Explore the references](references/reference-atlas.md) · [View the journey research](references/reference-journeys.md) · [Download ZIP](https://github.com/ai-saas-wizard/education-consulting-design/archive/refs/heads/main.zip)

## What you get

| Output | Contents |
| --- | --- |
| `design-direction.md` | One plain-language page you approve before any visual work: the look and its changes, your logo choice, how each page and the video will look, the numbers shown, how prices appear, and what's still needed |
| `design-handoff.md` | One base visual system plus your approved changes, page-by-page mapping from the funnel plan, hero and video presentation, statistics and pricing display, desktop/mobile wireframes, section specifications, component states, mobile experience, and acceptance criteria |
| `journey-map.md` | Navigation, CTA destinations, application/booking or enrollment flow, form requirements, success/error states, and unresolved dependencies |
| `asset-manifest.md` | Required images and media, aspect ratios, crop guidance, source and rights status, and missing assets |
| `brand/` | Logo set (primary, reversed, mark), favicon and social share image, generated when you don't have them, plus the concepts and prompts used |
| `design-tokens.css` | Every color, font, size, spacing and radius as CSS variables for the builder |
| `design-preview.html` | A static, nonfunctional preview of the first screen and key sections, built from the chosen reference's measured tokens |
| `design-references/` | Copies of the reference screenshots each section is modeled on, so the builder can match them (not for deployment) |

“Barebone” means a resolved design structure with clear content and asset slots. It does not mean an empty template.

## How it works

1. **Read the funnel plan, then interview.** It reads `funnel-plan.md` and doesn't re-ask anything it answers. Then it always asks about design, following the [interview guide](references/interview-guide.md): your inspirations (links or screenshots of whole sites or single sections), which reference look, how closely to follow it, what to leave out, your brand and logo, the imagery you have, and your sales video (whether you want one, where it goes, whether it's recorded, its length, language and who's on camera). Say “you decide” to accept its recommendations. It never invents prices, proof or results.
2. **Design direction.** It writes `design-direction.md`, a one-page summary in plain words, and waits for your approval before any visual work.
3. **Reference system.** It loads the measured fonts, colors, spacing and components of the look you chose ([visual systems](references/visual-systems.md)) as one base system plus your approved changes, and views the reference frame for every section it designs.
4. **Brand assets.** If you have no logo, it proposes three concepts in the chosen style and builds your pick as SVG with a favicon and social image. On Codex it can also explore symbols with the built-in image generator. On Claude without an image tool, it draws the SVG and gives you a ready prompt for ChatGPT, Ideogram or Recraft.
5. **Pages and flow.** It maps every page in your funnel plan to the look's section recipes, and designs the video block, numbers strip, pricing and every form and state screen ([conversion blocks](references/conversion-blocks.md)). A video that isn't recorded yet stays hidden on the live site; an old or off-topic video is never used in its place.
6. **Preview and compare.** It builds `design-preview.html`, screenshots it at the reference capture size, fixes differences against the reference frames, and asks for your approval.
7. **Handoff.** It writes the handoff, journey map and asset manifest. Builder rules at the top of the handoff tell the builder to keep the look intact, hide the video until the real one exists, and keep demo notes out of the page.

## Install

### Codex

Clone the skill into your personal skills directory:

```sh
mkdir -p ~/.codex/skills
git clone https://github.com/ai-saas-wizard/education-consulting-design.git ~/.codex/skills/education-consulting-design
```

If you use a custom `CODEX_HOME`, place the folder in its `skills` directory instead. Start a new task if your current task's skill list has not refreshed.

To update an existing clone:

```sh
git -C ~/.codex/skills/education-consulting-design pull --ff-only
```

Do not clone over an existing installation. Keep any local changes before updating.

### Download without Git

1. Download the [ZIP](https://github.com/ai-saas-wizard/education-consulting-design/archive/refs/heads/main.zip).
2. Extract it and rename the extracted directory to `education-consulting-design`.
3. Put the whole directory inside your agent's supported skills directory. Keep `SKILL.md`, `agents/`, and `references/` together.

### Other agents

The instructions are Markdown with skill frontmatter. Use them with an agent that supports directory-based `SKILL.md` skills, following that agent's installation convention. The `agents/openai.yaml` file supplies Codex metadata; other agents can use `SKILL.md` and its relative references directly. Cross-agent behavior has not been independently tested.

No API keys, package installation, or paid connector is required for the skill itself. The agent needs file access and image viewing to use the saved reference library. Live reference research additionally needs browser/web access.

## Use it

After the funnel planner has saved `funnel-plan.md` in your business folder:

```text
Use the education-consulting-design skill. Design the website from
funnel-plan.md. Create the design handoff, journey map, and asset
manifest for our builder.
```

For a video-led funnel, add what you already know about the look and the video:

```text
Use the education-consulting-design skill. Design the website from
funnel-plan.md. The page opens with my sales video (not recorded yet),
then the free quiz and my two plans. Follow the Aligned look closely,
but I'm known for my teal. Screenshots of pages I like are in ./inspiration/.
```

Without a funnel plan, the skill first recommends running `educational-funnel`, then continues with a few business questions if you prefer:

```text
Use the education-consulting-design skill to design a website for my
executive coaching business. The audience is first-time managers. The main
action is applying for a consultation. Follow the Aligned look closely.
```

Useful inputs: `funnel-plan.md`, any video script, your current site, your logo and brand colors, photos, links or screenshots of sites you like, and the reference look you want. The skill asks about anything the plan doesn't answer before it designs. Facts you can't answer yet are recorded as dependencies, not invented.

## Pair it with a builder

```text
funnel-plan.md (from educational-funnel)
    ↓
Education & Consulting Design
    ↓
design-handoff.md + journey-map.md + asset-manifest.md
(+ design-tokens.css, brand/, design-preview.html, design-references/)
    ↓
Your website builder
    ↓
Implementation, integrations, testing, deployment
```

The output matches the inspected input contract of the companion `website-generation` skill. That companion is not bundled or required: any builder that accepts a concrete design brief can consume the files.

Example follow-up:

```text
Use our website builder with design-handoff.md, journey-map.md, and
asset-manifest.md. Preserve the selected visual direction and visitor flow.
Resolve the listed business dependencies before implementing those parts.
```

Invoking the design skill alone does not authorize publishing, creating provider accounts, submitting forms, or making payments.

## Reference library

The skill includes 62 desktop screenshots, two contact sheets, a local HTML gallery, measured visual systems (fonts, colors, spacing and components taken from each reference's CSS), section descriptions, conversion research, and public visitor-journey observations.

| Reference | What it contributes |
| --- | --- |
| [Aligned Fitness](https://www.alignedfitnesscoaching.org/) | Soft-minimal coaching look (Inter Tight and DM Sans on warm ivory), founder photography, proof, team, and application flow |
| [Digital Launchpad](https://join.digital-launchpad.com/) | Dark product-led presentation, course catalog, membership progression, pricing, and checkout entry |
| [Metabolic Makeover Academy](https://www.metabolicmakeoveracademy.org/) | Engagement method, delivery details, fit criteria, and qualification flow |
| [IELTS Advantage](https://www.ieltsadvantage.com/) | Expert-led education, course purchase, diagnostic, and free-learning paths |

### Visual references

| Aligned Fitness | Digital Launchpad |
| --- | --- |
| ![Aligned Fitness reference hero](references/screenshots/aligned-01.png) | ![Digital Launchpad reference hero](references/screenshots/launchpad-01.png) |

Open the [reference atlas](references/reference-atlas.md) for section mappings, or download the repository and open `references/screenshots/gallery.html` in a browser. GitHub displays the gallery's source rather than hosting it as a website.

**Research date:** 17 September 2026. Captures overlap; larger sections span multiple frames. Some animations appear faded and some lazy-loaded images were absent. These are desktop references, not mobile captures. Descriptions document the gaps.

Public navigation and conversion entry points were inspected. Applications and payments were not submitted, so later states are marked as site-stated or unverified. Reference prices and links can change. No measured conversion uplift is claimed.

## Repository structure

```text
education-consulting-design/
├── SKILL.md
├── README.md
├── LICENSE
├── NOTICE.md
├── agents/
│   └── openai.yaml
└── references/
    ├── brand-assets.md
    ├── conversion-blocks.md
    ├── conversion-principles.md
    ├── handoff-contract.md
    ├── high-converting-landing-page.md
    ├── interview-guide.md
    ├── reference-atlas.md
    ├── reference-journeys.md
    ├── visual-systems.md
    └── screenshots/
        ├── gallery.html
        ├── aligned-contact-sheet.jpg
        ├── launchpad-contact-sheet.jpg
        └── … section and flow captures
```

## Design boundaries

- Match the chosen reference's visual system (type, color roles, spacing, components). Never reuse its logo, name, photos, copy or results.
- One base visual system plus the owner's listed changes. Never a blend of two looks.
- `funnel-plan.md` is read, never edited. Funnel strategy and video scripts belong to their own skills.
- A sales video that isn't recorded yet is hidden on the live site. Old or off-topic videos and fake players are never used.
- Use genuine client evidence. Missing testimonials, credentials, prices, policies, and outcomes remain visible dependencies. No fake discounts, countdowns or invented statistics.
- Map every designed interaction, including error, back, cancellation, confirmation, and access-help states where relevant.
- Separate observed behavior, publisher claims, proposed behavior, and unknowns.
- Treat conversion ideas as hypotheses, not guarantees.

## Validation and contributions

An earlier version passed Codex's skill metadata validator. For this version, a script checked that every relative link and heading anchor resolves and that the `SKILL.md` frontmatter parses as YAML. It was not re-run through Codex's validator.

**28 September 2026.** The earlier and the then-current versions were scenario-tested with Claude subagents on the same briefs.
- **Earlier version:** skipped the design questions and chose its own "original" palette and fonts.
- **Then-current version:** interviewed the owner first, reproduced the chosen reference's tokens (Aligned and Launchpad), compared screenshots against the reference frames, and generated an SVG logo set.

**29 September 2026.** Claude Sonnet subagents played the agent. The owner was simulated with answers taken from hidden fact sheets, and each question got only the answer the owner would give.
- **Previous version, three runs:** an assessment-first Excel course, with and without a funnel plan, and a high-ticket coaching offer.
  - It never asked for inspirations and asked little about the video.
  - Twice it offered the owner's old, off-topic video as a stand-in.
  - Its previews put play buttons, a made-up duration and developer notes on video placeholders.
  - It dismissed an owner's known brand color, dropped a system's button color on its own, and had no approval step before visual work.
- **This version, the same two businesses plus a membership whose owner said "don't wait on me":**
  - It read `funnel-plan.md` without re-asking or changing it (checksums identical), and asked for inspirations and every open video question.
  - It recorded one base system plus listed changes.
  - Under owner pressure it refused the old videos and an unsupported crossed-out price.
  - It showed a labeled video slot with no play button when no video existed, and a real player when one did.
  - Its previews read as the chosen reference (Aligned, IELTS).
- **Fixes from those runs:**
  - Too many questions in one message.
  - Draft tags inside the page.
  - Invisible placeholders.
  - Some measured colors failing contrast.
  - The order of the design direction when the owner delegates.
  - An over-long design direction.

  Each was fixed. Re-runs confirmed the question limit, the video states, the contrast overrides, and the direction's order and length.

Not tested: Codex, Launchpad's video hero, a real owner, and a funnel plan written by the upgraded funnel planner (a hand-written plan in the same shape was used). None of this certifies design quality, conversion performance, or every agent integration.

Issues and focused pull requests are welcome. Include the use case, proposed change, and an example of how it improves the resulting handoff. For reference updates, record the inspection date, source URL, and access limits. Do not contribute credentials, private client material, or fabricated results.

## License and reference rights

Original skill instructions and original supporting material are available under the [MIT License](LICENSE). Third-party screenshots, trademarks, quoted material, and the supplied research guide are excluded from that grant; see [NOTICE.md](NOTICE.md). Reference screenshots are not licensed production assets. No referenced business sponsors or endorses this project.
