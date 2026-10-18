# Walkthrough: Future state, booking and session (1.0), decided steps — `.ai/specs/product-brief.md`, 2026-10-18, session 002 (audited profiles)

With one run, this panel again supports no finding. The next real check is the same as in session 001: ask urgent-blocker developers whether the minimum start time after booking (R03, D22) makes help arrive too late (A04). On corrected profiles the clearest point is a different one: both personas said the mentor list gave them nothing to judge who has done this kind of problem (D21, A02). They said so in both sessions. Every item is synthetic and does not satisfy the Definition of Ready.

Stance: adversary (brief mode `own`)
Panel: 1 run × 2 personas; run 1: P01, P02
Basis: same as session 001. Persona lines were audited against `2026-08-20-interview-working-dev` and `2026-09-02-interview-platform-dev-solves-alone`; 10 lines without support in the notes were removed, and scenario assumptions were moved to separate `[ASSUMPTION]` blocks.
Panel snapshot: [personas.md](personas.md)
Session: `.ai/specs/research/walkthroughs/2026-10-18-future-state-booking-and-session-1-0-decided-steps-session-002/`; subject `.ai/specs/product-brief.md`; flow "Future state, booking and session (1.0), decided steps"
Composition: assumed (brief states no proportions). One persona per segment, because each segment has one note.
Saturation: not reached. Of P02's 15 topics, about 9 were not raised by P01.
Parity: 9 of 11 held-out themes also raised by the panel, against `holdout/2026-09-01-interview-backend-dev-fintech.md`. Same two real-only themes as session 001. See below and [calibration.md](../../calibration.md); the two rows are one measurement, not two.
Elapsed: persona subagents ran in parallel for about 53 s (P01) and about 32 s (P02). Other phases were not timed.
Not askable of this panel: none. A02 and A04 were put to both personas (Q6, Q7); both had no basis for Q7.

## 🎯 Scope and limits

Narrative walk of the five-step Key flow; no screens, no browser, no app. Not covered: mentor onboarding, prices, payments, cancellation, payouts, post-session note (brief Non-goals).

- This session is not an independent replication of session 001. It uses the same two source notes, so each seat is still one voice. A finding needs several runs with fresh panels, and this session adds one run.
- Each persona answered all parts in one fresh-context call, so the interviewer could not adapt questions.
- The changes against session 001 are the profile audit and the removal of the prompt sentence that told personas to say when "a number would decide". Everything else is unchanged.
- Acquiescence: of the 7 answered past-behaviour yes/no questions, 2 were "yes" (both P01, each tied to a line in its own note), none were above one half; 2 "no basis" answers (one per persona) are the material's gaps. Nothing excluded.
- Known biases: over-positivity absent (P02 leaves in 3 of 4 choices and states "no basis" at C3b). P02 again reuses the source's Polish quotes word for word in Q1, Q2, Q3 and Q5, which adds little beyond the profile. Both personas are developers; no tool was proposed by both.

## 🔍 Barriers that repeated

None. One run cannot show a repeat. The items below were each raised by two personas in one run, which is not replication.

## 📋 Missing cases that repeated

None. See *Seen once*.

## ⚠️ Contradictions with the brief

None reported as findings. P01's step 4 clash is with its own success criterion, not with the brief (D22 already says "within the hour" is not promised).

## 🔍 Outliers

P02 declined or would decline in three of four choices: C1 (open the list, but leave without a known name or evidence of what the mentor did), C2 (probably leave unless the company pays), C3a (leave without booking; nothing is urgent). At C3b, where urgency was imposed, P02 stated that its profile gives no basis and declined to invent a reaction. In session 001 the same seat said it would book if the company paid; that came from a line the note does not support and was removed. The only stated condition for paying a person is: a once-only job that costs a day, found in five minutes, done within the hour, paid by the company. Whether that condition ever meets the mentor's published-slot model is unknown.

## 🔁 Seen once, not reported as a finding

1. **The list gives no sign of who has done this kind of problem.** P01 (step 2 "too thin for a decision", moderate; C1 picks the top name only because the order is all it has). P02 (step 2 sceptical, mild; C1 would use a known name or evidence of what a mentor did, otherwise leave). [SYNTHETIC] Touches D21, A02. Present in both persona seats in both sessions. Caution: N02 (a link to public work and a description on each mentor page) is a decided element that the brief's flow and the persona excerpt do not show, so this may be a gap in the brief rather than the product.
2. **Minimum start after booking versus "within the hour" (urgent seat only).** P01 step 4 "that's not 'within the hour'" (moderate); C3a would check whether any slot arrives before the release and otherwise go back to the list. P02, in a non-urgent setting, found no friction. [SYNTHETIC] Touches D22 / R03, A04. In session 001 this was rated "frustrated / intense"; with the "anxious" line removed it is moderate.
3. **Who pays, and the mentor-set price.** P02 step 3: who pays and whether the company would; C2 leaves unless the company pays. P01 step 3: a one-off price is acceptable in principle, and it cannot say where its limit is. [SYNTHETIC] Touches D09 / R02, A02. The brief gives no price, so the personas react to an absence in the material.
4. **No fallback when no slot fits.** P01 step 4 (no option to ask for help sooner than published slots; C3a looks at another mentor). P02 step 4 (what happens if the mentor has no slot). [SYNTHETIC] Touches D22, A04.
5. **Sending code beforehand, and what is kept afterwards.** P01 steps 3 and 5. P02 step 5 would keep its own notes. [SYNTHETIC] Weak: the post-session note is a brief Non-goal.
6. **Browsing before login, and how long sign-up takes.** Raised by both as a question; neither reports friction. [SYNTHETIC] Touches D07. Weakest item.

## 🧪 To confirm with real users

| # | Hypothesis | Persona ids / runs | Settles | Who to recruit | How |
|---|---|---|---|---|---|
| 1 | A list ordered by recent availability gives no basis for choosing a mentor, so users fall back on a known name or on leaving. | P01, P02 / session 002 run 1 (also session 001) | A02 (D21, N02) | Developers who recently chose a helper for a technical problem | Ask what they looked at before choosing. Then show the list order alone and ask how they would pick. Check whether the public-work link from N02 changes that. |
| 2 | For a developer blocked before a release, the minimum start after booking makes help arrive too late. | P01 / run 1 | A04 (D22, R03) | Developers who hit a blocker before a release in the last month, with no senior available | Ask for the last time: when it happened, how long they waited for any help, and when help stopped being useful. Compare with the booking-to-start time D22 already requires. |
| 3 | The first obstacle for employed developers is who pays, not the price amount. | P02 / run 1 | A02 (D09) | Platform developers at companies with an internal channel | Ask who paid for any outside help last time, what reimbursement required, and what they did when the internal channel was silent (the note has no basis for this). |
| 4 | No slot fitting, with no fallback, ends the attempt. | P01, P02 / run 1 | A04 | Urgent-blocker developers | Usability task on step 4 with a case where no slot fits before a deadline. Check D27 and the spec for what the product already handles. |
| 5 | Urgent users want to send code before the session and to keep what they get. | P01 / run 1 | A02 | Urgent-blocker developers | Ask what they did with the answer after the last time they got help. |
| 6 | An account requirement before seeing mentors, or a slow sign-up, costs urgent users. | P01, P02 / run 1 | none directly (D07) | Urgent-blocker developers | Ask whether a visitor can see the mentor list before login, then time the sign-up on a task with a deadline. |

## 🔁 Against session 001

What stayed: the missing sign of mentor competence (both seats), the lead-time clash for the urgent seat, no fallback when no slot fits, and the pressure effect of removing P01's deadline.
What dropped, and why:
- "The price decides" for both personas. It came from my prompt wording, which is gone.
- P01's annoyance at login. It came from the removed "anxious" line.
- P02's "impatient" reaction at step 4 and the "urgency plus employer pays flips it" outlier story. Both rested on lines the note does not support.
- P01 wanting the session kept versus P02 and the held-out note not wanting it. P01 now only asks what is kept afterwards.
- P02's request for "reviews, history, any proof". It now asks for what the mentor did, which is closer to the held-out note.
The session 001 report is unchanged; read its outlier paragraph and table row 4 together with this section.

## 📝 Interviews

- [run 1, P01](transcripts/run-1-P01.md)
- [run 1, P02](transcripts/run-1-P02.md)

## 🔍 Parity with real interviews

The 11 themes extracted from the held-out note are the same as in session 001. The panel raised 9: urgent blocker with nobody available (P01), community post failed (P01's Discord), needs a helper fast (P01 "within the hour", P02 "five minutes, within the hour"), account and sign-up friction (both asked about browsing and sign-up time, thin), price and who pays (both), text preferred (both), judging a helper by what they did (both), not wanting saved answers (P02; P01 only asks what is kept), no subscription or learning path (both).

- **Real-only (blind spots):** a rollback and a slipped release as the cost of failing; one earlier paid session that was slow to find and ended on a failed call.
- **Panel-only (questions for the next real interview):** an internal channel as a reason not to buy; not paying for work personally; paying only for a once-only job costing a day; what happens when the channel is silent; no fallback when no slot fits; sending code beforehand.
- **Sentiment:** the two clashes seen in session 001 (reviews, saved answers) are gone with the profile audit. One remains: the held-out interviewee would pay out of its own pocket ("chyba"), while P02 would not.
- **Generic where real is specific:** the real note names twenty minutes and a five-minute booking cut-off; the panel says "within the hour" and asks how long sign-up takes.
- The held-out note was read before this audit. The audit checked lines against the two persona notes only, but the two parity rows should be read as one measurement.

## 📸 Evidence

Narrative walk; no screens and no screenshots exist for this session.
