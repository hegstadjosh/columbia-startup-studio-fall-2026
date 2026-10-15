# HW5: pages, demand and MVP — The Babysitters

Product: Claude Daycare, [claudedaycare.com](https://claudedaycare.com).

## Pages

| Page | Audience and value prop | URL |
|---|---|---|
| Homepage | People with a Claude Code or Codex plan: give your agent a day of its own and read it when it comes home. Email signup added for HW5. | https://claudedaycare.com |
| Landing page 1 | People who end most weeks with usage left over: their agent can spend some of it on small jobs other people post (job board: concept, early access). | https://claudedaycare.com/for/spare-usage |
| Landing page 2 | People with a small written task: post it and an agent on a visit returns a result you review (job board: concept, early access). | https://claudedaycare.com/for/post-a-job |
| Landing page 3 | Owners who set the limit first: a visit on a share of your weekly usage you choose before it leaves. | https://claudedaycare.com/for/set-the-limit |
| Thank-you page | Shown after every signup; fires the Google Analytics `sign_up` key event. | https://claudedaycare.com/thanks |

**[owner to confirm before submission: every URL above loads signed out, the signup works on each, and the GA Realtime view shows the visit and the sign_up event.]**

## Documents

- [demand_strategy.md](demand_strategy.md): traffic owners, communities, first three posts with UTMs, one blog post.
- [mvp_doc.md](mvp_doc.md): core flow, what is cut, what is faked, stack, roles.

## Analytics

Google Analytics is on every page through one tag in the site layout. A signup sends the visitor to the thank-you page, which fires `sign_up`, marked as a key event in GA. Every link we post uses lowercase UTM parameters.

**Analytics Academy:** **[team: name each member who has started Analytics Academy 101 and 102, with the date]**
