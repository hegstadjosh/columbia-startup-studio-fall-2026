# Weekly Update: AIDI (Aplovia), November 13, 2026

## Accountability: what we did

- **Build:** Took Aplovia from a pre-launch product to a live service at
  [aplovia.app](https://aplovia.app). We purchased and configured the domain,
  enabled HTTPS and DNSSEC, set up the `www` redirect, and moved the backend and
  database onto paid Render services so the product and its data will not expire
  or sleep like the earlier free instances. We also created
  `support@aplovia.app` through Zoho Mail, configured Resend for transactional
  messages, and verified the MX, SPF, DKIM, and DMARC records needed for reliable
  account-verification and recovery emails. Before launch, we created a production
  database backup, separated database migrations from the server start command,
  published four effective policy documents, added consent-controlled analytics,
  and completed end-to-end checks across English, Chinese, desktop, and iPad
  experiences. We published 36 institutions that passed final review; more than 30
  additional institutions remain in review or have missing data. We had planned to
  begin the application-material checklist and reach 100 colleges, but prioritized
  production reliability, privacy, policy readiness, and the usability fixes found
  last week because those were prerequisites for a responsible launch.
- **Grow:** Opened the product for real account registration and invited the users
  who had previously committed to trying the launch version. Three users have
  registered so far. We also published on both Chinese and international social
  platforms. The posts covered the core problem, product functions, version
  updates, and our next steps. We used two complementary voices: official team
  updates and softer user-perspective content designed to communicate how the
  product feels in practice. In China, we established contact with four college
  admissions counselors who agreed to participate in future product testing and
  help introduce the product to relevant student audiences. We did not run a large
  acquisition campaign because the full production version became available only
  at the end of the week.
- **Analyze:** Verified the production system rather than drawing conclusions from
  a very small first group of users. We checked registration, email verification,
  sessions, password recovery, saved preferences, filters, college lists, account
  settings, policy versions, and data publication on the live domain. We also
  confirmed that Google Analytics loads only after a user accepts analytics
  cookies. This gives us a trustworthy measurement foundation, but three early
  registrations are not enough to make claims about conversion or retention yet.
- **Research:** Did not complete another formal user-research round before this
  update. Instead, we translated last week's findings into changes to navigation,
  saved-preference guidance, protected-feature explanations, bilingual policy
  pages, and college-list interactions, then checked those changes in production.
  A new test of the live version is scheduled for tonight. Keeping this separate
  from completed research avoids treating internal launch QA as new user evidence.

## Planning: what we're doing next

- **Build:** First fix the post-launch issues already recorded during production
  review. The homepage and landing pages still describe the old waitlist phase and
  need to be redesigned around the live product. We will also add the missing
  favicon and `robots.txt`, make policy-version records read-only in the admin, and
  address the remaining API-schema warnings. After those fixes, we will review and
  complete the next batch of institution data. If time remains, we will improve My
  College List so it more clearly surfaces required application materials,
  application rounds, and deadlines. A later extension may let students prepare
  and save essays, activities, and other application materials in Aplovia, but that
  feature requires a separate privacy and data-security design before development.
- **Grow:** Follow up with the invited launch users and the four admissions
  counselors, then continue coordinated posting across Chinese and international
  channels. We will track official product posts and user-perspective posts
  separately so we can learn which message and channel produce registrations and
  meaningful product use rather than only views.
- **Analyze:** Build a launch funnel from visit to account creation, email
  verification, saved preferences, and the first college added to My College List.
  We will compare performance by channel and content type and examine where users
  leave before reaching the product's core value. This is more useful than
  optimizing for traffic alone.
- **Research:** Test the production version with target users, beginning tonight,
  and observe whether they can register, save their background and preferences,
  apply filters, inspect source-backed college information, and use My College List
  without assistance. We will prioritize interaction problems found in those
  sessions before adding broader application-planning features.

## Issues

- The public homepage and landing pages still use waitlist-era positioning even
  though account registration is now open.
- Only 36 institutions have passed final review and been published. More than 30
  additional records still require review or missing-data resolution before they
  can be released.
- We have only three early registrations, so there is not yet enough behavior data
  to evaluate activation, retention, or channel effectiveness.
- Reliable access for users in mainland China and the availability of required
  third-party services still need continued testing.
