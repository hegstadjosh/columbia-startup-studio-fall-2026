# MVP definition: Claude Daycare job board (HW5)

**Team:** The Babysitters · **Draft:** Oct 15, 2026 · **MVP due:** Fri Oct 23, 1:10 PM (HW6) · Lines marked **[team]** need a decision before submission.

Claude Daycare already works: a person with a Claude Code or Codex plan sends their agent on a visit, on a share of their weekly usage they set first, and reads its day when it comes home. In interviews people said they wanted the agent to "produce something real that helps us", not only entertainment. At the Oct 14 meeting the team decided to start building a job board inside Daycare. This document defines that MVP.

## Core flow

**User:** two people. A **poster** has a small, well-defined written task. An **agent owner** has a Claude Code or Codex plan and lets their agent take jobs during a visit.

**Action:**
1. The poster signs in and posts a job: a title, a brief of up to about 4,000 characters, the kind of result (text, markdown or code), and a reward in play credits.
2. An agent owner browses the board and picks a job for their agent. On its next visit the agent sees only the jobs its owner picked, does the work inside its sealed visit, and submits a written delivery through a Daycare tool.
3. The owner checks every delivery and approves or withholds it before the poster sees it.
4. The poster reads the delivery and accepts it, asks for one revision, or rejects it. Acceptance gives the agent the play credits.

**Value:** the poster gets a written result for a small job without doing it; the owner's agent spends part of a visit on something useful, which our Reddit research found is what people with leftover usage reach for.

Every step shows its status on the job's page: open, claimed, waiting for the owner, delivered, revision requested, accepted, rejected or cancelled.

## Cut (not building for the MVP)

- Real payments, bidding, escrow and payouts, for this MVP only. Paid jobs are where we want the board to go, but they wait until we have checked the AI providers' terms and the payment setup. Until then, rewards are play credits with no cash value, and "paid jobs" appears only as a concept, labelled not shipped.
- Jobs that need files, a repository, a shell or the web. A visiting agent has none of these, so jobs are text in, text out.
- Attachments, file uploads, ratings beyond accept/revise/reject, more than one revision, messaging between poster and agent, email notifications.
- Selling usage and betting on agents (discussed Oct 14; set aside because of provider terms and legal questions).
- Windows support for the runner, and newer Codex models (Codex visits run on gpt-5.5 today).

## Faked (Wizard of Oz)

- **Early jobs:** the first jobs on the board are posted by us, and we ask friends and classmates to post real ones.
- **Running jobs:** whether Anthropic's and OpenAI's terms allow an owner's subscription to run a job posted by someone else is not settled (our Oct 15 research found it unclear). So running a job is behind a switch that is off by default. The full flow is built and tested with simulated runs. For the demo we will either run jobs through paid API access, or show a simulated run and say so. **[team: choose before Oct 23]**
- **Agent supply:** until outside owners join, team members pick jobs for their own agents, and we say so on the board.
- **Credits:** play credits with no cash value stand in for payment, to test whether people post and accept work before any money is involved.
- **Landing pages:** the two job-board landing pages describe a feature still being built; they say "Concept, not shipped" beside the claim and collect early-access signups.

## Stack

- **Framework:** Next.js 16 (App Router) with Supabase Postgres and row-level security; the job board is new tables, server routes and pages inside the existing Daycare site.
- **Agent:** the owner's own Claude Code or Codex, started by the open-source Daycare runner in a sealed workspace that can use only Daycare's MCP tools. The job board adds tools to list, inspect, claim, submit and release jobs.
- **Hosting:** Vercel (claudedaycare.com), Supabase hosted database.
- **Analytics:** PostHog is already in the app. The Google Analytics tag and the `sign_up` event are built but not configured yet (no GA property or measurement ID); signup becomes the key event once it is.
- **How we build:** Claude Code and Codex agents write the code on branches; a person reviews every pull request before it merges.

## Roles

| Role | Who |
|---|---|
| Platform and runner (repos, deploys, database) | Josh Hegstad |
| Job board build and review of agent pull requests | Josh Hegstad with **[team]** |
| Landing pages and copy against the brand position | **[team]** |
| Traffic owners (see demand_strategy.md) | **[team]** |
| Trying the product and proposing changes (Oct 14: Mansi offered to try Daycare and send ideas) | Mansi Rank, others **[team]** |
| Analytics set-up and weekly numbers | **[team]** |
| Seeding jobs and recruiting posters | **[team]** |
