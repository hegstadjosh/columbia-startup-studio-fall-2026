# HW5: pages, demand and MVP — The Babysitters

Product: Claude Daycare, [claudedaycare.com](https://claudedaycare.com).

## Pages

| Page | Audience and value prop | URL |
|---|---|---|
| Homepage | People with a Claude Code or Codex plan: give your agent a day of its own and read it when it comes home. Email signup added for HW5. | https://claudedaycare.com |
| Landing page 1 | People who end most weeks with usage left over: their agent can spend some of it on small jobs other people post (job board: concept, early access). | https://claudedaycare.com/for/spare-usage |
| Landing page 2 | People with a small written task: post it and an agent on a visit returns a result you review (job board: concept, early access). | https://claudedaycare.com/for/post-a-job |
| Landing page 3 | Owners who set the limit first: a visit on a share of your weekly usage you choose before it leaves. | https://claudedaycare.com/for/set-the-limit |
| Thank-you page | Shown after every signup; sends the Google Analytics `sign_up` event once GA is configured (see Analytics). | https://claudedaycare.com/thanks |

**Status:** these are the production addresses the pages will have after release. Today they exist only on a password-protected preview, so they are not yet public. **[owner to confirm before submission: every URL above loads signed out and the signup works on each.]**

## Documents

- [demand_strategy.md](demand_strategy.md): traffic owners, communities, first three posts with UTMs, one blog post.
- [mvp_doc.md](mvp_doc.md): core flow, what is cut, what is faked, stack, roles.
- [first_posts.md](first_posts.md): the first three posts, written and ready; not yet posted (receipts go there once posted).

## Analytics

**Built:** one Google Analytics tag in the site layout that loads on every page once a measurement ID is set, and a `sign_up` event sent from the thank-you page once per real signup. Every link we post uses lowercase UTM parameters, and signups store the UTM tags with the address.

**Not yet configured:** there is no Google Analytics property or measurement ID yet, so no page sends data to GA today, and `sign_up` is not yet marked as a key event. **[owner: replace this paragraph with the verification receipt (property, Realtime visit, key event) once configured.]**

**Analytics Academy:** **[team: name each member who has started Analytics Academy 101 and 102, with the date]**
