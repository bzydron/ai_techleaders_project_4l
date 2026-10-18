# Walkthrough: Future state, booking and session (1.0), decided steps — `.ai/specs/product-brief.md`, 2026-10-18

With one run, this panel supports no finding. Everything below is "seen once". The next real check is a short interview round with urgent-blocker developers, testing whether the two-hour minimum start (R03) makes help arrive too late (A04). Both personas hit that point, and one of them said it would make the service useless. Every item is synthetic and does not satisfy the Definition of Ready.

Stance: adversary (brief mode `own`, so agreement is the risk)
Panel: 1 run × 2 personas; run 1: P01, P02
Basis: product brief (Target group, Problems, Key flows, Business rules, Non-goals, Scope, Glossary; assumptions A02 and A04 shaped questions only). Persona lines rest on `[INTERVIEW]` notes `2026-08-20-interview-working-dev` and `2026-09-02-interview-platform-dev-solves-alone`. Flow facts rest on `[DOCUMENT]` decisions D07, D09, D21, D22, D27, N01.
Panel snapshot: [personas.md](personas.md)
Session: `.ai/specs/research/walkthroughs/2026-10-18-future-state-booking-and-session-1-0-decided-steps-session-001/`; subject `.ai/specs/product-brief.md`; flow "Future state, booking and session (1.0), decided steps" (exact match to the brief's Key flow heading, no mapping needed)
Composition: assumed. The brief states no segment proportions. Two segments, one persona each, because each segment has one note. Each seat is therefore one voice (one source note), not a panel of independent people.
Saturation: not reached. Of P02's 15 topics, about 11 were not raised by P01.
Parity: 9 of 11 held-out themes also raised by the panel, against `holdout/2026-09-01-interview-backend-dev-fintech.md` (opened only at step 6; built no persona line). Real-only: failure ended in a rollback and slipped release; one earlier paid session that was slow to find and ended on a failed call. Details under Parity below, and in [calibration.md](../../calibration.md).
Elapsed: the two persona subagents ran in parallel for about 30 s (P01) and about 48 s (P02). The other phases were not timed.
Not askable of this panel: none. A02 and A04 are both mentee-side and were put to both personas (Q6, Q7). P02 had no basis for Q7.

## 🎯 Scope and limits

Narrative walk of the five-step Key flow. No screens, no browser, no running app: every "screen" is the brief's sentence for that step. A persona that expected something the sentence did not give recorded a missing case. Not covered: onboarding of mentors, prices, payments, cancellation, payouts, the note after a session (brief Non-goals).

Limits of the method in this run:
- Each persona answered the interview, decisions, walk and topics in one fresh-context call, so the interviewer could not adapt questions. The product text sat in the same prompt as the past-behaviour questions. No Part 1 answer shows product influence.
- My own prompt shaped one topic. In choice C2 the persona was told "if a number would decide your choice, say that the number decides". Both personas then said the price "decides". That price topic is therefore partly induced and should be read that way.
- Quality gate: every critical item passes. Items scored 1: persona independence (one note per segment); P02's answers reuse the source's own Polish quotes word for word, so they add little beyond the profile; parity overlap shares an interview script with the persona notes.
- Acquiescence: of the 7 answered past-behaviour yes/no questions, 2 were "yes" (both P01; Y1 Discord, Y3 shipped a workaround). That is not above one half, and both are supported by the persona's own source passage. Two answers were "no basis" (P01 Y4, P02 Y4) and are the material's gaps. Nothing was excluded.
- Known biases checked: over-positivity is absent (adversary instruction, and P02 declined 3 of 4 choices). No tool or workaround was proposed by both personas. Both personas are developers at product or payments companies, so the panel comes from one corner of the market. Engagement differs strongly between the two, as designed.

## 🔍 Barriers that repeated

None. One run cannot show a repeat. Two personas hit each of the items below, but those are two voices in a single run, not replication. Nothing here is reported as a finding.

## 📋 Missing cases that repeated

None, for the same reason. See *Seen once*.

## ⚠️ Contradictions with the brief

None reported as findings. See the first *Seen once* item for the one point where a persona's own success criterion clashed with a decided rule.

## 🔍 Outliers

P02 (platform developer, run 1) declined to continue in three of four choices: C1 (leave rather than pick from the list), C2 (leave on seeing a mentor-set price), C3a (close the slots view). P02 would have booked in only one case, C3b, where the pressure was changed to "shipping tomorrow, the internal channel silent for an hour". Even there the persona set a condition: the company must pay and a slot must exist soon enough. The persona's stated reasons: nothing was on fire, an internal channel with two hundred people exists, it does not pay for work personally. This is the barely-cares seat doing what it was built to do. It shows that for this segment, urgency together with employer payment is the pressure that matters. It is one persona from one note.

## 🔁 Seen once, not reported as a finding

1. **Two-hour minimum start versus "within the hour".** P01 (run 1): fast reaction frustrated / intense at step 4; would book the earliest slot only because the release is the day after, otherwise would "leave and go back to Stack Overflow and Discord"; P01's own success line (L4) says "within the hour". P02 (run 1): impatient / moderate at step 4; sees two hours as slow and notes a slot is not guaranteed. [SYNTHETIC] Touches D22 / R03, A04. Note: D22 already says "within the hour" is not promised; the clash is with the persona's own criterion, not with the brief. Transcripts: [P01](transcripts/run-1-P01.md), [P02](transcripts/run-1-P02.md).
2. **Price is set by the mentor and unknown until the offer.** P01: wary / moderate; the price "decides"; picks the 25-minute session if reasonable. P02: wary / moderate; leaves. [SYNTHETIC] Touches D09 / R02, A02. Caution: the brief gives no price, so the personas reacted to an absence in the material, and my prompt also pushed the "decides" wording (see limits).
3. **The list gives no sign of who is competent.** P01 (step 2, C1): picks on availability only, "no way to tell". P02 (step 2, C1): skeptical, lists reviews, history or proof as missing. [SYNTHETIC] Touches D21, A02. Caution: decision N02 ("no ratings; a link to public work and a plain description on every mentor page") exists in the repository but is not in the brief's flow or in the excerpt the personas saw. The missing case may therefore be an omission of the brief rather than of the product. P02's "reviews" request also runs against what the held-out note says about stars (see Parity).
4. **Logging in before seeing anything.** P01: annoyed / mild at step 1 (derived from the rushed state of mind, not from a source line). P02: shrug / mild; asks whether the list can be browsed without an account and which GitHub permissions are asked. [SYNTHETIC] Touches D07.
5. **What happens when no slot fits, the mentor does not show, or the session drops.** P01 step 4: no option for "now" and nothing for "no slot before tomorrow". P02 steps 4–5: asks whether another time can be requested and what happens on a no-show. [SYNTHETIC] Cancellation and payments are brief Non-goals, so this may be out of the slice by design. D27 mentions refunds and no-show rules, which the personas did not see.
6. **How code is shown in the session, and whether the conversation can be kept.** P01 step 5: asks how to show code and wants something to keep because it distrusts its workaround. P02 step 5: would keep its own notes; the note after the consultation is out of scope. [SYNTHETIC] The two personas, and the held-out note, differ here.

## 🧪 To confirm with real users

| # | Hypothesis | Persona ids / runs | Settles | Who to recruit | How |
|---|---|---|---|---|---|
| 1 | A developer who is blocked before a release would give up on a service whose earliest start is two hours after booking. | P01, P02 / run 1 | A04 (D22, R03) | Developers who hit a blocker before a release in the last month, with no senior available | Ask for the last time: when it happened, how long they waited for any help, and the point at which help stopped being useful. Compare with the measured booking-to-start time D22 already requires. |
| 2 | A mentor-set price that is unknown until the offer page stops or delays a booking. | P01, P02 / run 1 | A02 (D09, R02) | Developers who paid for one-to-one help, and developers who chose not to | Ask for the last time they decided whether to pay, and what they knew about the price at that moment. Add a usability task on the mentor offer page once real prices exist. |
| 3 | A list ordered by recent availability gives no basis for choosing a mentor. | P01, P02 / run 1 | A02 (D21, N02) | Developers who recently chose a helper for a technical problem | Ask what they looked at before choosing. Then give them the list order alone and ask how they would pick. Check whether the public-work link from N02 changes that. |
| 4 | Developers at large companies with an internal channel decline unless the problem is urgent and the employer pays. | P02 / run 1 | A02 | Platform developers at large companies | Ask who paid for any outside help last time, what reimbursement needed, and how often they run into an urgent case. Frequency is unknown in the material. |
| 5 | Missing handling for "no slot fits", no-show and a dropped session loses urgent users at steps 4–5. | P01, P02 / run 1 | A04 | Urgent-blocker developers | Usability task on the booking and session steps with a case where no slot fits before the deadline. Check D27 and the spec for what the product already handles. |
| 6 | Whether urgent users want to keep the session while non-urgent users do not. | P01, P02 / run 1 | A02 | Urgent-blocker developers and platform developers | Ask what they did with the answer after the last time they got help. |
| 7 | Requiring an account before seeing any mentor adds a drop-off for urgent users. | P01, P02 / run 1 | none directly (D07); adjacent to A04 | Urgent-blocker developers | Ask whether a visitor can see the mentor list before login, then test the sign-up step on a task with a time limit. |

## 📝 Interviews

- [run 1, P01](transcripts/run-1-P01.md): question, fast reaction and feeling, considered answer, passages used, decisions under pressure, walk, topics.
- [run 1, P02](transcripts/run-1-P02.md): same structure.

## 🔍 Parity with real interviews

The held-out note is a backend developer in fintech, interviewed once, urgent case on a Friday evening. 11 themes were extracted from it: (1) urgent blocker before a release with nobody on; (2) internal channel and a community post both failed; (3) rollback and slipped release as the cost; (4) needs a helper within about twenty minutes; (5) account creation or verification would stop a booking; (6) price a shrug, who pays unresolved; (7) one earlier paid session, slow to find, ended on a failed call; (8) prefers text; (9) judges a helper by specific prior work (GitHub), not title, and says ratings carry no information; (10) does not want saved answers on a site; (11) does not want a subscription, community or learning path.

The panel also raised 9 of these: 1, 2, 4, 5, 6, 8, 9, 10, 11. That is 9 of 11, written to [calibration.md](../../calibration.md).

- **Where the sentiment differs.** (a) On saved answers (10), P02 agrees with the real note, but P01 asked for something to keep. (b) On trust signals (9), P02 asked for "reviews, history, any proof", while the real note says "każdy ma pięć gwiazdek". (c) On paying (6), the held-out interviewee would pay out of its own pocket ("chyba"), while P02 would not.
- **Where the panel is generic and the real note specific.** The real note names twenty minutes, a five-minute booking cut-off and a wedding-weekend gap. The panel says "within the hour" and "login is an extra step".
- **Real-only (the panel's blind spots).** The cost of failing (a rollback and a release moved to Tuesday), and a first paid-help attempt that was slow to find and ended on a failed call. Both need persona lines.
- **Panel-only (questions for the next real interview).** An internal channel with two hundred people as a reason not to buy; not paying for work personally; paying only for a once-only job costing a day; willingness to pay depending on a deadline; no-show and no-slot handling; browsing without an account; showing code in the session.
- Both persona notes and the held-out note come from the same founders' interview programme. Some overlap reflects that shared script, not independent convergence.

## 📸 Evidence

Narrative walk; no screens and no screenshots exist for this session.
