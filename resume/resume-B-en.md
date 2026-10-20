# Resume — Version B (Software Tester / QA Analyst) · EN
> Master copy. Tailor per posting; copy before editing.
> Section order is fixed: Summary → Test Design & QA Practice → Work Experience → Automation Toolkit → Education.
> Tone rule for this version: automation is "I can also do this", never the headline. Nothing here may read
> as if the job is a stepping stone — the pitch is that test design is the skill I want to be paid to use.

**SUPAKORN SAWETWONGSAKUL (New)**
Software Tester / QA Analyst
Samut Songkhram, Thailand · open to Remote / Hybrid / Bangkok
newnertg@gmail.com · github.com/NNEWNERR · nnewnerr.github.io

## Summary
Tester with a developer's background: one year building Angular/Ionic on Firebase before moving
to testing, so I read a feature and can tell where it is likely to break and which question to
ask the developer first. I design cases with equivalence partitioning, boundary value analysis,
decision tables and state transition, and I have written up 8 defects found in a booking
platform that is in daily use — symptom through to root cause. I also automate what is worth
automating, but the part I care about is deciding what to test and why.

## Test Design & QA Practice
- Designed 24 cases for one access-control boundary alone (`public-boundary` suite), establishing that the real rule was "user has no tenant yet" rather than "user is not logged in" — the distinction the original requirement left ambiguous.
- Documented 8 defects from a production booking platform as case studies, each tracing symptom → reproduction → root cause, so a developer can act on the report without a follow-up conversation: an auth race condition, roles failing silently, a booking-slot leak, a tenant-isolation hole, a stale service worker serving dead code, a button clickable only on desktop, legacy records escaping new rules, and one case where the test was wrong and the system was right.
- Recorded which technique each test applies and why, per test, in the `qa-automation` README — equivalence partitioning, boundary, decision table, state transition — so case selection is reviewable instead of personal habit.
- Wrote 90 permission cases asserting what the system must **refuse**, after finding that "it works for an admin" says nothing about what a logged-out visitor can reach.
- Wrote `TESTING.md`, a test strategy document with scope, risk matrix and test pyramid, to decide coverage by risk rather than by what is easy to test.
- Insisted that intermittent failures from external dependencies be written down rather than hidden with a retry — a retry added to make a run pass also hides the next real defect in that same test.

## Work Experience
**Frontend Developer** — startup · 1 year
- Shipped features in Angular, Ionic and Tailwind CSS on a Firebase backend, working to a release cycle with developers — which is why a bug report from me arrives with the reproduction steps and environment already filled in.
- Learned where defects actually originate in this stack: state that survives a navigation, permissions checked only in the UI, and behaviour that differs between mobile and desktop.

**Event Organizer / Project Coordinator** — Nai Krit Sticker sign shop · current
- Produce pre-event documentation, project summary reports and survey data — detail-checking work against a fixed deadline.

**Krungthon Air — booking platform** · my own business, ongoing
- Run the QA for a Firebase booking platform used daily by real customers: wrote the test cases, found the defects, and fixed the reports into something actionable.

## Automation Toolkit
Available when a team wants it, and useful for regression work I would otherwise repeat by hand:
Playwright with TypeScript (358 tests across 4 projects, 10 Page Objects), Selenium, API testing with Postman,
accessibility checks with axe-core, and GitHub Actions pipelines including a daily run against production
that reports a regression within 24 hours. Happy to start manual and automate the suites that earn it.

## Education
**B.Eng. (Continuing Program), Electronics Engineering Technology**
King Mongkut's University of Technology North Bangkok — College of Industrial Technology

---
### If it runs past one page, cut in this order
1. The second Frontend Developer bullet — the first already connects dev background to bug reports.
2. The Event Organizer bullet — keep the job title for the timeline, drop the description.
3. The last sentence of Automation Toolkit ("Happy to start manual…") — say it in the interview instead, where tone carries it better than print.
Never cut: the 8 case studies or the 24-case boundary work. For a manual role those are the whole argument.
