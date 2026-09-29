# Conversion blocks

How to present the blocks that decide whether a funnel page converts: the sales video (VSL), the statistics strip, pricing, the screens around checkout, the assessment and the application.

What each page contains, and in what order, comes from `funnel-plan.md`. This file covers presentation: layout, behavior, states and what never to do. Checkout mechanics (payment provider, verification, emails) belong to the funnel plan and the builder. How each block looks in each visual system is in [visual systems](visual-systems.md), in each system's "Funnel blocks" section.

Contents: [VSL](#1-vsl-block) · [statistics](#2-statistics-strip-and-counters) · [pricing](#3-pricing-display) · [checkout and purchase screens](#4-checkout-and-purchase-screens) · [assessment](#5-assessment-or-quiz-screens) · [application](#6-application-screens)

## 1. VSL block

A VSL (video sales letter) is a short video that explains the offer and asks for the next step. The page must still work, and still sell, without it.

### Placement

Match placement to traffic warmth and the video's job ([guide, Part III §2](high-converting-landing-page.md#2-where-the-video-should-go)). Use the funnel plan's traffic and page order, and the owner's answer to the placement question.

| Placement | Use when | Order |
|---|---|---|
| **Video-first centerpiece** | Warm traffic that already knows the owner (Instagram, YouTube, email list). The video carries the pitch. | Compact header → audience qualifier → outcome headline → one support line → large centered 16:9 player → CTA with microcopy directly under it → statistics strip |
| **Beside the headline** | Considered or high-ticket offers, mixed or cold traffic. The page must work without playing. | Copy column about 55% (qualifier, headline, mechanism and effort subhead, CTA, microcopy) beside the video at about 45% (benefit poster, captions, play control, one proof caption). Proof strip of three to five items below. |
| **Below the first screen** | Cold traffic that needs the promise and proof before a long video, or a system whose hero can't hold a player. | The system's own hero, then a section with a centered heading, the player and the CTA |
| **None** | No video planned | The system's hero with CTA and proof strip |

Rules:
- The first screen explains audience, outcome and next step without playing anything.
- The player is the one dominant visual. No competing hero photo, illustration or diagram.
- The CTA is visible and working from the first second. Never hide or delay it until a timestamp: that blocks ready buyers and fails accessibility.
- "Compact header" means the logo and one button (or the system's logo-only header), without full navigation. At 390px the button stays on one line; give it a shorter label on phones if needed (for example "Start the check").
- On a laptop screen the CTA under a large player usually falls just below the fold. Where the system's header has a button, give it the same label so the next step is always visible.
- Don't force a split into a system whose hero is centered (IELTS). Use the centerpiece or below-the-first-screen placement there.

### Size and behavior

- **Shape:** 16:9.
- **Width, desktop:** the system's centered media width: Aligned 1024px, Launchpad about 794px, IELTS 800px (see each system's "VSL-first hero"). Beside the headline: the video column.
- **Width, phones:** the full content width. At 390px with 24px gutters that is 342×192px. The CTA sits directly under the player and may span the content width.
- **Duration** on the poster before play (for example "8:40"), in the system's small label style.
- **Controls:** play and pause, seek bar, elapsed and total time, mute and volume, captions toggle, fullscreen, and optionally speed. Keyboard operable, with a visible focus ring. Don't block seeking and don't hide the controls. (The Aligned live site hides native controls and stops viewers skipping ahead; don't copy that part.)
- **Captions** in the language the owner chose, on by default when a video starts muted. A **transcript** as a "Read the transcript" disclosure under the player, or on a linked page.
- **Autoplay:** never with sound. Default is click to play. Muted autoplay only if the owner insists, and then with captions on, a clear unmute control, and no looping.
- **Loading:** show the poster and load the player only on click, which keeps slow phone connections fast. Hosting is the builder's choice. Turn off end-screen recommendations where the host allows.
- **Microcopy** under the CTA says what happens next, how long it takes and whether it costs money, using the funnel plan's wording where it has some. Example: "Free · takes about 2 minutes".

### Poster frame

- The owner's face looking at the camera (or toward the CTA), or a real frame from the video's demonstration.
- At most one short benefit line, set in the system's type. If a script file exists, take the line from its opening.
- The duration.
- Never a generic laptop mockup, a big play icon with no information, an old video's thumbnail, stock people, "LIVE" on a recording, or a face looking away from the page.

### Video states

| State | Live site | `design-preview.html` |
|---|---|---|
| **The final video exists** | The player as specified, with poster, duration, captions and transcript. Missing captions or transcript are dependencies to finish before launch, not a reason to hide the video. | The real poster, or a still from the video, with the real duration and play control. Without a still in the project yet, a labeled poster placeholder inside the player frame, with the real duration; list the still as a dependency. |
| **Not recorded yet** | The whole block is hidden. The hero closes up: qualifier → headline → support line → CTA with microcopy → statistics strip. No "video coming soon". | A **design-only slot**: a flat block at the player's exact size and corners, in the system's surface color, with a small label such as "VSL slot, design only. Hidden on the live site until the final video exists. About 8 min, English." No play button, no duration, no controls, no poster art pretending to be a video. |
| **Only an old or off-message video exists** | Same as not recorded. | Same design-only slot. |

A video is **on-message** only if it sells this offer, to this audience, at today's price and terms. An old reel about a different promise, a webinar made for a different audience, or another product's video is off-message even when it's the owner's own. Never embed it "until the new one is ready". Never use a stock clip, an AI avatar presented as the owner, or a fake playable placeholder.

### Script

This skill doesn't write, outline or brief the script. If the owner needs one, tell them the `vsl-scriptwriter` skill can write it from `funnel-plan.md` (or from their brief when there is no plan). If a script file already exists, read it only for its runtime (the duration label) and its opening line (the poster's benefit line).

## 2. Statistics strip and counters

**Content**
- Three to five items, taken from the funnel plan's proof and confirmed by the owner. Each has a number, a short label, a source and a period, recorded in the handoff.
- Verified results only, with their source: "1,200 students since 2019" backed by enrolment records.
- Without verified results, use truthful offer facts: lessons, sessions, access length, years of experience.
- Never invented results, ratings, success rates or percentages. A number on an old page is unverified until the owner confirms it.

**Behavior (for the builder)**
- The final value is in the HTML, so screen readers, visitors without JavaScript, search engines and screenshots all get the true number.
- Default: no count-up. The number fades or rises in with its section.
- If the owner wants a count-up: start at no less than half the final value, run once when the strip is about 40% visible, finish within about 1.6 seconds, never loop, and hide the moving digits from assistive technology (`aria-hidden`) while the final value stays exposed.
- `prefers-reduced-motion: reduce` means no animation: show the final value.
- Never show "0", or any misleadingly low number, even for a moment.
- Example values are allowed only in the preview, marked "example" in the label itself, and never shipped.

## 3. Pricing display

Tiers, prices, recurrence, inclusions and terms come from `funnel-plan.md`, exactly as written there. Ask only when there is no plan.

**Each tier card**
- Name, and a one-line "best for".
- Price with its recurrence on the same line: "₹2,499 one-time", "$97 a month, cancel anytime", "3 payments of $330 ($990 total)". Say whether tax is included when the plan does.
- What's included, in the same order on every card. A higher tier says "Everything in [lower tier], plus:" and lists only the differences.
- Access length and delivery as the plan states them: "Lifetime access · login emailed right after payment".
- One CTA per tier that names it: "Get Starter, ₹2,499". It leads where the plan says (checkout with that tier chosen, an application, a call).
- The refund or guarantee line under the CTA, in the plan's exact terms.

**Recommended tier:** mark one only with a real reason ("Best if you want feedback on your work"). "Most popular" needs sales data.

**Anchors:** a crossed-out price, "save ₹X" or "% off" appears only when the funnel plan records that the exact offer really sold at the higher price, or that a real launch price ends on a stated date. The owner wanting one is not evidence. Otherwise the price stands alone. No value stacks with invented totals.

**Layout:** side by side on desktop. Stacked on phones in the same order (left to right becomes top to bottom). No sideways scrolling, and no differences hidden behind hover.

**High ticket:** show the price or "Investment from $4,500" when the plan says to, with its payment options and inclusions, near the application CTA.

## 4. Checkout and purchase screens

The funnel plan names the payment method, what the buyer does and what each state says. The design doesn't choose providers or specify payment mechanics. It gives the screens the plan lists a consistent look:

- **Order summary:** the system's pricing or offer card with the tier name, a short list of inclusions, the exact amount and recurrence, and the plan's refund and access terms visible before the pay action.
- **Forms:** the system's field and button styles (see each system's "Forms, quiz and checkout"), labels above fields, errors in words beside the field, one primary action, and "back to plans" keeping the chosen tier.
- **Codes and QR images** the plan requires sit on a white tile with a clear margin, even in dark systems, with a text alternative.
- **Trust marks** only if true (the provider's name, "secure checkout"). No invented badges, no "12 people are viewing".
- **Every state the plan names**, each saying what happens next in the plan's words: success, pending, failed, cancelled, duplicate, access not received, refund request.
- The promised timing is word-for-word the same on the page, the checkout screens, the confirmation and the emails the plan lists.

## 5. Assessment or quiz screens

Questions, answer options, scoring and result content come from the funnel plan. The design makes the screens easy and honest:

- **Entry:** what they get, how long it takes, that it's free, and whether an email is needed to see the result, in the plan's words. Example: "5 questions · about 2 minutes · see your result instantly".
- **One question per screen,** with large tappable options at least 48px tall and a clear selected state.
- **Honest progress:** "2 of 5 · your goals". Back keeps the answers.
- **Contact details last,** with why they're asked, marketing consent unticked by default, and a privacy link.
- **No fake "analyzing your answers" delay.**
- **Result page:** the result's name and meaning, the plan's first steps, how the method addresses it, the recommended tier with its reason and the other tier still visible, and the CTA. Design one layout that fits every result type in the plan.
- **States:** entry, each question, nothing selected, back, contact errors, submitting, result, email sent, email failed, retake.

## 6. Application screens

Questions, qualification rules and outcomes come from the funnel plan. The design presents them:

- **Before the click:** what the application involves, what happens next and the price or threshold, in the plan's words. Example: "6 questions · about 5 minutes · you'll hear back within 3 days".
- **Steps:** one topic per screen or group, honest progress ("3 of 6 · your team"), save and back, and a review screen before submitting. No phone number first.
- **Outcome screens** for each outcome in the plan: under review (when they'll hear back), qualified (scheduling, with the time zone shown), not a fit yet (a respectful message and the plan's alternative).
- **After booking:** confirmation with the date and time in their time zone, how to prepare, and a reschedule or cancel route.
- **Capacity** only as the plan states it, with its real reason: "We run two cohorts a year of 20 people each."
