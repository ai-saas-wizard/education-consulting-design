# Reference visitor journeys — checked 17 September 2026

Scope: all distinct homepage navigation/action destinations, major conversion branches, and useful downstream pages. Duplicate links are grouped. Deep article archives, every video, all social content, and authenticated journeys were not exhaustively tested. Public pages were inspected in browser or web reader; no real/fake applications, appointments, accounts or purchases were submitted. URLs are evidence only, never endpoints for a new client's site.

Status: **observed** = visible page/behavior; **linked** = target extracted but destination not fully inspected; **site-stated** = promised next step; **unknown** = gated or not exercised.

## Aligned Fitness

```text
Homepage → section navigation / video / proof / bios / FAQ
         → coaching CTA → Typeform welcome → first question (1 of 18)
                       → [remaining answers + submission: unknown]
         → legal links → shared privacy page
```

| Element | Destination / behavior | Evidence and limit |
|---|---|---|
| Programs navigation | In-page programs section | Button clicked; same page retained, smooth scrolling observed. |
| Success Stories navigation | In-page success-stories section | Button clicked; same page retained. |
| About navigation | In-page founder section | Button clicked; same page retained. |
| FAQ navigation | In-page faq section | Button clicked; same page retained. |
| Work With Us / Start Your Transformation / Apply for Coaching | [Typeform](https://form.typeform.com/to/hB1pnBuk?typeform-source=www.alignedfitnesscoaching.org) | All three CTA variants clicked; application tab observed. Start opens welcome screen; advancing welcome reveals question 1 of 18, requesting first name. |
| Video/proof cards | Embedded play controls; transformation images exposed as buttons | Controls inventoried, individual playback/lightbox behavior not exhaustively exercised. |
| Team bios and FAQs | Expandable content on homepage | Controls and associated content observed; not a separate route. |
| Privacy / Terms | Both target [privacy-policy](https://www.alignedfitnesscoaching.org/privacy-policy) | Same href observed; fetched page title refers to Hallie June. Treat label/identity consistency as an audit item. |

Welcome eligibility mentions employment and adult age. This is observed reference behavior, not a recommended universal rule. The homepage describes a call-led engagement; the actual post-submission routing was not reached. Do not assert that Typeform definitely auto-books or displays a calendar. [Application screenshot](screenshots/aligned-application.png).

## Digital Launchpad

```text
Homepage repeated CTA → #pricing → monthly access action
  → branded checkout step 1 (contact details) → [step 2 gated]
  → [payment/receipt/access unknown; URL declares app return target]
```

| Element | Destination / behavior | Evidence and limit |
|---|---|---|
| Repeated main actions | [#pricing](https://join.digital-launchpad.com/#pricing) | Hrefs grouped and one action clicked; hash destination verified. |
| Comparison's alternative action | Homepage URL | Linked back to the same page rather than an educational alternative. Don't copy as a deceptive choice. |
| Monthly access | [Checkout](https://checkout.digital-launchpad.com/pay/price_1OgrJGDM6ttbLpZZtNZh6uzb:1?isAuth=0&isEmbedded=1&formFields=email:email:required_firstName:string:required_lastName:string:required_phoneNumber:phone:&returnUrl=https://app.digital-launchpad.com) | Observed two-step progress. First step requires email, first and last name; phone shown optional. Next disabled with empty required fields. No data entered. |
| Course content, sample lessons, proof, FAQ | On-page catalog, slideshow controls and grouped FAQ | Controls/content inspected, no evidence that catalog items provide public paid-course access. |
| Contact | [educate.io/contact-us](https://educate.io/contact-us) | Web reader redirected to [Consulting.com](https://consulting.com/), not a dedicated contact page in that observation. Recheck before relying on it. |
| Legal | [Privacy](https://join.digital-launchpad.com/policies/privacy), [Terms](https://join.digital-launchpad.com/policies/terms) | Both destinations fetched successfully. |

Pricing displayed $37/month, billed monthly during inspection. Store this as dated evidence, not a default price. The checkout URL contains an intended return to `https://app.digital-launchpad.com`; actual payment success, provisioning, login and cancellation are unverified. [Checkout screenshot](screenshots/launchpad-checkout.png).

## Metabolic Makeover Academy

```text
Homepage / about / testimonials → coaching application
 → contact + qualification form → [submit not performed]
 → calendar + strategy call (site-stated, not observed)
Homepage → contact / social
About → book purchase on Amazon (linked)
```

| Element | Destination / behavior | Evidence and limit |
|---|---|---|
| Brand | [Homepage](https://www.metabolicmakeoveracademy.org/) | Observed anchor. |
| About / Meet Coaches | [About](https://www.metabolicmakeoveracademy.org/about) | Loaded founder story, team, book branch and application links. |
| Testimonials | [Results](https://www.metabolicmakeoveracademy.org/testimonials) | Public result page fetched. |
| Contact | [Contact](https://www.metabolicmakeoveracademy.org/contact) | Public contact page fetched. |
| All main start/apply actions | [LeadConnector application](https://api.leadconnectorhq.com/widget/form/aZFeCfUfowDY3F3GStXJ) | Same URL throughout homepage; actual form inspected. |
| Social footer | [Instagram](https://www.instagram.com/metabolicmakeoveracademy/), [YouTube](https://www.youtube.com/@metabolicmakeoveracademy) | Target links observed; platform content not audited. |
| About-page book action | Amazon book destination | Linked from About; purchase not exercised. |
| Form terms | `https://example.com/` | Placeholder href observed. Must not be carried into a new design. |
| Form privacy | `https://metabolicmakeoveracademy.com/privacy-policy` | Different .com host from .org marketing site; linked, not verified here. |

The application requests identity/contact, age, Instagram, goals/barriers, employment/location/work, readiness, investment willingness, and attribution. Form states minimum age 21, and says scheduling follows submission. Consent includes text messaging. These details reveal a high-friction qualification path; adapt only justified questions and explain the next step. No calendar/availability/confirmation was reached. [Form screenshot](screenshots/mma-application.png).

## IELTS Advantage

```text
Homepage → VIP Academy → pricing anchor → branded checkout ($497 one-time)
                                 └→ alternate Stripe action ($397 USD displayed)
         → diagnostic → eligibility question 1 of 3 → [gated onward path]
         → free course → email registration → [delivery unverified]
         → resources / student proof / contact / policies
```

| Element | Destination / behavior | Evidence and limit |
|---|---|---|
| Main VIP actions | [VIP Academy](https://www.ieltsadvantage.com/vip-academy/) | Loaded long-form sales page. |
| Course-page repeated Apply actions | [Pricing anchor](https://www.ieltsadvantage.com/vip-academy/#vip-pricing-card) | Hrefs inspected; label does not itself imply an application form. |
| Enroll action | [Branded checkout](https://pay.ieltsadvantage.com/vip-3) | Loaded: $497 one-time, email + Continue, terms links, stated instant access. No email entered. |
| Additional Apply action | [Stripe checkout](https://buy.stripe.com/bJe5kE4oJ4gA7ey9ad5kk0x) | Also visible on course page. Loaded: IELTS VIP 3.0, $397 USD option plus localized currency; email/card/billing fields. Different prices observed, reason unknown. Do not assume equivalent offers or a guaranteed discount. |
| Diagnostic | [submit.ieltsadvantage.com](https://submit.ieltsadvantage.com/) | Homepage advertises a $10 diagnostic. Destination initially checks location then displays question 1 of 3 about exam timing, with two 21-day options. Later questions/payment/result unknown. |
| Free-learning action | [Fundamentals](https://my.ieltsadvantage.com/) | Fetched course opt-in page requesting name/email. Actual signup and delivery untested. |
| Success stories | [Video evidence page](https://www.ieltsadvantage.com/video-success-stories/) | Destination fetched. |
| Resources | [Preparation hub](https://www.ieltsadvantage.com/ielts-preparation/) | Destination fetched; routes learners to subject material. |
| Subject navigation | [Writing 1](https://www.ieltsadvantage.com/writing-task-1/), [Writing 2](https://www.ieltsadvantage.com/writing-task-2/), [Speaking](https://www.ieltsadvantage.com/ielts-speaking/), [Reading](https://www.ieltsadvantage.com/ielts-reading-2/), [Listening](https://www.ieltsadvantage.com/ielts-listening-2/), [Vocabulary](https://www.ieltsadvantage.com/ielts-vocabulary-2/) | All six fetched as learning resource pages; deep article links not recursively audited. |
| Contact | [FAQ/contact](https://www.ieltsadvantage.com/faq-and-contact/) | Destination fetched. |
| Footer/checkout policies | [Terms](https://www.ieltsadvantage.com/terms-and-conditions/), [Privacy](https://www.ieltsadvantage.com/privacy-policy/), [Refund/guarantee](https://www.ieltsadvantage.com/refund-and-guarantee-policy/) | All fetched; distinct policy destinations. |
| Logo / skip links | Homepage / main-content anchor / footer anchor | Homepage anchors observed. |

Guarantee wording differs in specificity between homepage and sales page; design consistent summaries with proximate conditions rather than copying slogans. Price discrepancies and diagnostic prequalification are strong reasons to inspect the destination behind every CTA. [Diagnostic screenshot](screenshots/ielts-diagnostic.png).

## Flow lessons for future handoffs

Specify every screen, transition, gate and recovery route. Keep a consistent offer identity from landing page through checkout. Explain form effort before external navigation. Distinguish stated fulfillment from verified fulfillment. Never claim a live purchase or booking was tested when inspection stopped at its entry form. For new designs, propose success and failure states explicitly even when reference sites hide theirs.
