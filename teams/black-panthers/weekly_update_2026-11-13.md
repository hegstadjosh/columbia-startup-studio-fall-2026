# Weekly Update: Black Panthers (Plandit), November 13, 2026

#### Accountability: what we did

- **Build:** Added account creation, per-account cloud sync, usage events, direct TikTok and
  Instagram caption extraction, exact-address place matching, route lines, travel modes, and
  editable stop prices. We also fixed an iOS 18 URL bug that prevented sync, events, and account
  deletion. This went beyond our original prototype plan because the real share-to-plan path needed
  working accounts, reliable imports, and navigation before we could test activation.
- **Grow:** We recruited three college-student testers through class, a friend, and a random student.
  We did not run a broader acquisition campaign because the sessions showed that adding a place and
  reading the finished plan still create too much friction.
- **Analyze:** We compared all three sessions and found three repeated blockers: two participants
  struggled to add a place, two could not understand or edit the budget, and two lost their place
  after building or opening a plan. Two participants also reacted positively to sharing.
- **Research:** We ran three usability sessions on November 6, including one session with a
  stranger. Participants attempted sign-up, adding a saved place, building a budget-aware day plan,
  and sharing. The available notes did not record the exact activation moment for each participant.

#### Planning: what we're doing next

- **Build:** First, make adding a place one reliable action from Saved, with paste/search support for
  Instagram and TikTok. Then show editable per-stop costs and a running budget total, land users
  directly on the finished plan with clear walk/subway labels, and make sharing a one-tap link with
  place and ticket links. These changes address the repeated blockers closest to activation.
- **Grow:** Distribute a signed TestFlight build to a small group of college students, then recruit
  at least three new testers after the core flow is fixed. We are delaying wider promotion until a
  new user can save a place and reach a plan without help.
- **Analyze:** Add a simple activation funnel from shared/pasted link to saved place, finished plan,
  and shared plan. This will show which usability fix improves completion rather than only clicks.
- **Research:** Re-run at least three sessions with people who have not seen Plandit, including at
  least one stranger. Record where each person reaches the aha moment and whether the revised
  add-place, budget, route, and share flows work without moderator help.

#### Issues

- Real-device and TestFlight testing require access to the team's paid Apple Developer account
  because Personal Teams cannot sign the current Sign in with Apple and App Group capabilities.
- App Store submission still needs privacy/security hardening and accurate disclosures for cloud
  sync, Apple Maps lookup, and exact public-post caption processing.
- The November 6 notes did not capture recording details or exact aha-moment timing, so the next
  sessions need a stricter note-taking checklist.

