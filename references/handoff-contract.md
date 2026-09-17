# Builder-ready design contract

Compatible with the inspected `website-generation/references/design-handoff.md` contract on 2026-09-17: a concrete brief with a selected visual direction is an accepted design input. This schema is portable and does not require that exact builder.

## design-handoff.md

1. **Status and brief:** business, audience, offer, traffic context, main conversion, chosen direction, assumptions, source references, scope exclusions.
2. **Page inventory:** route, page job, entry source, main action, next route/state. Include needed application, booking, confirmation, checkout, access-help, resource, and policy surfaces; do not add pages gratuitously.
3. **Visual system:** specific color roles/hex, typography/fallbacks/weights/sizes/line heights, spacing scale, maximum width, columns/gutters, border/radius, image ratios, components, interaction and focus treatments. State proposed breakpoints and why elements reflow.
4. **Per-page wireframes:** desktop and mobile diagrams with labeled content areas, realistic relative widths, hierarchy, and section order. A diagram plus tokens and section specs is the minimum concrete design, even without a rendered mockup.
5. **Per-section table:** ID, visitor question/job, draft headline and content slots, desktop layout, mobile layout, media dimensions/crop, proof source, CTA label/destination, and interaction states. Mark each copy slot `supplied`, `draft`, or `missing`.
6. **Reusable components:** navigation, button hierarchy, proof card, curriculum row, FAQ, form field/error, loading, empty, confirmation, and any offer-specific component.
7. **Responsive/accessibility behavior:** evaluate proposed layouts at approximately 1440, 768, and 390px; these are design review widths, not required device targets. Specify keyboard/focus, touch controls, heading order, labels, contrast, motion, captions, and sticky element clearance.
8. **Dependencies and acceptance:** missing facts/assets, consequential decisions for the owner, concrete visual/journey acceptance checks, and handoff files.

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

Provide a flow diagram and this complete action table:

| Source page/section | Element/label | Action type | Destination URL/route/state | Same/new tab | Fields/gate | Success/next step | Error/back/cancel | Evidence/status |
|---|---|---|---|---|---|---|---|---|

Use `observed`, `site-stated`, `proposed`, or `unknown` status. For external providers, record the business-owned destination if known; otherwise use an explicit named dependency such as `BOOKING_URL — owner to supply`. Do not use a competitor endpoint.

- Application: explain purpose, step count or estimated effort when known, validation, consent placement, save/back expectations, qualification outcomes, next step.
- Scheduling: time zone, availability/empty state, selection, booking confirmation, reschedule/cancel route. Unknown rules remain dependencies.
- Checkout: offer/amount/currency/recurrence when supplied, terms, pending/declined/success states, duplicate-submit handling as an implementation requirement, receipt and access instructions.
- Digital fulfillment: guest/member entry, login/reset/access-pending/help states; who owns access. Do not invent an LMS.
- Resources: browsing/filter/detail route and contextual course action; avoid forcing a sales form before genuinely free public content.
- Contact/legal: real distinct destinations or named content dependencies. Explain any observed mismatch.

Do not confuse a CTA labeled 'Apply' with an application: inspect its actual target.

## asset-manifest.md

For each asset: ID, section, intended subject, dimensions/aspect ratio, crop/focal point, source/path, alt-text intent, supplied/missing status, rights status, and acceptable fallback. List competitor screenshots separately as reference-only and exclude them from production assets. Never substitute synthetic before/after results for evidence.

## Integration notes for the builder

Summarize design-expressed roles, forms, data ownership, offer/payment terms, delivery, integrations, and external destinations. Record unknown provider accounts and policies without requesting secrets. The builder makes implementation choices consistent with this accepted design and owns functional validation. Do not prescribe Supabase/Stripe/Vercel unless the project or builder requires them.
