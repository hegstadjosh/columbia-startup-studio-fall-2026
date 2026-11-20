# SettleWise: Experiment Card ($100 Meta test)

**Locked:** Nov 19, 2026 (committed before publishing) · **Owner:** Sami · Sections 1 to 8 are not edited after launch.

## 1. Question

Should we keep sending paid and outreach traffic to our current homepage, or fix the page before we spend more on traffic?

## 2. Hypothesis

At least 8% of NYC-area adults (Meta Housing audience) who click an ad promising "Find apartments anywhere. Compare them here." will create a SettleWise account (`sign_up` event).

## 3. The one variable

- **What we're testing:** the current homepage and its promise, "Find apartments anywhere. Compare them here.", shown to NYC renters.
- **Everything we hold fixed:** homepage (no edits during the test), Google sign-in flow, one audience, one ad and image, $100 lifetime budget, 7 days, placements.

## 4. Audience

- **Platform and targeting:** Meta (Facebook + Instagram), declared under Meta's **Special Ad Category: Housing** (required for rental-related ads). That fixes the audience at ages 18–65+, all genders, a radius of at least 15 miles around New York, NY, and no detailed interest targeting.
- **Why this audience:** our users are people mid-search for an NYC apartment. We can't target renters directly under the Housing rules, so the promise in the ad does the filtering: people who click are self-selected apartment hunters. 16 real signups as of Nov 18 (`/api/metrics`, team and test accounts excluded) came mostly from people we know; this tests strangers.

## 5. Setup

- **Platform:** Meta
- **The question this platform can answer:** do visitors sign up?
- **Campaign objective:** Traffic, Special Ad Category Housing, optimized for link clicks. Campaign `jims_settlewise_nov2026`, ad set `nyc_housing_broad`, ad `compare_here` (one image, primary text and headline repeat the homepage hero, button "See details").
- **Meta Pixel** (`29522313900803573`) is installed **for reporting only** (PageView, Lead, CompleteRegistration, ViewContent, AnalysisRequested; no personal data). It does not change optimization. Meta's numbers are a cross-check; the decision uses GA4.
- **Budget:** $100 as a lifetime budget
- **Start date:** Thu Nov 19, 2026, 2:52 PM ET (or on approval, if later) **End date:** Thu Nov 26, 2026, 2:52 PM ET (7 days)
- **What counts as a signup:** the GA4 `sign_up` event (fires once, when Google sign-in creates a new SettleWise account).
- **Where we read signups from:** GA4, Session campaign = `jims_settlewise_nov2026`. Cross-checked with `/api/metrics` (signups before vs. after).
- **Ad link:** `https://settlewise.group/?utm_source=meta&utm_medium=paid_social&utm_campaign=jims_settlewise_nov2026&utm_content=compare_here`
- **Placement tag** (Meta URL parameter, appended on click): `utm_term={{site_source_name}}_{{placement}}`, e.g. `ig_Instagram_Stories`. Lets GA split visitors by Facebook/Instagram and placement. It doesn't change delivery and isn't part of the pass/fail.
- **Tracking check:** we signed up with a fresh Google account through a UTM link and saw `sign_up` arrive in GA4 Realtime on Nov 18. Yes → `ad_tracking_proof.jpg`. A second test signup on Nov 18 also showed all five Pixel events in Meta Events Manager.
- **Expected clicks:** Ads Manager showed no click estimate for this Housing campaign (audience 15.4–18.2M). We planned for ~166 (class median, ~$0.60 a click); the bar below has rows for fewer clicks.

## 6. The bar

Floor 2% (the page isn't working) vs. good 8% (it is). Each wrong call held to about 5%.

- We read the result once, after the end date.
- **PASS** if signups are **8 or more** (at ~166 clicks).
- **FAIL** if signups are **7 or fewer** (at ~166 clicks).
- **If clicks come in lower:** 100 clicks → PASS 6+, FAIL 3 or fewer, UNCLEAR 4–5. 140 clicks → PASS 7+, FAIL 5 or fewer, UNCLEAR 6.
- **Our prediction:** 5 signups (Sami), which would be a FAIL against the bar.

## 7. What we'll do

- **If PASS:** run a costlier second test (the AI-vs-priorities choice page, or ask signups to book a 10-minute call), and email every new signup to ask what made them sign up.
- **If FAIL:** low click rate (under ~1% CTR) means the hook or audience is off: change the ad's promise or audience. Clicks but no signups means the page is off: fix the hero and the Google sign-in step before spending more. Change one, not both.
- **If UNCLEAR:** spend no more on ads; decide from interviews and usability tests.
- **Diagnosis for any result:** GA4 funnel exploration filtered to campaign `jims_settlewise_nov2026`: landing `page_view` → `signup_started` → `/signup` view → `sign_up` → `comparison_viewed`, counted in users, not events. The biggest drop tells us which step to fix.

## 8. Stop rules

Only: tracking broken (a test signup doesn't reach GA4), ad disapproved, or spend over $100. Nothing else.

## 9. Result

Fill in after the end date.

- **Impressions:** ___ **Clicks:** ___ **Click rate:** ___%
- **Signups:** ___ **Signup rate:** ___% (range: ___% to ___%)
- **Spend:** $___ **Cost per signup:** $___
- **Call:** PASS / FAIL / UNCLEAR
- **Did we do what section 7 said?**
- **Screenshot:** GA4 Traffic acquisition filtered to the campaign UTM.
