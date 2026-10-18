# DevMentor — product brief

- Date: 2026-10-18
- Mode: own; Owner: founder A (decider, workshop 2026-08-26); Pass: full (one interview round, skeptic read)
- Evidence basis: 7 interviews (4 developers who get stuck, 3 senior engineers who answer questions), one 14-day Discord export (109 help threads), one 54-response survey on the same Discord, two founder-run documents (workshop, board exports), five benchmark checks dated 2026-09-04. All interviewees came through the founders' networks and invitation list; the Discord export and survey come from one community. Most consequential untested belief: that developers who say they would pay for a fast text answer will pay (A01); 3 of 54 survey respondents ever paid anyone.
- Coverage: 47 claims — 42 sourced (interview 16, data 5, document 15, product 1, benchmark 5), 0 synthetic, 5 assumed; 1 entries on the collection plan
- Synthetic hypotheses outside Coverage: 0
- Definition of Ready signed by: not yet signed — founder A decided scope and the stop line; the test group, launch date, how a mentee reaches a mentor, mentor price and terms are open (Q01, Q02, Q04, Q05, Q06); ready for: a named experiment, not implementation planning
- Sources: `.ai/specs/research/` (interviews 2026-08-20 to 2026-09-03; `2026-08-26-workshop-export.md`; `2026-09-04-discord-help-requests.csv`; `2026-09-04-survey-discord-willingness-to-pay.md`; `2026-09-04-benchmark-*.md`; Miro exports 2026-09-02 to 2026-09-05; `decisions/`), `.ai/specs/implemented/2026-09-01-devmentor-monorepo-bootstrap.md`

## Decision summary

Founder A decided the first version is a paid 25 or 50-minute text session between a developer with a specific blocker and a senior engineer who has solved it (D01), with the vault, subscription and MCP access deferred. The decision is made; its basis is partly evidence and partly a bet.

Developers describe being stuck on a deadline with nobody to ask, and the Discord export shows the community often fails them: 21% of threads got no reply and the median wait for a first reply was 67 minutes (see Problems). Three of four developer interviewees wanted an answer within the hour or the same day, and for a bug three accepted text (the freelancer wants a call for estimates). Two of three senior engineers would consider answering in text if they see the question first (Problems, Target group).

The biggest uncertainty is a mismatch: the need is speed (20 minutes to a day, one blocker arose on a Friday evening), but Now is a bookable 25/50-minute slot, and nothing says when invited mentors can answer (A03). The stop line (D02) measures a booking, not speed, and "paid session" can be met by one booking. Willingness to pay is stated (69% in the survey), not observed (3 of 54 ever paid).

Next: before building, founder A defines the test group, the launch date and how a mentee reaches a mentor (Q01, Q02, Q04); the founders collect mentor rate and answering hours from the first invitees (Q05, collection plan); someone takes the terms of service (Q06).

## Vision

For developers stuck on a specific blocker and seniors who answer such questions for free: an answer from someone who has done it, and income for the senior. The founders' board states it as turning private conversations into paid, mentor-owned knowledge; that is the team's direction, and the knowledge part is deferred by D01. `[DOCUMENT]` `2026-09-02-miro-board-vision-target-needs.md`

## Target group and stakeholders

- Customer (pays): a working developer; of 4 developer interviewees, the freelancer would pay from their own pocket (below 200, the currency was not asked), the fintech backend developer first said the company and ended on "sam bym zapłacił. chyba" (unresolved), the platform developer only if the employer pays, and the working developer said "I'd pay for speed, not for a subscription" (who pays was not asked). `[INTERVIEW]` 2026-08-20, 2026-09-01, 2026-09-02 (freelancer), 2026-09-02 (platform dev)
- Customer (pays), survey: 24 of 54 would pay out of their own pocket, 19 would ask their employer (13 asking, 6 without asking), 2 their client, 9 nobody. `[DATA]` `2026-09-04-survey-discord-willingness-to-pay.md`, one Discord, 2026-08-29 to 2026-09-03
- User (uses): a developer with a concrete blocker and no senior at hand, as in three interviews (working developer, fintech backend, freelancer); the platform developer works at a 200-person company with an internal channel and would not pay. `[INTERVIEW]` 2026-08-20, 2026-09-01, 2026-09-02 (freelancer), 2026-09-02 (platform dev)
- User (answers): a senior engineer who already answers the same questions unpaid (3 interviews); the staff engineer declined monthly mentoring ("nie chcę relacji"), the others were not asked. `[INTERVIEW]` 2026-08-22, 2026-09-03 (Python), 2026-09-03 (staff engineer)
- Stakeholders: founder A (sponsor, product owner, UX/UI), founder B (tech lead, project manager, developers); Stripe for payments; QA and legal have no person behind them yet. `[DOCUMENT]` `2026-09-05-miro-board-raci-matrix.md`
- Decider for scope decisions: founder A. `[DOCUMENT]` `2026-08-26-workshop-export.md`

## Problems, with evidence

- A developer stuck on a release-critical error found no timely answer: an hour of search, a Discord answer on Saturday that was wrong, rollback, release slipped from Monday to Tuesday. One account. `[INTERVIEW]` 2026-09-01
- A freelancer sent a migration estimate that was too low after two evenings of reading and a Discord reply of "it depends", losing about a week of unpaid time. One account. `[INTERVIEW]` 2026-09-02 (freelancer)
- A developer lost half a day to a TypeScript error the day before a release, with two contradictory answers from a Discord and a workaround shipped. One account. `[INTERVIEW]` 2026-08-20
- Counter-case: a platform developer solved a half-day blocker alone and would pay only for a once-only, day-long task, found within five minutes, answered within an hour, and paid by the employer. One account. `[INTERVIEW]` 2026-09-02 (platform dev)
- Prior paid help: the fintech developer paid Codementor once about two years ago (40 minutes to find someone, then a call whose microphone failed); the working developer bought a course; the freelancer and the platform developer had paid for no help. Four accounts. `[INTERVIEW]` 2026-09-01, 2026-08-20, 2026-09-02 (freelancer), 2026-09-02 (platform dev)
- In 14 days, 109 help threads were posted on one developer Discord: 23 (21%) got no human reply; among the 86 answered, the median first reply took 67 minutes; 31 (28%) carried an urgency signal such as "release tomorrow", of which 9 got no reply. `[DATA]` `2026-09-04-discord-help-requests.csv`, #help channels, 2026-08-18 to 2026-08-31, topic and resolution labels assigned by founder B
- Only 35 of the 109 threads (32%) ended with the poster saying it was solved; 20 partially. `[DATA]` `2026-09-04-discord-help-requests.csv`, same period and filter
- In the survey, 30 of 54 were stuck this week or this month; asked what they did the last time (all 54, multiple choice), they searched (49), asked an AI (38), asked a community (31), asked a friend (26), shipped a workaround (20), paid someone (3). `[DATA]` `2026-09-04-survey-discord-willingness-to-pay.md`, one Discord, self-selected
- On the answering side, a mentor answers the same three questions a month for free from a private notes file; a Python speaker answers weekly in DMs from a paste doc; a staff engineer is asked constantly on Slack and answers only interesting ones. `[INTERVIEW]` 2026-08-22, 2026-09-03 (Python), 2026-09-03 (staff engineer)
- The need is a quick answer, not a learning path; the interviewees did not want a subscription (working developer, platform developer), community or mentorship journey (freelancer), or saved answers (fintech and platform developers). That the need is the same for developers beyond these four is not established. `[INTERVIEW]` 2026-08-20, 2026-09-01, 2026-09-02 (freelancer), 2026-09-02 (platform dev)
- Conditions in the account: the fintech developer would pay if a mentor replied within twenty minutes and booking took under five; the freelancer needed it the same day and the price before writing anything; the working developer wanted it "within the hour"; the platform developer, within five minutes of searching and an hour of answer. `[INTERVIEW]` 2026-09-01, 2026-09-02 (freelancer), 2026-08-20, 2026-09-02 (platform dev)

## Product and how it stands out

- What it is: a marketplace where a developer books a paid 25 or 50-minute text session with a senior engineer; details in Scope. `[DOCUMENT]` `decisions/D01-first-version-paid-text-session.md`
- What makes it different: Now has no sourced advantage over Codementor except what the interviews asked for, text first and no ratings; the vault differentiator is deferred. `[ASSUMPTION]` the founders' board claims a gap that nobody sells mentor-owned knowledge (`2026-09-02-miro-board-competitors-benchmark.md`); tested by A01
- What exists in the repository today: a monorepo skeleton with placeholder User and MentorProfile entities; no booking, scheduling or payments. `[PRODUCT]` `.ai/specs/implemented/2026-09-01-devmentor-monorepo-bootstrap.md`, `packages/db/src/entities/`
- Alternatives developers use today: 38 of 54 asked an AI assistant and 31 a community the last time they were stuck; 20 shipped a workaround and 9 gave up on the approach. `[DATA]` `2026-09-04-survey-discord-willingness-to-pay.md`

| reference | what it does well | where it falls short for our users | checked on | link |
|---|---|---|---|---|
| Codementor | request-to-live-session is the whole product; rates $15 to $80 per 15 min on 10 cards `[BENCHMARK]` | nothing kept after a session; all ten cards show 5.0, so ratings carry no information | 2026-09-04 | https://www.codementor.io/react-experts |
| MentorCruise | free intro call before payment; 7,200 mentors `[BENCHMARK]` | monthly commitment; "Starting from $100 /month"; 97% of exit ratings are 5 stars | 2026-09-04 | https://mentorcruise.com/ |
| ADPList | 36,000+ experts, booking in minutes `[BENCHMARK]` | free for mentees, mentor earnings not stated; career help more than code | 2026-09-04 | https://adplist.org/ |
| Topmate | expert's own link and price; 10% commission on own link, 20% on marketplace customers `[BENCHMARK]` | any profession; no way to find an expert by problem | 2026-09-04 | https://topmate.io/pricing |
| Preply | trial then subscribe; free cancellation up to 12 hours before `[BENCHMARK]` | recurring lessons, not one-off; ratings as the trust signal | 2026-09-04 | https://preply.com/en/how-it-works |

## Goals and success criteria

- Business goal: validate with real users that mentors accept requests and mentees pay for text sessions before building the vault; chosen by founder A. `[DOCUMENT]` `decisions/D01-first-version-paid-text-session.md`
- Business goal (deferred): the board's goals (100 mentors with published vaults in year one, 30% of mentees on a vault subscription) depend on the vault and are not tested by D01. `[DOCUMENT]` `2026-09-02-miro-board-product-goals.md`
- User outcome: an answer from someone who has done the same thing within the time the interviewees named (twenty minutes to the same day). `[INTERVIEW]` 2026-09-01, 2026-09-02 (freelancer), 2026-08-20
- Primary metric, baseline today, threshold, date: paid sessions booked by the test group in the two weeks after launch; baseline 0 (nothing is built); stop if none, per D02; no success threshold and no launch date exist (Q02, Q03). `[DOCUMENT]` `decisions/D02-stop-criterion-two-weeks.md`
- What must not get worse: trust of mentees and mentors in what is published, per R02; no ratings, per N02. `[DOCUMENT]` `2026-08-26-workshop-export.md`

## Scope

- **Now:** a proposed experiment, not a complete product: a mentee sends a request with the question to a mentor; the mentor accepts or not; the mentee pays and gets a 25 or 50-minute text session; bounded by R01, R02, N01, N02 and D03. How the mentee reaches the mentor is open (Q04).
- **Later:** vault subscription, MCP access, the 24-hour async tier, AI answers, session notes published to a vault (D01; R02 applies); commission and revenue streams beyond sessions (Q07).
- **Not doing:** see Non-goals.

## Domain glossary

| Term | Meaning | Owned by | Visible to |
|---|---|---|---|
| Session | a paid 25 or 50-minute text exchange between one mentee and one mentor | founder A | mentee, mentor |
| Request | the mentee's question and context, sent before the session; senior engineers asked to see it before accepting `[INTERVIEW]` 2026-09-03 (Python), 2026-09-03 (staff engineer) | pending | the addressed mentor |
| Test group | the mentees whose booking decides D02; membership not yet defined (Q01) | founder A | founders |
| Vault | a mentor's published notes sold as a subscription; deferred | founder A | not applicable in Now |

## Key flows

- Current state: stuck, searches docs and issues, asks a community or an AI or a friend, waits, ships a workaround or rolls back. `[INTERVIEW]` 2026-09-01, 2026-09-02 (freelancer), 2026-08-20
- Future state: a mentee sends a request to a mentor, the mentor sees the question and accepts, the mentee pays, the session runs in text, the mentee has the answer; the order of accept and pay, the lead time and how the mentee finds the mentor are unknown. `[ASSUMPTION]` shaped by D01, R01, N01, A03, Q04

## Business rules

| Id | Rule | Applies to | Source | Status | Review by | Required path to change | Owner | Supersedes |
|---|---|---|---|---|---|---|---|---|
| R01 | Sessions are 25 or 50 minutes ("bookable in a lunch break") | session | `[DOCUMENT]` `2026-08-26-workshop-export.md` | active | unknown | superseding row by founder A | founder A | none |
| R02 | Nothing from a session is published without the mentee's approval ("trust is the product") | session notes, vault | `[DOCUMENT]` `2026-08-26-workshop-export.md` | active | unknown | superseding row by both founders, founder A decides | both founders | none |
| R03 | Price is shown before the mentee writes anything, and payment is taken before the session | booking | `[INTERVIEW]` 2026-09-02 (freelancer), 2026-09-03 (Python); proposed by the agent | proposal | unknown | founder A | pending | none |
| R04 | A mentee whose mentor does not show is refunded the same day, without a ticket | booking | `[INTERVIEW]` 2026-09-02 (freelancer); proposed by the agent | proposal | unknown | founder A | pending | none |

## Non-goals

| Id | We are not building | Why | Owner | Status | Review by | Required path to change | Source | Supersedes |
|---|---|---|---|---|---|---|---|---|
| N01 | video calls | decided 2026-09-03; sessions are text, the product says so on every session screen; the workshop excluded video and a mentee said "text is fine, faster" (2026-08-20); the freelancer wants a call for estimates, a case N01 does not serve | founder A | active | unknown | superseding record by founder A | `[DOCUMENT]` `decisions/N01-no-video.md` | none |
| N02 | ratings or review profiles; each mentor page links to public work instead | decided 2026-09-03; the mentor interviewee said "my GitHub is my profile", ratings were the least chosen trust signal in the survey (12 of 54), and every mentor page carries a link to public work and a plain description | founder A | active | unknown | superseding record by founder A | `[DOCUMENT]` `decisions/N02-no-ratings.md` | none |

## Decisions

| Id | Date | Decision | Why | Owner | Status | Review by | Required path to change | Source | Supersedes |
|---|---|---|---|---|---|---|---|---|---|
| D01 | 2026-10-18 | First version is a paid 25/50-minute text session; vault, subscription, MCP and AI answers are later | quick validation without the vault architecture; options weighed: vault first, both within 25 hours; agent recommendation accepted | founder A | active | when D02 is decided | superseding record by founder A | `[DOCUMENT]` `decisions/D01-first-version-paid-text-session.md` | none |
| D02 | 2026-10-18 | The test fails if, within 2 weeks of launch, no mentor accepts a request or the test group books no paid session despite declared interest | stop line set by founder A | founder A | active | at the first result or when Q01 and Q02 are answered | superseding record by founder A | `[DOCUMENT]` `decisions/D02-stop-criterion-two-weeks.md` | none |
| D03 | 2026-08-26 | The MVP is limited to 25 hours of build time and Stripe as the only payments provider; no video | workshop constraints | founder A | active | unknown | superseding row by founder A | `[DOCUMENT]` `2026-08-26-workshop-export.md` | none |

## Riskiest assumptions

| Id | Assumption | Importance | Evidence today | If false | Smallest test | Owner | By when | Result |
|---|---|---|---|---|---|---|---|---|
| A01 | Developers who say they would pay for a fast text answer will pay for a booked session `[ASSUMPTION]` origin: the survey's 37 of 54 and interviews | high | stated: 37 of 54 would pay something, 23 would pay 25 EUR or more; observed: 3 of 54 ever paid; price was a shrug in one interview | the demand side of the marketplace is not there; Now stops (D02) | publish a priced offer to the test group; count paid bookings, separately from stated interest | founder A | 2 weeks from launch (launch date unknown) | untested |
| A02 | Senior engineers who said "maybe" or "why not" will accept requests at a price mentees pay `[ASSUMPTION]` origin: two conditional interview answers | high | the Python speaker ("no w sumie czemu nie") and the staff engineer ("to bym może zrobiła") answered with conditions (setup under twenty minutes, see the question first, a high price they set, a link to share rather than a list); the first mentor was not asked about paid text sessions; the list is marked "not contacted" for all 50 although two listed people were interviewed, so it most likely means not invited | no supply; Now stops (D02) | invite the first batch of 20 from the warm contacts; count acceptances of real requests | founders | 2 weeks from launch (launch date unknown) | untested |
| A03 | A bookable 25/50-minute slot meets the speed developers asked for `[ASSUMPTION]` origin: no material on lead time | high | developers named twenty minutes, an hour, the same day; the fintech blocker arose on a Friday at 18:00; the staff engineer answers between meetings and not at weekends; no data on when invited mentors can answer | the product needs on-demand answers or a response-time promise instead of a calendar; Now changes | record time from request to answer in the test | pending | with the test | untested |

## Kill criteria

Founder A's stop line is D02: within 2 weeks of launching the test platform, no mentor accepts a request, or the test group books no paid session despite declared interest. It is a stated intention, not an observed result. It does not say what counts as continuing (Q03), who is in the test group (Q01) or when the clock starts (Q02), and it does not test speed (A03).

## Hypotheses to test

None. No synthetic walkthrough was run in this session.

## Open questions

| Id | Question | Blocking | Who can answer | Status |
|---|---|---|---|---|
| Q01 | Who is in the test group, how many, how are they recruited, may founders' own contacts be paying mentees, and how is "declared interest" recorded? | yes: D02 cannot be read without it | founder A | open |
| Q02 | When does the test platform launch (when does the two weeks start)? | yes: D02 has no clock | founder A, founder B | open |
| Q03 | What result counts as continuing, and is a single paid booking enough? | no for building; yes for reading the result | founder A | open |
| Q04 | How does a mentee reach a mentor: a public directory, or links the mentors share? The staff engineer refused a list; the platform developer wanted to find someone within five minutes and the fintech developer wanted booking to take under five. | yes: it shapes the booking flow | founder A | open |
| Q05 | What does a mentor charge and how many hours a month can they give? (collection plan) | yes: price is needed before launch | the invited mentors | open |
| Q06 | Who owns terms of service for both roles and handling pasted production code? The RACI has no one in the legal role; the interviewer's own unasked item was pasting production config to a stranger (the fintech developer said he would paste the yaml). | yes: before real payments | founder A by default | open |
| Q08 | Does the test need the built platform, or could a manual offer (a payment link and a text chat) answer A01 to A03 first? | no | founder A | open |
| Q07 | Pricing per mentor or per platform, and the commission (the board mentions 15 to 20%; Topmate shows 10% and 20%)? | no | founder A | open |

## Definition of Ready addendum (own)

Problems and Target group have support from interviews and one Discord export (four developer accounts, one of which is a counter-case; the data comes from one community). That support does not show frequency beyond this community, or willingness to pay. Founder A decided Now (D01) and the stop line (D02); A01, A02 and A03 are untested and no one has accepted them as risks. The brief is ready for a named experiment: a priced text-session offer to a defined test group. It is not ready for implementation planning until Q01, Q02, Q04, Q05 and Q06 are answered.

## Collection plan

### What do mentors charge, on which days and hours can they answer, how many hours a month will they give, and does their employer allow it?

- What decision or work needs it: the price shown to mentees (R03), the supply side of A02 and the launch (Q05)
- Who can answer it: the senior engineers on the invitation list, starting with those a founder knows personally
- How: a short interview with each of the first invitees, using the interview note template
- Owner and by when: unknown
- Template: `.ai/specs/research/templates/interview-note.md`
