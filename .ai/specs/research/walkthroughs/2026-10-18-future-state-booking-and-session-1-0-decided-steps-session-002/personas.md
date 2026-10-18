<!-- Immutable snapshot of the panels used in session 002 (audited profiles). Run 1 panel: P01, P02. Session 001 used earlier wording. -->

# Personas — DevMentor

Basis: `.ai/specs/product-brief.md` (Target group, Problems, Key flows, Business rules) · research notes `2026-08-20-interview-working-dev.md`, `2026-09-02-interview-platform-dev-solves-alone.md` · Built 2026-10-18, audited against the notes 2026-10-18 · Stance default: adversary
Panel composition: two segments named in the brief's Target group, one persona each. Share of each segment is assumed (brief: "Brak danych o proporcjach"). Each segment rests on one interview note, so there is one persona per segment.
Coverage after audit: 24 sourced persona lines (P01 11, P02 13), 0 assumed lines inside the persona blocks. Everything assumed sits in the separate *Scenario assumptions* blocks.
Held out, not used for any line: `holdout/2026-09-01-interview-backend-dev-fintech.md`.
Session 001 ran on the earlier wording of these personas; its immutable snapshot is `walkthroughs/2026-10-18-future-state-booking-and-session-1-0-decided-steps-session-001/personas.md`. The changes are listed under *Removed after audit* for each persona.

## Scenario assumptions common to both personas `[ASSUMPTION]`

Not from the material. They are needed only to run the scenario.
- The persona is a first-time visitor who knows nothing about DevMentor beyond the brief's flow text.
- The persona is placed in the situation of its own Q1 episode "right now", with a thirty-second limit at the list step.
- The persona reads the flow text as written, with no screens, no price and no known earliest slot.
- Pressure variations (C1–C3b) are imposed by the interviewer. They are not behaviour seen in any note.

## P01 — developer blocked the day before a release, no senior available

Runs: 1
- Segment: urgent-problem developer at a mid-size product company `[INTERVIEW]` 2026-08-20-interview-working-dev; brief Target group
- Situation the problem shows up in: stuck on a TypeScript generics error the day before a release; the team's only senior was on leave `[INTERVIEW]` 2026-08-20-interview-working-dev
- What happened and what it cost: 40 minutes on Stack Overflow, a question in a Discord, two contradictory answers, a workaround shipped with a TODO; "half a day, and I still don't trust that code" `[INTERVIEW]` 2026-08-20-interview-working-dev
- Goal, in their words: "I don't want a course, I want an answer." `[INTERVIEW]` 2026-08-20-interview-working-dev
- Success, as they would recognise it: "someone who has actually done this looks at my code and tells me what to do, within the hour." `[INTERVIEW]` 2026-08-20-interview-working-dev
- Constraints: the release was the next day; "I'd pay for speed, not for a subscription." `[INTERVIEW]` 2026-08-20-interview-working-dev
- Tools they already use: Stack Overflow, a Discord, a paid course last year `[INTERVIEW]` 2026-08-20-interview-working-dev
- Words they use: answer, course, speed, subscription, "trust that code" `[INTERVIEW]` 2026-08-20-interview-working-dev
- Objections: the course was "generic, and outdated by the time I finished"; does not want a subscription `[INTERVIEW]` 2026-08-20-interview-working-dev
- Did not care about: video calls ("text is fine, faster") `[INTERVIEW]` 2026-08-20-interview-working-dev
- No basis for: budget amount, who pays, who else decides, how they judge a stranger's competence, attitude to creating an account, whether they use GitHub. Real check: a mentee interview that asks about the last purchase of help and how the helper was chosen.

### Scenario assumptions for P01 `[ASSUMPTION]`
- State of mind at entry: under deadline pressure, because the release is the next day. The note names no emotion; "anxious" and "rushed" are mine.
- That the objection to the course ("generic, outdated") carries over to a mentor session. The note says it only about the course.
- That P01 treats the five steps in the flow as the way it would look for help now.
- The C3b variation ("no deadline") is imposed.

### Removed after audit (not supported by the note)
- "Rushed and anxious" as a sourced state of mind (moved to scenario assumptions, reduced to "under deadline pressure").
- "Topic matters centrally": the note shows a cost and a lack of trust in the workaround, not a rating of importance.
- "Will not pay a subscription" as a refusal: the note says "not for a subscription" as a preference.
- "Discord gave two contradictory answers" as an objection: it is an event; kept under *What happened*.
- "The reason this person would not switch: generic or outdated help they cannot trust": extrapolated from the course.

## P02 — platform developer at a payments company, internal channel available, barely cares

Runs: 1
- Segment: non-urgent configuration developer at a payments company, hybrid `[INTERVIEW]` 2026-09-02-interview-platform-dev-solves-alone; brief Target group
- Situation the problem shows up in: the coding agent stopped applying the team's lint rules; half a day; solved alone; nothing was shipping that day. Handles the agent configuration "bo ktoś musi" `[INTERVIEW]` 2026-09-02-interview-platform-dev-solves-alone
- How much this mattered: "nic się nie paliło"; costs described as normal; would need a platform for this "raz w roku może" `[INTERVIEW]` 2026-09-02-interview-platform-dev-solves-alone
- Goal, in their words: "doszedłbym sam. doszedłem." `[INTERVIEW]` 2026-09-02-interview-platform-dev-solves-alone
- Success, as they would recognise it: pays a person only for something done once and never again that costs a day (a migration); found in five minutes; done within the hour; paid by the company `[INTERVIEW]` 2026-09-02-interview-platform-dev-solves-alone
- Constraints: "nie płacę za rzeczy do pracy sam"; "jest nas dwieście osób" on the internal channel (the note does not say whether this means the company, the department or the channel); "kogo. to mnie pytają" `[INTERVIEW]` 2026-09-02-interview-platform-dev-solves-alone
- If something were on fire: would post on the internal channel, "zawsze ktoś jest" `[INTERVIEW]` 2026-09-02-interview-platform-dev-solves-alone
- Tools they already use: the internal channel; paid only for conferences and books, never a person `[INTERVIEW]` 2026-09-02-interview-platform-dev-solves-alone
- Words they use: "nic się nie paliło", "platforma", "subskrypcja", "co szybsze" `[INTERVIEW]` 2026-09-02-interview-platform-dev-solves-alone
- Objections: a subscription ("jak to subskrypcja, to nie otworzę drugi raz"); "nie potrzebuję platformy do tego"; saved conversations ("sam sobie zapiszę") `[INTERVIEW]` 2026-09-02-interview-platform-dev-solves-alone
- How they judge a helper: "zobaczyłbym, co zrobił" or the word of someone they know; if it were good, they would tell people `[INTERVIEW]` 2026-09-02-interview-platform-dev-solves-alone
- Channel: text or a call, "co szybsze" `[INTERVIEW]` 2026-09-02-interview-platform-dev-solves-alone
- The reason this person would not switch: the internal channel, and being able to solve it alone `[INTERVIEW]` 2026-09-02-interview-platform-dev-solves-alone
- No basis for: any price or budget (the interviewer did not ask), the company's expensing process, attitude to GitHub sign-in, what they would do if the internal channel were silent. Real check: a mentee interview with a platform developer on what the company reimburses and who approves it.

### Scenario assumptions for P02 `[ASSUMPTION]`
- State of mind at entry: the problem is not urgent. The note shows the interviewee glancing at the time and not settling in; that is time pressure during the conversation, not a state of mind about the task.
- Any behaviour once the internal channel is silent. The note says only that, if it were on fire, they would use the internal channel.
- The C3b variation ("ship tomorrow, channel silent for an hour") is imposed.

### Removed after audit (not supported by the note)
- "Unhurried and sceptical" as a sourced state of mind: the note shows glancing at the watch and not sitting down, which points to limited time, and names no scepticism.
- "Large" payments company: the note says a payments company.
- "Little time" as a standing constraint.
- "Will not pay for a problem that is not urgent": the note says "nie" only for that lint problem. It names the conditions under which they would pay (once-only, a day's cost, found in five minutes, within the hour, company pays), and they do not require urgency. When something is on fire, they use the internal channel.
- "Need most of any offer like this not at all" as a general trait: the note says "większości", about the things on offer in the question.
