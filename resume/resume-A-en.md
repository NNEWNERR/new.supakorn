# Resume — Version A (Automation QA / SDET) · EN
> Master copy. Tailor per posting; never edit this file for a single company — copy it first.
> Section order is fixed: Summary → Test Automation Projects → Technical Skills → Work Experience → Education.
> Every number here traces to a real repo. Do not round up.

**SUPAKORN SAWETWONGSAKUL (New)**
Automation QA Engineer — Playwright + TypeScript
Samut Songkhram, Thailand · open to Remote / Hybrid / Bangkok
newnertg@gmail.com · github.com/NNEWNERR · nnewnerr.github.io

## Summary
Frontend developer who moved into test automation. 358 automated tests across four projects —
Playwright E2E, API contract, and Firestore security rules — behind 10 Page Objects and
7 GitHub Actions workflows, one of them a daily soak run against a live production booking
platform. One year shipping Angular/Ionic on Firebase means I test the layer I used to write.

## Test Automation Projects

**Krungthon Air — Booking QA suite** *(private repo — my own business)*
- Built 96 E2E/API tests across 36 spec files for a production Firebase booking platform, covering auth, booking, access rights, concurrent double-booking, tenant isolation, a11y and mobile responsive.
- Wrote 90 Firestore security-rules tests running on the emulator on every push, asserting what must be **denied**, not only what must pass.
- Traced 53 test cases back to TC-IDs, so coverage is auditable rather than estimated.
- Ran 4 GitHub Actions workflows: a 17-config matrix on PRs, the 90-case rules suite per push, Discord alerts, and a daily production soak that surfaces regressions within 24 hours instead of at the next PR.

**multitenant-booking-qa** — github.com/NNEWNERR/multitenant-booking-qa
- Designed 93 tests in two layers over one system: 76 Firestore rules tests + 17 Playwright UI tests on desktop and Pixel 7, both against a real emulator, no mocks.
- Found 2 real defects by writing the UI layer: legacy documents the query could not see although the rules allowed them, and a modal trapped under the topbar for 200 ms mid-animation.
- Proved with a 24-case `public-boundary` suite that the real access boundary is "no tenant yet", not "not logged in".
- Kept the suite credential-free so a reviewer runs it with `npm ci && npm test`.

**qa-automation** — github.com/NNEWNERR/qa-automation
- Structured 63 tests into 8 Playwright projects: API contract, UI, accessibility (axe-core), visual regression, smoke, and per-role auth via `storageState`.
- Shortened CI feedback by running 4 parallel shards and merging blob reports into a single HTML report.
- Tagged tests `@smoke` `@regression` `@a11y` `@visual` so one layer can be run on demand instead of the whole suite.
- Ran Playwright Test Agents end to end (planner → generator → healer): 32 planned scenarios → 31 generated tests reviewed against a flake playbook, with each human fix recorded; the repo rule lets the healer repair locators but not change expected values, weaken assertions or add retries — and I verified it obeys that.

**sauce-demo-tests** — github.com/NNEWNERR/sauce-demo-tests
- Covered login, product sorting, cart and checkout in 16 tests behind 4 Page Objects on a shared `BasePage`, with visual and accessibility checks.
- Wrote `TESTING.md`, a test strategy document with scope, risk matrix and test pyramid.

## Technical Skills
**Automation** Playwright (TypeScript), Selenium, Page Object Model, API/contract testing, Postman, axe-core accessibility, visual regression, Firebase Emulator, Vitest
**CI/CD** GitHub Actions (matrix, sharding, blob-report merge, scheduled soak), Discord notification, Git
**Development** TypeScript, JavaScript, Angular, Ionic, Tailwind CSS, Firebase/Firestore
**Test design** equivalence partitioning, boundary value analysis, decision table, state transition, risk-based testing

## Work Experience
**Frontend Developer** — startup · 1 year
- Shipped features in Angular, Ionic and Tailwind CSS on a Firebase backend — the same stack I now write tests against, which is why I know where it breaks.

**Event Organizer / Project Coordinator** — Nai Krit Sticker sign shop · current
- Produce pre-event documentation, project summary reports and survey data.

## Education
**B.Eng. (Continuing Program), Electronics Engineering Technology**
King Mongkut's University of Technology North Bangkok — College of Industrial Technology

---
### If it runs past one page, cut in this order
1. `sauce-demo-tests` bullet 1 — the 16 tests are the smallest number on the page and the strategy doc is the part worth keeping.
2. The Event Organizer bullet — current job, but unrelated to QA; the job title alone covers the employment gap.
3. `qa-automation` bullet 3 (tags) — nice design detail, but the sharding bullet already shows CI judgement.
Never cut: the 90 rules tests, the daily soak, or the 2 real defects found. Those are the three things no bootcamp portfolio has.
