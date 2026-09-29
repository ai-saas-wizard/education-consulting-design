# Builder-ready design contract

Compatible with the inspected `website-generation/references/design-handoff.md` contract on 2026-09-17: a concrete brief with a selected visual direction is an accepted design input. This schema is portable and does not require that exact builder.

**Files.** This skill reads `funnel-plan.md` (from the educational-funnel skill) and never writes, edits or renames it. It writes `design-direction.md` (for the owner), then `design-handoff.md`, `journey-map.md` and `asset-manifest.md` (for the builder), plus `design-tokens.css`, `brand/`, `design-preview.html` and `design-references/`.

## design-direction.md

One page the owner reads and approves before any visual work: no tokens, logo files or preview until then. Plain words, no jargon, no hex codes unless the owner used them. Keep it under about 700 words: one or two lines per item, "Decided for you" as a list of a few words each, and a short reason whenever you decline something they asked for. The detail and the reasoning belong in the handoff. Count the words before sending; if it's over 700, move explanations into the handoff. Use this shape:

```markdown
# Design direction: [business name]

Status: awaiting your approval
Built from: funnel-plan.md ([its title or date]), your answers ([dates]), [other inputs: script file, current site, photos]

**The look:** [system], matched [closely / its layout with your colors / loosely]. [One sentence on what that means, for example "warm ivory, light headings, soft taupe buttons, lots of space".]
**Changes to the look:** [each override in plain words, or "none"]
**Left out:** [exclusions]
**Your brand:** [logo: keep as supplied / refine / new; if new, "pick a direction: 1) … 2) … 3) …, my pick: …"; where your colors appear]
**Inspirations:** [each one: what I'll use and how, or why not]
**Your pages:** [each page from the funnel plan, in its order, with one line on how it will look]
**The sales video:** [placement; hidden on the live site until the final video exists, shown as a labeled box in the preview; length; language; who's on camera; captions and transcript]. [If there's no script yet: "The vsl-scriptwriter skill can write it from your funnel plan."]
**Numbers under the headline:** [each number with its source]
**Prices:** exactly as in your funnel plan, [side by side on computers, stacked on phones]. [No crossed-out price unless the plan shows it was really charged.]
**Photos:** [what's used; what shows a labeled box until you send it]
**On phones:** [two or three lines]
**Decided for you:** [each delegated decision, or "nothing"]
**Still needed from you:** [each missing item]

Reply "approved", or tell me what to change. I won't start the visual design until you approve.
```

Status values: `awaiting your approval`, `approved on [date]`, `approved with changes on [date]`, `proceeding on your "don't wait" — please review`.

**Approval handling**
- Approved: set the status and date, then continue.
- Changes: update the file, note what changed at the end, and continue unless a change reopens something the owner hasn't seen.
- The owner can't reply in this session: leave the status as awaiting approval, write the request to `design-questions.md`, and stop. No tokens, logo or preview on an unapproved direction.
- The owner said "don't wait on me": set the delegated status, list every decision made for them under "Decided for you", and continue. The handoff can then be at most `design-ready-with-dependencies`, with "owner review of design-direction.md" as its first dependency.

## design-handoff.md

Open the file with this block, filled in:

> **Builder rules.** This design reproduces the *[reference]* visual system with the owner-approved overrides listed below. Business facts (offer, prices, terms, page content, CTA destinations, checkout mechanics) come from `funnel-plan.md`: use them exactly and don't change them. Implement the tokens exactly: the same font families, weights, sizes, colors, spacing and corners. Use `design-tokens.css` and the logo files in `brand/` as delivered. Before building each section, open its model frame in `design-references/`. Screenshot your build at 1265×712 and compare it with the frame. Don't restyle with a different aesthetic or another design skill's defaults, and don't substitute fonts. Keep the video block hidden until the final, on-message video exists: never embed an old, unrelated or placeholder video, and never show a play button on a placeholder. Keep demo, test and status notes out of the designed page; use the browser tab title or a developer-only overlay that is off by default. Put each statistic's final value in the HTML and follow the counter rules in section 6. Show prices, recurrence and terms exactly as in `funnel-plan.md`, with no crossed-out prices, countdowns or seat counters that the plan doesn't support. Ask the owner before changing the look.

Then these sections. Where a section doesn't apply, say why in one line.

1. **Status and inputs.** Status (`ready-for-build` or `design-ready-with-dependencies`). The funnel plan used (its title and date) and what the design took from it: offer and tiers, audience, route, pages, CTAs and destinations, proof, video. The script file, if any (runtime and opening line only). The owner's design answers, with delegated decisions marked. Assumptions and scope exclusions. With no funnel plan: say so, and list the minimum business answers that stand in for it.
2. **References and priorities.** The one base visual system and the closeness level. Each inspiration with its decision: adopt (what, rebuilt with the base tokens), note only, or decline (why). The order that settles conflicts: 1) the funnel plan's facts, 2) the ethics rules, 3) the base system's tokens and recipes, 4) the approved overrides, 5) inspirations, only within 3 and 4.
3. **Visual system.** The chosen token block from [visual systems](visual-systems.md), or an equivalent block measured from the owner's own reference: color roles and hex values, font families with Google Fonts names and fallbacks, weights, sizes and line heights, spacing scale, maximum width, columns and gutters, borders and radii, image ratios, components, interaction and focus treatments. Then:
   - **Override table:** element, base value, override, reason (the owner's answer). This sentence under it: "Everything not listed here is the base system exactly."
   - **Conflicts resolved:** each clash between the reference look and the owner's existing brand (colors, fonts, logo, photo style), the decision, and where the owner's element appears.
   - **Exclusions and substitutions,** such as the no-photography opening.
   - **Imagery, motion, and fonts** for any non-Latin script.
   - Logo usage rules from [brand assets](brand-assets.md). `design-tokens.css` is the source of every value. Proposed breakpoints and why elements reflow.
4. **Page inventory and mapping.** One row per page or stage in the funnel plan: plan page, route, the page's job, main action and destination, its sections in the plan's order, and for each section the base-system recipe and model frame. Include every state screen the plan names. Don't add or drop funnel steps. When the plan is missing something the design needs, list it as a dependency.
5. **Hero and video presentation.** Placement and why. First-screen order. The copy: qualifier, headline, support line, CTA and microcopy, taken from the plan's starter copy where it has some and marked `draft` where you wrote it. The player in the base system (cite the recipe's values), poster, duration, captions and transcript. The video's state: final video exists; not recorded yet (hidden on the live site, labeled design-only slot in the preview); or an old video excluded (name it and say why). The hero layout while the video is hidden. See [conversion blocks](conversion-blocks.md#1-vsl-block).
6. **Proof and statistics.** The strip's items (number, label, source, period), the counter rules, where each piece of proof sits, and what is omitted for lack of proof.
7. **Pricing display.** The tiers exactly as the plan states them: card content, recurrence beside the price, inclusions in the same order, "best for", one CTA per tier and its destination, the refund line. Anchors only with the plan's evidence, quoted; otherwise "none". Desktop and phone layouts.
8. **Forms, assessment, application and purchase screens.** For each one the plan includes: layout in the base system, field and option styles, progress, result or outcome layouts, and every state the plan names.
9. **Per-page wireframes:** desktop and mobile diagrams with labeled content areas, realistic relative widths, hierarchy and section order. The diagrams, tokens, section specifications and `design-preview.html` together are the concrete design.
10. **Per-section table:** ID, visitor question or job, **model frame** (the reference screenshot it follows), headline and content slots, desktop layout, mobile layout, media size and crop, proof source, CTA label and destination, and interaction states. Mark each copy slot `plan`, `supplied`, `draft` or `missing`. Words in quotation marks attributed to a real person, the owner included, are `missing` until that person supplies or approves them.
11. **Reusable components:** navigation, button hierarchy, video player, statistics strip, tier card, proof card, curriculum row, FAQ, form field and error, quiz option, loading, empty and confirmation states, each styled as in the reference.
12. **Mobile experience:** the first screen at 390px wide (order and what's visible), video width, where the CTA sits, how statistics and tiers stack (same order as desktop, no sideways scrolling), tap targets, readable text sizes, and zoom never disabled.
13. **Responsive and accessibility behavior:** evaluate layouts at about 1440, 768 and 390px; these are review widths, not device targets. Specify keyboard and focus, touch controls, heading order, labels, contrast, motion, captions, and clearance under sticky elements.
14. **Trust and ethics in the design:** no fake countdowns or seat counters, no invented scarcity, no fabricated statistics, no guaranteed outcomes, no testimonials without permission, no misleading discounts, no AI-generated people presented as the founder, clients or students. Urgency only from the plan's real dates or capacity, with the reason shown.
15. **Dependencies and acceptance.** Missing facts and assets, each with who supplies it and what shows until then. Acceptance checks specific to this business, including at least:
    - The first screen names the audience, the outcome, the mechanism and the next step.
    - The video is in its planned state, with no old or off-message video anywhere.
    - Prices, recurrence and terms match `funnel-plan.md` on every page and state screen; anchors appear only with the plan's evidence.
    - Statistics match section 6 and follow the counter rules.
    - Every assessment result, application outcome and purchase state the plan names is designed.
    - Layouts work at 390, 768, 1265 and 1440px; keyboard, focus, labels, contrast, captions and reduced motion work.
    - No demo, status or developer notes inside the design.
    - Side-by-side screenshots of the build and each model frame read as the base system plus the section 3 overrides, and the generic-output check in visual systems passes.

## design-preview.html and design-references/

`design-preview.html` is a static, nonfunctional page: the first screen plus two or three representative sections, built from the token block with real fonts, the plan's copy (or marked draft copy) and labeled image placeholders. Label it in the page title and a small corner tag, not a banner inside the design. A video that isn't recorded appears only as the labeled design-only slot, with no play button. `design-references/` holds copies of every model frame cited in the section table. Keep it out of public or deployed folders; it is reference material, not production assets.

Example wireframe language (adapt to actual content):

```text
Desktop / 12-column content grid, max 1180px
NAV [brand 3] [method | proof | FAQ 6] [apply 3]
HERO [audience + H1 + explainer + CTA + note 7] [portrait 5]
PROOF [matched case 8] [scope/time/context 4]
METHOD [step 1 4] [step 2 4] [step 3 4]

Mobile / 390px review width, 20px side gutters
NAV [brand] [menu]
HERO [audience → H1 → explainer → CTA → note → portrait]
PROOF [case → context]
METHOD [step 1 → step 2 → step 3]
```

## journey-map.md

Build it from the funnel plan's journey map and page specifications. Provide a flow diagram and this complete action table:

| Source page/section | Element/label | Action type | Destination URL/route/state | Same/new tab | Fields/gate | Success/next step | Error/back/cancel | Evidence/status |
|---|---|---|---|---|---|---|---|---|

Use `plan`, `observed`, `site-stated`, `proposed` or `unknown` status. Every CTA and destination follows the plan; don't add or remove funnel steps. Where the plan lacks a destination, record an explicit named dependency such as `BOOKING_URL — owner to supply` and tell the owner the funnel planner can fill it. Never use a competitor endpoint.

- Application: purpose, step count or estimated effort, validation, consent placement, save and back, the qualification outcomes the plan defines, next step.
- Scheduling: time zone, availability and the empty state, selection, confirmation, reschedule and cancel route. Unknown rules remain dependencies.
- Checkout and purchase: the plan's method, amount, currency and recurrence, the terms shown, and every state the plan names (pending, failed, success, duplicate, access help). Implementation is the builder's.
- Digital fulfillment: guest or member entry, login, reset, access-pending and help states, and who owns access. Do not invent an LMS.
- Resources: browsing, filter and detail routes, with a contextual course action; don't force a sales form before genuinely free public content.
- Contact and legal: real, distinct destinations or named content dependencies. Explain any observed mismatch.

Do not confuse a CTA labeled "Apply" with an application: inspect its actual target.

## asset-manifest.md

For each asset: ID, section, intended subject, dimensions or aspect ratio, crop or focal point, source or path, alt-text intent, supplied or missing status, rights status, and acceptable fallback.

- **Brand files** in `brand/`: status `generated`, the prompt or method used, and rights "created for the owner; not trademark-cleared". A logo the owner supplied is listed as `supplied` and used unchanged.
- **Video:** the sales video (status: final, not recorded yet, or excluded), its poster, captions file and transcript. List each old or off-message video as `excluded` with the reason. A video that doesn't exist yet is a dependency, never filled with another video.
- **Photos and screens:** a missing photograph or product screen gets a labeled placeholder with the reference's crop, corner radius and tone, plus a shot-list entry. Never fill it with an illustration, diagram, icon grid or invented interface. Never substitute synthetic before/after results for evidence.
- **Reference material:** list competitor screenshots, including `design-references/`, separately as reference-only, excluded from production assets.

## Integration notes for the builder

Summarize the design-expressed roles, forms, data ownership, offer and payment terms, delivery, integrations and external destinations, pointing to `funnel-plan.md` for the business facts and checkout mechanics. Record unknown provider accounts and policies without requesting secrets. The builder makes implementation choices consistent with this accepted design and owns functional validation. Do not prescribe Supabase, Stripe or Vercel unless the project or builder requires them.
