# Weekly Update: AIDI (Aplovia), November 20, 2026

## Accountability: what we did

- **Build:** Expanded the production catalog from 36 to 100 published
  institutions by completing review and release of 64 additional schools. We
  also filled the remaining Cost of Attendance gaps in the original batch and
  normalized the 2027 ranking metadata before the final production release.
  After discovering that Google Analytics had stopped receiving events after
  November 14, we repaired event collection after analytics consent, prevented
  analytics from running on sensitive account paths, and exposed a public
  metrics endpoint for consistent reporting of registrations, verified
  accounts, production waitlist contacts, and page views. This differed from
  last week's plan: we completed the planned institution-data release, but
  deferred the homepage redesign, My College List application-planning work,
  `robots.txt`, read-only PolicyVersion administration, and OpenAPI warning
  cleanup. We prioritized reviewed data and trustworthy production measurement
  because both were prerequisites for evaluating and improving the live
  product.
- **Grow:** Published multiple posts across three RedNote accounts. This gave us
  more opportunities to present Aplovia and reach relevant students, although
  we do not yet have reliable attribution from individual posts to
  registrations. As of November 20, Aplovia has 13 registered accounts, up from
  3 last week, and 11 of those accounts have verified their email addresses.
  The 17 people reported before launch remain a separately maintained group of
  pre-launch waitlist contacts or committed testers; the production database
  currently contains 3 waitlist contacts, so these figures should not be
  interpreted as a decline from 17 to 3. We did not complete the planned
  follow-up with invited launch users and the four admissions counselors.
- **Analyze:** Diagnosed the post-launch analytics interruption and restored
  GA4 collection. We then verified that a server-side, read-only GA4 query could
  report page views through the public metrics endpoint; the November 20
  snapshot showed 2,473 page views. The events missed during the interruption
  cannot be reconstructed, so the period after November 14 contains a known
  measurement gap. We also completed several access tests with users in
  mainland China and confirmed that they can reach the production website. We
  did not build the launch funnel planned last week because restoring a reliable
  analytics foundation had to come first.
- **Research:** Did not conduct another formal user-research round this week.
  The team concentrated on the 100-school data release, analytics repair, and
  production verification. This means the live-product usability testing
  planned in the previous update remains outstanding rather than being treated
  as completed through internal QA.

## Planning: what we're doing next

- **Build:** First redesign the homepage and landing pages so they describe the
  live product and open registration instead of the old waitlist phase. In
  parallel, advance My College List into Application Planning by making
  application materials, application rounds, and deadlines clearer and more
  actionable. These two changes address the largest remaining gaps between the
  current product and the experience promised to users. We will also close the
  smaller production-maintenance items carried over from the previous update:
  add `robots.txt`, make PolicyVersion records read-only in Django Admin, and
  clean up the remaining OpenAPI schema warnings.
- **Grow:** Complete the postponed follow-up with invited launch users and the
  four admissions counselors. Continue publishing through the three RedNote
  accounts, testing different topics and clearer calls to register. Direct
  conversations are important for learning why interested users do or do not
  try the product, while the RedNote accounts provide continued reach.
- **Analyze:** Monitor GA4 to confirm that event collection remains stable after
  the repair. Compare the views, interactions, and qualitative feedback across
  the three RedNote accounts and their different post topics. This will give us
  a practical basis for deciding which content to continue without making
  unsupported attribution claims from the current small sample.
- **Research:** Resume the formal live-product usability testing postponed over
  the previous two weeks. Observe whether target users understand the revised
  homepage positioning and can use college filtering and My College List
  without assistance. Use those findings to determine the next Application
  Planning improvements rather than expanding the feature based only on
  internal assumptions.

## Issues

- The homepage and landing pages still contain waitlist-era positioning even
  though account registration is open.
- GA4 has an unrecoverable data gap from the post-November 14 interruption, so
  analysis of this week's traffic must account for incomplete collection.
- With 13 registered accounts, the current sample remains too small for strong
  conclusions about retention or channel effectiveness.
- Several nonblocking production-maintenance tasks remain open, including
  `robots.txt`, read-only PolicyVersion administration, and OpenAPI schema
  warning cleanup.
