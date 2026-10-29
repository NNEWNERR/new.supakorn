# Supakorn Sawetwongsakul (New) — Automation QA Engineer
Samut Songkhram, Thailand · open to remote / hybrid / Bangkok · newnertg@gmail.com
github.com/NNEWNERR · nnewnerr.github.io

> Resume version A — for Automation Tester / QA Engineer (Automation) /
> Test Automation Engineer / SDET postings. Every number here comes from a real repo.

## Summary
I write end-to-end and API automation in Playwright + TypeScript on the Page Object Model —
358 automated tests and 7 CI workflows across 4 systems, one of them a platform in live use.
Before moving into QA I spent a year as a frontend developer, so I can read the code I am
testing and I know first-hand how apps break.

## Test Automation Projects

**Krungthon Air — QA suite** *(private · live Firebase booking platform)*
- Designed and maintain 96 E2E/API tests across 36 spec files in Playwright + TypeScript,
  covering auth, booking, access control, concurrent double-booking, tenant data isolation,
  accessibility and mobile responsiveness, with 53 tests traced back by TC-ID.
- Wrote 90 Firestore security-rules tests that run against the real emulator on every push —
  no mocks.
- Built 4 GitHub Actions workflows: a 17-way matrix on pull requests, the 90-case rules suite
  on every push, Discord reporting, and a daily soak run against production that catches
  regressions within 24 hours instead of waiting for the next PR.

**multitenant-booking-qa** — github.com/NNEWNERR/multitenant-booking-qa
- Wrote 93 tests in two layers over the same system: 76 Firestore rules tests + 17 Playwright
  UI tests (desktop and Pixel 7), both against Firebase Emulator. `npm ci && npm test` is the
  whole setup — no credentials needed.
- Found 2 real bugs while writing the UI layer: legacy documents the query could not see even
  though the rules allowed them, and a modal trapped under the topbar for 200 ms mid-animation.
- Designed a 24-case `public-boundary` suite proving the real permission boundary is
  "no organisation yet", not "not logged in".

**qa-automation** — github.com/NNEWNERR/qa-automation
- Structured 63 tests across 8 Playwright projects, separating API contract, UI, accessibility
  (axe-core), visual regression, smoke, and per-role auth via `storageState`.
- Set CI to run 4 shards in parallel and merge the blob reports back into a single HTML report;
  tagged tests (`@smoke` `@regression` `@a11y` `@visual`) so any one layer can be run alone.
- Used Playwright Test Agents (planner → generator → healer) for real: a 32-scenario plan
  became 31 generated tests reviewed against a flake playbook, under a repo rule that the
  healer may repair locators but must never change expected values, weaken assertions, or add
  retries/timeouts — and I verified it holds.

**sauce-demo-tests** — github.com/NNEWNERR/sauce-demo-tests
- 16 tests covering login, product sorting, cart and checkout, with visual and accessibility checks.
- 4 Page Objects on a shared `BasePage` (10 across all repos) and `TESTING.md`, a test strategy
  document with scope, a risk matrix and a test pyramid.

**Case Studies** — new.supakorn/case-studies · 8 cases from systems in live use
Each traced from symptom to root cause: 640 queue seats leaked through the cancellation path,
tenant isolation that turned out to be broken at all 3 layers, and legacy permission rules that
left 15 cases red in the original rules suite.

## Technical Skills
**Automation:** Playwright, TypeScript, Selenium, Postman / API testing, Vitest, axe-core
**CI & infra:** GitHub Actions (matrix, sharding, blob-report merge), Firebase Emulator, Git
**Systems tested:** Firebase / Firestore Rules / Cloud Functions, Angular, Ionic
**Test design:** EP/BVA, decision tables, state transition, risk-based, negative testing

## Work Experience
**Frontend Developer** — startup · 1 year
Shipped features in Angular, Ionic and Tailwind CSS on a Firebase backend. I understand what
I test because I used to build it — I know which layer stale state and race conditions live in.

**Event Organizer / Project Coordinator** — Nai Krit Sticker sign shop · current
Pre-event documentation, project wrap-up reports, and survey data handling.

## Education
B.Eng. (continuing programme), Electronics Engineering Technology —
King Mongkut's University of Technology North Bangkok, College of Industrial Technology
