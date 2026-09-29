# Interview guide

Use this for step 1 of the skill. It has two readers:

- **You, the agent:** what to read first, what not to re-ask, when to branch, and what to do with "you decide".
- **The owner:** the questions. Most owners have never designed a website, so every question is in plain words with a one-line example and your recommendation. A first-time founder should be able to answer a round in a few minutes.

Contents: [start from the funnel plan](#start-from-the-funnel-plan) · [no funnel plan](#if-there-is-no-funnel-plan) · [how to ask](#how-to-ask) · [design questions](#design-questions) · [follow-up modules](#follow-up-modules) · [defaults](#defaults-for-you-decide) · [message templates](#message-templates) · [no reply possible](#when-the-owner-cannot-answer-in-this-session)

## Where this skill sits

This skill is step 5 of the owner's website pipeline:

1. `educational-funnel` interviews the owner and saves `funnel-plan.md`: the funnel, a backup route, every page, the follow-up emails and a launch checklist.
2. `vsl-scriptwriter` (optional) writes the sales-video script from `funnel-plan.md`.
3. **This skill** designs the website from `funnel-plan.md`.
4. `website-generation` builds it.
5. `website-security` checks it.

Business strategy belongs to step 1. This skill decides how the site looks and how every page, block and state is presented.

## Start from the funnel plan

1. **Find the inputs.** Look in the project folder for `funnel-plan.md`, a video script (a file with "vsl" or "script" in its name), an existing site or page, brand files and photos.
2. **Read `funnel-plan.md` completely before asking anything.** It is the source of truth for business facts: offer, tiers and prices, audience, route, pages, CTAs and destinations, proof, whether there's a sales video, checkout and follow-up.
3. **Never edit it.** Don't rewrite, rename, move or overwrite `funnel-plan.md`, and never create a file with that name. If something in it looks wrong or clashes with what the owner tells you, ask the owner. If the plan must change, tell them to update it with the funnel planner (or by hand); then re-read it.
4. **Don't re-ask what it answers.** Pre-fill the design inputs from it. You may confirm one genuinely unclear point, quoting the plan.
5. **A script file** is read only for its runtime and its opening line or poster wording. Don't review, edit or rewrite the script.

Plans differ by version, so match sections by meaning, not by exact heading. Newer plans have their own sections for most rows below; older plans keep the same facts in the business brief and the page specifications.

| The design needs | Where the funnel plan usually has it | If missing |
|---|---|---|
| Audience and positioning: who, their situations, the core line, promises and non-promises, who it's not for | Audience and positioning section; older plans: business brief, each page's visitor question, FAQ content | Ask (minimum business round) |
| Offer, named mechanism and curriculum | Offer and mechanism section; older plans: business brief, offer page spec | Ask |
| Tiers, prices, recurrence, inclusions, refund terms | Tiers section; older plans: decision summary, plans and checkout page specs | Ask |
| Route, pages, each page's first-screen intent and ordered content, starter copy, CTAs, destinations | Journey map; page and stage specification | Ask what a ready visitor should do; use the [fallback page recipes](conversion-principles.md#page-recipes-by-path-fallback) |
| The video decision: whether there is one, placement, length, language, status | Video (VSL) section; older plans: page ordered content, build walkthrough | Ask ([video module](#video-vsl)), only the parts missing |
| Proof and statistics rules | Proof and statistics section; older plans: readiness and proof, each page's proof row | Ask |
| Assessment or lead-magnet flow: questions, scoring, results, data | Its own section; older plans: the assessment page spec | Ask for a draft, or mark it as a dependency |
| Traffic source, warmth, device mix | Device mix section; older plans: business brief | Ask |
| Language | Language section; older plans: business brief | Ask |
| Existing funnel audit | Its own section, if any | Audit the design side yourself ([existing site](#existing-site-or-page)) |
| Checkout, payment, follow-up emails, systems | Page specs, follow-up design, systems | Not asked. The design shows the screens the plan lists; the builder implements them. |

The funnel plan never covers the look. Always ask the [design questions](#design-questions).

## If there is no funnel plan

Tell the owner the recommended order (template: [no funnel plan](#no-funnel-plan)): run `educational-funnel` to plan the funnel, optionally `vsl-scriptwriter` for the video script, then this skill. The funnel planner does the business strategy properly; this skill only designs. In the same message, ask the minimum business questions below, so an owner who'd rather continue can answer straight away. The design round follows in the next message.

Don't do funnel strategy: no route comparison, follow-up emails, checkout mechanics or economics. Record in the handoff that no funnel plan existed and which answers stand in for it.

**Minimum business questions**

**B1. What do you sell?** Each option, what's in it, its exact price, and one-time or recurring.
Example: "Starter: 30 recorded piano lessons, ₹2,499 one-time. Pro: Starter plus 6 live feedback calls, ₹6,999."
My suggestion: only you know this. Until you tell me, the page shows a marked price slot.

**B2. Who is it for?** Their stage, three to five real situations in their words, and who it's not for.
Example: "Home bakers who sell to friends but can't price their cakes." "Not for people opening a café."

**B3. Where do visitors come from, do they already know you, and do they use phones or computers?**
Example: "Pinterest and my email list, mostly on phones."
My suggestion: phone-first for social traffic.

**B4. What should a ready visitor do, and what happens right after?** Buy, take a free quiz, apply for a call, or join a list. If it's a quiz or an application, share your draft questions or say "later".
Example: "Book a free 15-minute call; I confirm it by email."

**B5. What proof can we show, and what must we never claim?** Testimonials with permission, numbers you can verify, credentials.
My suggestion: no guaranteed results, no income or job promises, no number without a source.

**B6. Do you have a current site or page?** A link or files, and what from your brand must stay.

**B7. Which language on the page, and what tone?**
Example: "English-led Hinglish, warm and encouraging."

## How to ask

1. **Rounds.** With a funnel plan: the design round, then one follow-up round only if needed. Without one: the minimum business round, the design round, then follow-ups. Never more than three rounds. After the last round, record what's still unknown as dependencies. Approving the design direction (step 2) and the preview (step 6) are separate checkpoints, not interview rounds.
2. **Format.** Number every question. Give each one a plain example and your recommendation marked "My suggestion". Group questions under short headings. **Never send more than 12 numbered questions in one message**; fold related details into a/b/c parts, and move the rest to the next round. Without a funnel plan, that usually means the business questions in one message and the design questions in the next. Say that short answers are fine, any order is fine, and "you decide" works for anything with a suggestion.
3. **Always ask,** even when the owner is in a hurry: inspirations; look, closeness and exclusions; brand and logo; imagery; and the video questions the plan doesn't answer.
4. **Facts are never defaulted.** "You decide" covers design decisions. It never covers facts: prices, inclusions, proof, numbers, credentials, terms, dates. An unknown fact becomes a named dependency and a visibly marked slot. Never propose a placeholder price, sample numbers or invented testimonials.
5. **The owner's brand is theirs to judge.** Never decide that their known color, logo or style "isn't a real brand". Ask what must stay. A logo they supply is kept as supplied; the logo rules in [brand assets](brand-assets.md) apply only to logos you create or that they ask you to refine.
6. **Record everything** in `design-direction.md` and the handoff: each answer, each default you applied, each dependency, and the owner's own words for how the site should feel.

## Design questions

### H. Inspirations (always ask)

**H1. Show me what you like.** Links or screenshots of whole sites, or of single parts: a hero, a video block, pricing, a quiz. For each, one line on what you like and anything you dislike.
Example: "That site's big photos and short sections. A pricing table I saw with three columns. Dislike: pop-ups asking for my email."
My suggestion: two or three are plenty. I'll use them inside the one look you choose, never as a second look.

Rule for you: inspect each one. Record a decision for each: *adopt* (what exactly, rebuilt with the base system's tokens), *note only*, or *decline* (why). Never take an inspiration's logo, photos, copy, numbers or results. A whole-site inspiration that should drive the look is option D in I1, not an extra layer.

### I. Look, closeness and exclusions (always ask)

**I1. Which look should the site follow?**
- A) **Aligned:** soft and minimal. Warm ivory, light Inter Tight headings, taupe pill buttons, real photography.
- B) **Launchpad:** dark and product-led. Near-black, bold condensed uppercase headings, an orange button, product screenshots.
- C) **IELTS:** expert education. White with a navy hero band, an orange button, serif numerals. Its hero was captured; other sections are extrapolated.
- D) **Your own reference:** a link or screenshot.

Show or link each option's hero frame ([Aligned](screenshots/aligned-01.png), [Launchpad](screenshots/launchpad-01.png), [IELTS](screenshots/ielts-hero.png)). For a video-led page also show the video frames: [Aligned 02](screenshots/aligned-02.png) and [03](screenshots/aligned-03.png), [Launchpad 24](screenshots/launchpad-24.png). If you can't show images, give the file paths. Recommend one and say why in a sentence. Never choose for the owner unless they say "you decide".

**I2. How closely?** (a) closely: its fonts, colors, spacing and components, with your content; (b) its layout and components with your own brand colors and fonts; (c) loose inspiration.
My suggestion: (a). It is the surest way to look professional on a first site.

**I3. What should we leave out or change?**
Example: "Leave out the team section; I work alone."

**I4. Only when their brand clashes with the chosen look.** Name the clash and offer a choice:
"Your teal isn't part of the Aligned look, which uses only warm neutrals. Which do you prefer? (a) Keep the Aligned look exactly and use your teal in your logo, social images and videos. (b) Use your teal for one job on the site, such as the main button, in place of Aligned's taupe. (c) Choose a look that already suits your teal."
My suggestion: (a) or (b). Never both palettes.

Rule for you: the answer becomes the override list in the handoff. A site with two palettes or two type systems fails the quality gate. When the owner's brand covers fewer roles than the system has (one brand color, say, where the system has a band color and a button color), their color replaces only the role they chose; every other role keeps the system's value. Shades of the chosen role (a raised or hover version) follow it: derive them the way the system does and label them extrapolated. Never invent a replacement color for a role the owner didn't mention; ask.

### J. Brand and logo

**J1. Do you have a logo, brand colors and fonts?** Keep, refine, or create new.
My suggestion: with no brand colors or fonts, the site uses the chosen look's own. No logo yet? I'll design one ([logo module](#logo)).

### K. Imagery

**K1. What photos or screens can you supply?** Photos of you or your team, student or client photos (with permission), course or product screenshots.
My suggestion: two or three natural-light portraits of you are enough to start. Until they exist, the page shows plain labeled boxes, never illustrations.

### L. Video (always ask what the plan doesn't answer)

**L1. Do you want a sales video on the page?** A sales video (often called a VSL) explains the offer in a few minutes, so visitors can watch instead of reading everything.
My suggestion: yes for warm social traffic. If you'd like one, see the [video questions](#video-vsl).

### M. Numbers strip

**M1. Which true numbers should sit under the video or headline?** Three or four. When the funnel plan lists proof, propose the numbers from it and ask for a yes.
Example: "1,200 students since 2019; 36 lessons; 12 live calls."
My suggestion: verified results if you have them; otherwise honest facts about the offer (lessons, sessions, access). Never invented results.

### N. Motion, must-haves and devices

**N1. Motion:** none, subtle (gentle fade-ins, one-time counters) or lively?
My suggestion: subtle, and switched off for visitors whose device asks for less motion.

**N2. Must-haves and must-avoids:** sections, features or effects you want or never want.
Example: "Must: a refund FAQ near the price. Never: pop-ups or auto-playing music."

**N3. Phone or desktop first?** Skip if the plan gives the device split.
My suggestion: phone first for social traffic, desktop first for work-hours B2B traffic; both must work.

## Follow-up modules

Ask a module in the round where its trigger appears. Skip whatever is already answered.

### Video (VSL)

Trigger: the plan includes a sales video, or L1 is yes.

1. **Placement:** (a) centerpiece of the first screen, (b) beside the headline, (c) just below the first screen, (d) none.
   My suggestion: (a) for warm social traffic; (b) or (c) for cold traffic and considered, high-ticket offers. See [placement](conversion-blocks.md#placement).
2. **Does it exist?** Recorded, script ready, or not started. If recorded: what it's about, how long, when it was made.
3. **About how long?** My suggestion: a few minutes for a low-ticket offer to warm traffic; longer only when the decision needs it.
4. **Language** of the voice, and of the captions.
5. **Who's on camera?** You, a team member, or screen recording only.
6. **Poster:** a still of you, or a real moment from the video, with one benefit line.
7. **Captions and a transcript:** confirm both will exist. My suggestion: yes; many people watch with the sound off.

If they need a script, say only: "The `vsl-scriptwriter` skill can write it from your funnel-plan.md." Don't ask script questions, and don't write, outline or brief a script.

Rule for you: until the final video exists, the video block is hidden on the live site and appears in the preview only as a labeled design slot. An old or off-message video never stands in for it. See [video states](conversion-blocks.md#video-states).

### Logo

Trigger: J1 says no logo, or asks for a refinement. Ask the six logo questions in [brand assets](brand-assets.md#1-investigate-before-drawing) in the design round.

### Existing site or page

Trigger: the owner has a current site, page or videos. If the funnel plan has an existing-funnel audit, start from it and add only the design side. Inspect the site yourself before the design round and bring findings, not questions:

- Brand DNA worth keeping: logo, a known color, photos, phrases.
- Videos: what each one sells, its length and date, and whether it's on-message for the new offer.
- Claims and pressure tactics visible on the page (numbers, testimonials, discounts, countdowns), so none is carried into the design unverified. The funnel plan decides the offer; the design only refuses to display what isn't true.

Then ask one question: "Here's what I'd keep from your current page: …. OK?"

## Defaults for "you decide"

Apply these only to design decisions, and list each one in `design-direction.md` under "Decided for you".

| Decision | Default |
|---|---|
| Reference look | The best fit: Aligned for coaching and personal brands with real photos or video; Launchpad for courses and memberships with a real product interface; IELTS for expert education and exam or skill training. |
| Closeness | Match closely. |
| Brand-color clash | Keep the look exactly; the owner's color stays in the logo, social images and videos. |
| Hero with no photo shoot | The system's no-photography opening, or the VSL-first hero when a video is planned. |
| Video placement | Warm social traffic: centerpiece of the first screen. Cold or high-ticket: beside the headline or below the first screen. |
| Video not recorded yet | Hidden on the live site; labeled design slot in the preview. |
| Numbers strip | Truthful offer facts until verified results exist. |
| Motion | Subtle; off under reduced-motion settings. |
| Device priority | From the plan's traffic; otherwise phone first for social traffic, desktop first for work-hours B2B traffic. |
| Tiers | Side by side on desktop, stacked in the same order on phones. |
| Logo | A wordmark in the system's display font, with one ownable detail. |

Facts with no answer (prices, proof, terms, dates) are not defaults. They become dependencies and marked slots.

## Message templates

Adapt the wording to the owner and their language. Remove anything already answered. Keep the numbering continuous so the owner can reply "3: yes, 5: you decide".

### No funnel plan

Send the recommended order and the minimum business questions (below) as one message, so the owner can choose without an extra round trip:

```text
Hi [name]! I don't see a funnel-plan.md in this folder. The recommended order is:
1. The educational-funnel skill plans your funnel: who it's for, your offer and prices, every page and what each button does. It saves funnel-plan.md.
2. (Optional) The vsl-scriptwriter skill writes your sales-video script from that plan.
3. Then I design the website from the plan.

If you'd like to plan the funnel first, just say so. Otherwise answer the questions below and I'll continue from your answers.
```

### Design round (with a funnel plan)

```text
Hi [name]! I've read your funnel plan: [one line: offer and prices, who it's for, the path, e.g. "video → free quiz → your result → plans → checkout"]. I won't ask you anything it already answers. These questions are about how the site should look. Short answers are perfect, and "you decide" works for anything with a suggestion.

Inspiration
1. Share links or screenshots of anything you like, whole sites or single parts (a video block, pricing, a quiz), and one line on what you like or dislike about each.

The look
2. Which look should your site follow? A) Aligned: soft and minimal [link]. B) Launchpad: dark and product-led [link]. C) IELTS: expert education [link]. D) Your own example. My suggestion: [letter], because [reason].
3. How closely: match it closely, keep its layout with your own colors and fonts, or loose inspiration? My suggestion: closely.
4. Anything to leave out? For example "leave out the team section".
[If their brand clashes:] 5. Your [color] isn't part of the [look]. (a) keep the look exactly and use your color in your logo and videos, (b) use it for [one job] on the site, or (c) pick a look that suits it? My suggestion: [a or b].

Brand and pictures
6. Logo, colors and fonts: keep, refine, or create? [If none: add the logo questions.]
7. What photos or screens can you supply? My suggestion: 2–3 natural-light portraits of you.

Your sales video
8. Your plan includes a sales video [and already says: …]. [Ask only what the plan leaves open:] Where should it go (centerpiece of the first screen / beside the headline / lower down)? Is it recorded yet? About how long, in which language, and who's on camera? Will it have captions? My suggestion: [placement]. [If there's no script: "If you need a script, the vsl-scriptwriter skill can write it from your funnel plan."]

Finishing touches
9. Numbers under the video: I'd use [numbers from the plan's proof]. OK?
10. Motion: none, subtle or lively? My suggestion: subtle.
11. Must-haves and must-avoids? For example "a refund FAQ near the price; never pop-ups."

Next I'll send you a one-page design direction to approve before I design anything.
```

### Minimum business round (no funnel plan)

```text
A few business questions first, since there's no funnel plan. Short answers are fine; say "later" for anything you haven't decided.

1. What do you sell? Each option, what's in it, its exact price, one-time or recurring.
2. Who is it for, what 3–5 real situations do they struggle with (in their words), and who is it not for?
3. Where do visitors come from, do they know you already, and phone or computer?
4. What should a ready visitor do (buy, free quiz, apply for a call, join a list), and what happens right after? For a quiz or application, your draft questions or "later".
5. What proof can we show (testimonials with permission, numbers you can verify, credentials), and what must we never claim?
6. A current site or page? What must stay from your brand?
7. Which language and tone? For example "English-led Hinglish, warm and encouraging".

After this I'll ask about the look, then send a one-page design direction for you to approve.
```

### Follow-ups

```text
Almost done. A few details for [the video / your logo / the look]:

1. [Module question, with an example and "My suggestion".]
2. …

Anything you don't know yet, say so. I'll mark it as something to add later rather than guess.
```

### When the owner says "don't wait on me"

```text
Understood. I'll use my suggestions for every open design decision and list them in design-direction.md under "Decided for you", so you can change any of them later. I won't invent facts: prices, proof or details that aren't in your funnel plan or your messages will show as marked slots until you send them.
```

## When the owner cannot answer in this session

If nobody can reply (an autonomous or scheduled run, or a request to finish without replying), write the next round's questions, with your recommendations, to `design-questions.md` in the project, say where it is, and stop. Don't design on guesses. When the answers arrive, continue from where you stopped.

"Don't wait on me" is different: the owner delegated, so apply the defaults and continue.
