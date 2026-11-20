# Usability synthesis: Gable

**Sessions run:** 3 (Nov 6, [Nov ?], Nov 11), on the staging MVP, over Zoom, 3 different Columbia-area testers.
**Participants who reached the aha moment (a short list of sublets that fit what they asked for):** 3 of 3.
Notes for each session are in `sessions/`.

## Patterns across sessions

| Pattern | Sessions |
|---|---|
| Tried "Sign in" before creating an account | 3 of 3 |
| Said there aren't enough listings, or wanted more options | 3 of 3 |
| Missed the chat search at first (scrolled or filtered by eye) | 2 of 3 (the third typed into it at once and loved it) |
| Messages unclear: "looks like WhatsApp", who am I messaging? | 2 of 3 (session 1 didn't reach Messages) |
| Travel-time lines on cards confused them ("Columbus Circle", "20 min to Times Square") | 2 of 3 |

## What surprised us

- The chat search is the aha moment, and it worked every time someone used it ("wowwwww this is great!!!!", "Saves me going through everything"). The problem isn't the search. It's that people don't always see it.
- Nobody got stuck on the actual search or saving a place. The friction is around the edges: sign-up, labels and Messages.
- Session 1's tester didn't realize the listings come from Columbia students, even though that's our main trust promise.

## What we're changing and why

> **What we observed:** All 3 testers clicked "Sign in" first and got an error or a pause before finding sign-up. Session 1's login "didn't work" until she realized she had no account. Session 2's login was "wrong." Session 3 said "Oh, wait, I don't have an account yet."
>
> **What we're changing:** In the header and on the sign-in page, make "Sign up" the filled primary button and "Log in" a plain text link. When a login fails because the email has no account, show "No account with that email. Create one" with a link to sign up, instead of a generic error.
>
> **Why:** It cost every tester time on the first thing they tried, before they reached the product.

> **What we observed:** 2 of 3 testers didn't use the chat search at first. One scrolled the listings before noticing it, and one filtered by eye and never used the chat on the left. The tester who typed into it right away reached the aha moment fastest.
>
> **What we're changing:** Put the "Tell us what you want" box at the top of the results page, above the listings, with an example in the box ("Try: June to August, under $1,600") so people see what to type.
>
> **Why:** The chat search is our aha moment, and 2 of 3 people only found it by accident.

> **What we observed:** All 3 testers said there weren't enough listings. Session 1: "expected to see more options." Session 2: "the selection was very limited." Session 3: "I'd want a few more places to choose from."
>
> **What we're changing:** When a search finds nothing that fits, show a "We don't have that one yet" form that takes their email and what they want, and promise to email what we find within 48 hours. We look for matches by hand from our network and from students who use List your room. (Built on the `no-results-request` branch of our Gable repo.)
>
> **Why:** Nobody left because the product was bad. They said it was good but empty. A request form turns an empty search into a lead we can follow up on, and tells us which listings to go find.

> **What we observed:** 2 of 3 testers were confused by Messages. Session 2: it "looks like WhatsApp" and was the most confusing part of the session. Session 3: "Am I messaging the person renting it out?"
>
> **What we're changing:** On every message thread, put the lister's first name and the listing at the top ("Message [first name], about [listing title]") and add one line of text above the empty message box: "This goes to the student who posted this place."
>
> **Why:** Testers couldn't tell who was on the other end, which is exactly the trust question Gable exists to answer.

> **What we observed:** 2 of 3 testers were confused by the travel-time lines on listing cards. Session 3 asked "Why does this say Columbus Circle? Is that how far away it is?" Session 1 didn't understand "20 min to Times Square," "15 min to Columbus Circle" or "Replies in ~3h."
>
> **What we're changing:** Replace the two or three travel lines with one: "X min to Columbia by subway." Remove the "Replies in ~3h" line until we have real reply times.
>
> **Why:** Our testers are mostly Columbia students and expect distance to campus. Other landmarks read as noise.

> **What we observed:** Session 1's tester clicked "Summer" in the header and ended up on a landing page instead of searching, and she didn't realize the listings come from Columbia students.
>
> **What we're changing:** Keep the search flow's header to Explore, Favorites, List your room and Messages, with no links out to marketing pages (the old `/summer`, `/verified` and `/together` pages now redirect home). Add "Listed by a Columbia student" to every listing card.
>
> **Why:** The header pulled a tester out of the product, and the trust promise only works if people can see it on the card.

## What we're not changing (yet)

- **The map:** Sessions 1 and 3 opened it briefly and went back to the listing list to compare; Session 2 left it quickly. Nobody got stuck on it, and Session 1 liked it, so it stays.
- **The overall look:** Testers called it "clean," "very aesthetically pleasing" and compared it to Airbnb. No changes.
- **Comparing places side by side in Favorites:** nobody asked for it, and they compared in the search results instead.
