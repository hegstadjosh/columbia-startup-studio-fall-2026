# Weekly Update: Plandit, November 13, 2026

## Accountability: what we did

**Build:** We got the app ready for the App Store and submitted it for review.

- Accounts and data: built the sign-up and sign-in flow, connected the app to a Supabase database,
  and set up tracking for sign-ups and active users. Recorded a demo of the Plandit workflow for
  Apple's reviewers. (Abraham)
- Getting around: users can choose walking, subway, or driving between stops, with times from Apple
  Maps and routes drawn on the map. Fixed route lines not showing. Added editing stop times after a
  plan is made. (Eldad)
- Budgeting: each stop has a price estimate users can change, plus their own extra costs and a full
  budget breakdown. (Eldad)
- Video import: reworked the short-form video sharing and extraction flow so we no longer depend on
  a paid API. (Jaden)
- Wrote the Terms of Service page for the website, which the App Store requires. (Eldad)
- This matched our plan.

**Grow:** We set up our channels and prepared our first content.

- Created TikTok, Instagram, and LinkedIn accounts. (Hunter, Catherine)
- Drafted five video ideas; filming starts Friday morning. Reached out to the professor to schedule
  filming. (Hunter, Catherine)
- Set up Meta ads accounts so they are ready when we launch ads. (Hunter, Catherine)
- Contacted the Columbia University PR team about a collaboration. (Hunter, Catherine)
- This matched our plan.

**Analyze:** We have not completed product analysis yet. Tracking for sign-ups and active users is
now live, so we will have data starting this week.

**Research:** We ran three usability sessions and received a separate design review.

- Adding a place was the biggest blocker. One participant's upload button failed and took 17 clicks
  to add a single place. Another could not find how to add a place at all.
- In two of three sessions, participants could not tell how the budget worked and wanted to change
  the cost at a specific stop.
- In two of three sessions, participants got lost: they were sent to Google Maps without expecting
  it, could not find their plan after creating it, or could not tell walking legs from subway legs.
- Sharing is what excited people most, but one participant found the share flow too complex and
  wanted links to restaurants and tickets in the shared plan.
- The design review recommended a tutorial for new users, a Home tab with selected lists instead of
  an empty map, and simplifying the Saved tab.
- Full findings are in `hw7-usability-testing/usability_synthesis.md`.

## Planning: what we're doing next

**Build:**

- Fix anything Apple flags in the App Store review. (Jaden, Eldad) This is the gate to getting real
  users onto the app.
- Polish the UI based on usability feedback. (Jaden) Start with one reliable Add Place action, then
  clarify per-stop budget editing, keep users on the finished plan with labeled travel legs, and
  reduce sharing to one actionable link.
- Improve how short-form videos are stored in the database. (Abraham) This supports adding places
  from Reels and TikTok, where participants struggled most.
- Refine the UI of sign-up and sign-in. (Abraham)
- Polish the map. (Eldad) Participants could not tell walking from subway legs.
- Build contributions and inviting friends. (Eldad) Sharing with friends is the main way
  participants said they would use Plandit.

**Grow:**

- Finish filming, edit, and upload the first batch of videos. (Hunter, Catherine)
- Print and put up Plandit posters around campus with QR codes to the website. (Hunter, Catherine)
- Post about Plandit on Reddit. (Hunter, Catherine)
- Why: Videos, posters, and Reddit get Plandit in front of students who have not heard of it.
  Because Plandit is built for planning and sharing days out with friends, each new user has a
  reason to bring others in, so early visibility should turn into word of mouth.

**Analyze:**

- Review the first video analytics to see which platform and which videos bring people to the
  website. (Hunter, Catherine) This tells us where to focus our time and ad spend.
- Use the new sign-up and active-user tracking to measure the funnel from account creation to first
  saved place and first completed plan. This shows whether the add-place and navigation changes
  improve activation.

**Research:**

- Run at least three more usability sessions after the add-place and navigation fixes ship,
  including at least one stranger. Record whether each participant reaches a finished plan without
  help and the exact moment they understand Plandit's value.

## Issues

- The App Store review is still pending. We cannot get users onto the app until Apple approves it,
  and we need to fix any flags quickly.

## Key Metrics

- Sign-ups and active users: tracking is live as of this week; no reporting period has completed
  yet.
- Usability: three sessions completed. The available notes did not record a reliable aha-moment
  count.

## Decisions Needed / Action Items

- Jaden, Eldad: Fix App Store review flags (Due: Friday, November 20).
- Hunter, Catherine: Upload first batch of videos (Due: Friday, November 20).
- Hunter, Catherine: Put up QR code posters and post on Reddit (Due: Friday, November 20).
- Decision needed: Should contributions and inviting friends come before simplifying the share
  flow? Only one of three usability participants asked for collaboration.
