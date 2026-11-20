# Plandit usability synthesis

**Team:** Black Panthers  
**Sessions run:** 3 on November 6, 2026  
**Strangers among them:** 1 (P3)  
**Participants who reached the aha moment:** Not recorded. All three attempted the core flow, but the
available notes do not identify each participant's first successful activation moment.

**Aha moment:** The user sees a day plan built from places they wanted to visit and understands that
it fits their budget and travel constraints.

**Sessions:** [P1](sessions/session_1.md), [P2](sessions/session_2.md),
[P3](sessions/session_3.md)

## Patterns across sessions

| Pattern | Sessions | Count |
|---|---|---:|
| Budget was unclear or the participant tried to edit a stop's cost | P1, P3 | 2 |
| Adding a place was difficult or broken | P1, P2 | 2 |
| The participant lost context in the plan or route | P1, P2 | 2 |
| The participant reacted positively to sharing | P2, P3 | 2 |
| Share flow was too complex or lacked actionable links | P3 | 1 |
| Wanted collaborative plans | P3 | 1 |

## What surprised us

- The step that supplies the planner with places was the largest activation blocker. P1 could not
  find a working add action, and P2 needed 17 clicks to add one place.
- Sharing was one of the strongest value signals. P3 said they would most likely use Plandit to send
  plans to friends, while P2 also reacted positively to the share option.
- The budget is a core promise, but two participants treated it as a number they could not
  understand or control.

## What we're changing and why

### Change 1: Make adding a place one reliable action

> **What we observed:** In two of three sessions, participants struggled to get a place into
> Plandit. P1 could not find how to add a place and pressed blocked or unresponsive controls. P2
> needed 17 clicks because the upload action did not work reliably.
>
> **What we're changing:** Put one prominent **Add place** button on Saved. It accepts a pasted
> Instagram Reel or TikTok link or a place-name search, shows one clear progress state, and either
> saves the place or presents a specific recovery action. Fix the blocked and unresponsive controls.
>
> **Why:** The planner cannot reach its aha moment without places. This repeated failure occurs
> before every valuable downstream action.

### Change 2: Explain and edit the budget at each stop

> **What we observed:** P1 and P3 asked for more budget explanation and tried to change the cost at
> an individual stop.
>
> **What we're changing:** Show each stop's estimated cost and a running total such as "$34 of $50"
> on the plan. Make each stop cost tappable, allow the user to replace the estimate, and update the
> total immediately.
>
> **Why:** Participants could not trust or control a core product input. Per-stop amounts explain how
> the total was calculated and let users correct it.

### Change 3: Keep the finished plan visible and label every transition

> **What we observed:** P1 opened Google Maps by tapping a stop without expecting to leave Plandit.
> P2 could not find the plan after creating it and could not distinguish walking legs from subway
> legs.
>
> **What we're changing:** After **Create plan**, open the finished plan directly. Label each leg
> with walk/subway/drive, time, and distance. Keep stop rows inside Plandit and use a separate,
> clearly labeled **Open in Maps** button for external directions.
>
> **Why:** The finished plan is the activation surface. Users cannot recognize its value if they
> cannot find it, understand movement between stops, or predict when they will leave the app.

### Change 4: Make sharing one tap and make the result actionable

> **What we observed:** P2 liked the share option. P3 said sharing was the primary reason they would
> use Plandit, but called the flow too complex and expected restaurant and ticket links.
>
> **What we're changing:** Add one **Share plan** action on the finished plan that creates a single
> browser-viewable link. The shared view lists stops in order and includes the place website, Maps
> link, and ticket link when available.
>
> **Why:** Sharing was a repeated value signal and can bring new users into the product, but only if
> recipients can act on the plan without extra explanation or an app download.

## What we're not changing yet

- **Collaborative editing:** One participant requested it, but it is a large separate feature.
  First prove that recipients can open and use a simple shared plan.
- **A new recommendation feed:** The repeated blocker was importing places users already wanted,
  not finding unrelated places. Fixing Saved remains aligned with Plandit's planner positioning.
- **Prioritizing only Instagram or TikTok:** P2 preferred Instagram Reels, but the change above
  supports pasted links from both platforms.
- **Purely visual Saved-screen changes:** Watercolor imagery, filtering, and card simplification came
  from a separate design review, not a repeated usability pattern, so they rank below the four
  observed flow fixes.

