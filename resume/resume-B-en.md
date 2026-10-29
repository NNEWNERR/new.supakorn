# Supakorn Sawetwongsakul (New) — Software Tester / QA Analyst
Samut Songkhram, Thailand · open to remote / hybrid / Bangkok · newnertg@gmail.com
github.com/NNEWNERR · nnewnerr.github.io

> Resume version B — for Software Tester / QA Analyst / Manual QA postings.
> The pitch is how I think as a tester, not a pile of scripts; automation sits last,
> as something I can also do.

## Summary
I test software by starting from case design, not from tooling — decision tables, state
transition, EP/BVA and risk-based analysis to find the paths bugs actually live on — and I
write bug reports a developer can act on without asking me a follow-up question. A year as a
frontend developer means I speak the team's language and ask the questions that rule variables out.

## Test Design & QA Practice
- Designed cases with a **decision table (role × screen)** when one single new role was added,
  and found 6 places that failed silently — including refresh and deep-link paths that ordinary
  click-through testing never reaches.
- Applied **state-transition testing** to the cancellation path and found 640 queue seats left
  stranded, filing the bug report together with an idempotent clean-up approach.
- Built **negative testing across 3 layers** for cross-organisation data isolation, found a hole
  in all 3, and confirmed the fix with a 90-case permission-rules suite on a real emulator.
- **Separated "flaky test" from "unstable system" before reaching for retries**: a login that
  failed at random turned out to be a race condition between two sessions, not something to
  paper over.
- Proved **the test was wrong, not the system**, by dropping the UI and calling the API directly —
  turning a "double booking is possible" accusation into an answerable question. The root cause
  was 4 layers of bugs in the test itself.
- Used **hit-testing instead of visibility checks** on a button that was visible but unclickable,
  and only on mobile, because a tool reporting "pass" is not a user being able to use it.
- Wrote **8 bug reports** to one consistent shape: symptom → how I traced it → root cause → fix →
  verification → lesson, publishable with no customer data or config values
  (new.supakorn/case-studies).
- Annotated every test in my qa-automation repo with the technique behind it and why
  (equivalence partitioning, boundary, decision table, state transition).

## Work Experience
**Frontend Developer** — startup · 1 year
Shipped features in Angular, Ionic and Tailwind CSS on a Firebase backend. I have been on the
receiving end of bug reports, so I know which ones a developer can act on straight away, and
which seams of a system bugs tend to collect in.

**Event Organizer / Project Coordinator** — Nai Krit Sticker sign shop · current
Pre-event documentation, project wrap-up reports and survey data handling — work where the
paperwork has to match reality every time.

## Automation Toolkit *(something I can also do, not a replacement for test design)*
Playwright + TypeScript on the Page Object Model — 358 automated tests, 10 Page Objects,
7 GitHub Actions workflows, Firestore rules tests on the emulator, API testing with Postman.
I reach for it when repetitive regression cases start eating the time that should go to
exploratory testing.

## Education
B.Eng. (continuing programme), Electronics Engineering Technology —
King Mongkut's University of Technology North Bangkok, College of Industrial Technology
