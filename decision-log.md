# Decision Log

## Parked Ideas

Ideas that came up before the problem was defined. They are recorded so they
are not lost, then compared fairly with other ideas during ideation.

### Idea A: All-in-one selling app (PM's idea, 2026-10-16)

One app that connects to Vinted, Kleinanzeigen, and other selling platforms.

- Choose which platforms to post an item on.
- AI-enhanced photos.
- See what the same item from the same brand sells for, and its original price.
- AI writes the listing text.
- All incoming messages from every platform in one inbox.
- When an item sells, it's automatically removed from the other platforms.
- A DHL shipping QR code is created automatically; the seller only packs it.

Status: **parked until ideation.** Not evaluated yet.

## Approved HMW

> How might we help someone with a pile of unworn clothes turn their intention
> to sell into listed items, when each piece takes effort and they doubt it's
> worth it?

## Ideas

_Generated 2026-10-16. Not yet evaluated._

| # | Idea | What it is | Responds to |
|---|---|---|---|
| A | All-in-one selling app (PM, parked) | One app connected to several platforms: AI photos, price comparison, AI text, shared inbox, auto-delist, shipping label. | Effort per item (phases 2-4) and post-listing friction |
| B | Worth-it check | Snap one photo or the label; get a likely sale price and estimated minutes of effort, then decide: sell, donate, or keep. | "Is it worth it?" at phase 2; mood turns at the price check |
| C | One-session pile sprint | A guided session for the whole pile: sort fast into sell/donate, photograph everything in one daylight slot with a minimal photo set, list in a batch. | Effort repeated per item; daylight delay; desk-research workaround (one session, no "later" pile) |
| D | Hand it over | Someone collects the pile and sells it on commission. The person never photographs or lists. | "Too much effort" overall; giving up on the whole pile |
| E | One photo, many listings | Lay several items out and take one photo; the items are split into separate draft listings to finish later. | Photo effort and lighting (phase 3); effort per item |
| F | Little-and-often challenge | One item a day, with a visible tracker of money earned and pile shrinking. | Progress feeling unachievable; desk-research workaround (a few listings a day) |
| G | Sell-by date | Every listed item gets a deadline (e.g. 14 days); unsold items automatically go into a scheduled donation pickup. | Discouragement from unsold items (phase 5); the pile lingering |
| H | Swap instead of sell | Trade clothes with friends or at swap events instead of selling. Challenges the frame: the goal becomes "clothes go somewhere useful", not "listed". | Doubt about payoff; effort of selling |

## Selection Criteria

_Proposed by Claude on 2026-10-16. Accepted by the PM without changes._

Score each idea 1 (low) to 3 (high):

| Criterion | Question |
|---|---|
| User value | Would this meaningfully address the evidence: the per-item effort and the "Is it worth it?" doubt? |
| Learning value | Could a prototype test an important assumption from the open questions? |
| Feasibility today | Can a convincing first prototype be built and tested today? |
| Risk (3 = low risk) | What could mislead, exclude, or disappoint users? |

## PM Shortlist

PM favourites (2026-10-16): **E, F, G**.

## Scoring

_Proposed by Claude on 2026-10-16 using the criteria above. PM did not change the scores._

| # | Idea | User value | Learning value | Feasibility today | Risk (3 = low) | Total |
|---|---|---|---|---|---|---|
| A | All-in-one selling app | 3 | 1 | 1 | 2 | 7 |
| B | Worth-it check | 2 | 3 | 3 | 2 | 10 |
| C | One-session pile sprint | 3 | 2 | 3 | 3 | 11 |
| D | Hand it over | 2 | 1 | 1 | 2 | 6 |
| **E** | **One photo, many listings** | 3 | 3 | 2 | 2 | **10** |
| **F** | **Little-and-often challenge** | 2 | 2 | 3 | 2 | **9** |
| **G** | **Sell-by date** | 2 | 2 | 3 | 2 | **9** |
| H | Swap instead of sell | 1 | 1 | 2 | 3 | 7 |

Reasons for the key scores:

- **A:** covers the most pain points, but seven features make it hard to test
  one assumption; platform integrations are unverified.
- **B:** tests the open question "is price information the missing piece?",
  but P0 already checks prices and still doubts. Overlaps with Idea A.
- **C:** directly matches the desk-research workaround and the daylight delay;
  low risk.
- **E:** hits the photo step (the daylight delay and "Ugh, I have to take good
  pics"), and the effort per item. Risk: group photos may not be good enough
  for buyers.
- **F:** makes the pile feel achievable, but does not reduce the effort per
  item, which is where P0's annoyance starts. Risk: guilt from broken streaks.
- **G:** responds to discouragement after unsold listings, but phase 5 is
  outside the current scope. Risk: valuable items donated automatically.
- **H:** does not answer the approved HMW (items listed).

## Decision

**Gate 3, approved by the PM on 2026-10-16: combine E + C, "one photo session
for the whole pile".**

One daylight session for the whole pile: lay items out in groups, take a few
photos, and get a draft listing for each item. The drafts can be finished
later.

Why:

- E was the PM's strongest favourite and responds directly to P0's photo
  thought ("Ugh, I have to take good pics, but it's already dark") and to the
  15+ minutes per item.
- C scored highest and matches the desk-research workaround (one session, no
  "later" pile).
- They overlap: both move from item-by-item to the whole pile at once.

## Rejected Options

| # | Idea | Reason |
|---|---|---|
| A | All-in-one selling app | Seven features make it hard to test one assumption; platform integrations unverified. Parts may return later (AI text, price comparison). |
| B | Worth-it check | P0 already checks prices and still doubts; overlaps with Idea A. Kept as a possible later experiment. |
| D | Hand it over | Hard to prototype and test today; removes the person's control. |
| F | Little-and-often challenge | PM favourite, but doesn't reduce the effort per item, where P0's annoyance starts. |
| G | Sell-by date | PM favourite, but addresses phase 5, outside the current scope. Candidate for a later cycle. |
| H | Swap instead of sell | Doesn't answer the approved HMW. |

## Prototype Plan

**Gate 4, approved by the PM on 2026-10-16, with two PM changes.**

- **Learning question:** Does turning the whole pile into drafts in one photo
  session get a person from "pile" to "drafts ready" without wanting to stop or
  put it off?
- **Secondary question:** Do they believe the drafts are good enough to finish
  and post?
- **Format:** clickable, phone-sized HTML prototype. Photo-taking is simulated;
  no real AI; no price estimate.
- **Flow:** start session → lay out a group → take one photo → check items →
  drafts → session summary. A draft opens with photo, suggested title, and
  fields to complete.
- **Test task:** "Imagine it's Saturday afternoon and you have a pile of clothes
  you've been meaning to sell. Show me how you'd use this to get them ready to
  sell."

**PM changes to Claude's proposal:**

| Change | PM reason | Risk noted by Claude |
|---|---|---|
| Add an editable price field | "As real as possible" | None, as long as no price estimate is shown (that would mix in Idea B). |
| Earthy visual design (lime green, warm brown) instead of grey wireframe | Design matters to the PM | Testers may react to visual polish instead of the flow. Mitigation: observe behaviour, not opinions about the look. |

## Pre-Test Changes (after prototype review)

PM accepted all 7 prototype-reviewer findings on 2026-10-16 and added two
wishes.

| Change | Source |
|---|---|
| Test with real clothes: the tester lays out and photographs a real pile; the facilitator notes the real time. On-screen timer removed. | Reviewer finding 1 |
| Real photo upload; each draft shows its crop from a 3 x 2 grid of that photo. Drawn sample kept only as a labelled demo. | Reviewer finding 2 |
| "List now" replaced by "Mark ready"; counters show "ready to sell". | Reviewer finding 3 (Claude had added "List now" outside the approved plan) |
| Camera and draft titles are headings, so focus lands correctly. | Reviewer finding 4 |
| Price placeholder "Your price" (no number); commas accepted. | Reviewer finding 5 |
| Daylight tip made general; no fixed time. | Reviewer finding 6 |
| Item chips announce "included" or "left out". | Reviewer finding 7 |
| Start screen explains the idea in three steps. | PM wish |
| Each draft has a "Where do you want to sell it?" choice: Vinted or Kleinanzeigen. Nothing is posted. | PM wish; compromise with finding 3 to stay within the "drafts ready" scope |

Note: naming the platforms moves slightly toward Idea A. The choice is
recorded only; there is no cross-posting.

## Further PM Changes (2026-10-16)

| Change | PM reason | Note by Claude |
|---|---|---|
| Platform choice is multi-select: Vinted, Kleinanzeigen, or both. | PM wish | Moves closer to Idea A's cross-posting. Only the choice is recorded; nothing is posted. |
| Item recognition ("Black skirt", "Red shirt"), built as **Wizard of Oz**: the facilitator types the names on a facilitator-only screen; the tester sees "Recognising..." and then the names. | PM chose option 1 of 3 (Wizard of Oz, real AI, colour only) | Moves closer to Idea A's AI features. Tests whether recognition makes the pile feel like less work before building real AI. **Test notes must state that recognition was simulated.** |

## Shared Link (2026-10-16)

Published at https://claude.ai/artifact/7VXfAoLPAW4uWEn1V8rcNx (private until
the PM shares it).

- The shared link has **no facilitator**: the demo photo is shown as
  "recognised"; real photos get blank titles that the tester fills in.
- Facilitator mode (Wizard of Oz) runs only when the local file is opened.
- Added light and dark themes for the shared page.
- Remote testers cannot be observed, so their feedback is mostly opinion.
  Observed sessions remain the stronger evidence.

