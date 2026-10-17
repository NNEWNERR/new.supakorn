# เรซูเม่เวอร์ชัน A — Automation QA Engineer / SDET

> เวอร์ชันกลาง (master) สำหรับระดับ A — ห้ามส่งทั้งฉบับนี้ตรง ๆ ต้องปรับคีย์เวิร์ดตามประกาศทุกครั้ง
> ตัวเลขทุกตัวในไฟล์นี้มาจาก repo จริง (ดู `README.md` ของโปรเจกต์นี้) — ห้ามปัดขึ้น
> ลำดับหัวข้อ: Summary > Test Automation Projects > Technical Skills > Work Experience > Education

---

## ฉบับภาษาไทย (1 หน้า)

**ศุภากร เศวตวงศ์สกุล (นิว)**
Automation QA Engineer — Playwright + TypeScript
newnertg@gmail.com · github.com/NNEWNERR · nnewnerr.github.io · นครปฐม · รับ remote / hybrid / กรุงเทพฯ

### Summary
- เขียน E2E และ API automation ด้วย Playwright + TypeScript รวม **358 automated tests** ใน 4 ชุดเทส ครอบคลุม UI, API contract, Firestore security rules, accessibility และ visual regression
- ออกแบบโครงสร้างชุดเทสด้วย **Page Object Model 10 คลาส** และวาง **CI 7 workflow** บน GitHub Actions ที่รันจริงทุก PR และทุกวัน
- เคยเป็น frontend developer 1 ปี (Angular / Ionic / Firebase) จึงอ่านโค้ดที่ตัวเองทดสอบได้ และรู้ว่าบั๊กมักเกิดที่รอยต่อไหน

### Test Automation Projects
**ระบบจองคิวบน Firebase (ระบบลูกค้าที่ใช้งานจริง — repo private)** · Playwright, TypeScript, Firebase, Angular
- สร้างชุดเทส **96 E2E/API tests ใน 36 spec files** ครอบคลุม auth, การจอง, สิทธิ์การเข้าถึง, การจองชนกันแบบ concurrent และการแยกข้อมูลระหว่าง tenant
- เขียน **Firestore security rules tests 90 เคส** รันบน emulator จริงทุก push จึงจับ rule ที่เปิดกว้างเกินได้ก่อนขึ้น production
- ทำ **traceability ด้วย TC-ID 53 เคส** ให้ทุกเทสอ้างกลับไปที่ test case ได้ ใช้รายงานผลกับผู้ดูแลระบบได้ตรงเคส
- วาง **CI 4 workflow** — matrix 17 ชุดตอน PR, ชุด rules บน emulator ทุก push, แจ้งเตือนเข้า Discord และ **daily soak ยิง production ทุกวัน** ลดเวลาจับ regression เหลือภายใน 24 ชั่วโมง

**[multitenant-booking-qa](https://github.com/NNEWNERR/multitenant-booking-qa)** · Firestore Rules, Playwright, Vitest, Firebase Emulator
- ทดสอบระบบเดียวกันสองชั้น **93 tests** = security rules 76 เคส + Playwright UI 17 เคส (desktop + Pixel 7) รันกับ emulator จริงทั้งคู่ ไม่ใช้ mock
- ออกแบบชุด **public-boundary 24 เคส** ด้วย equivalence partitioning พิสูจน์ว่าเส้นแบ่งสิทธิ์จริงคือ "ยังไม่มีสังกัด" ไม่ใช่ "ยังไม่ล็อกอิน"
- **เจอบั๊กจริง 2 ตัว** จากการเขียน UI test: เอกสารรุ่นเก่าที่ query มองไม่เห็นแม้ rules อนุญาต และ modal ที่ถูกขังใต้ topbar 200 ms ระหว่าง animation
- ทำให้ติดตั้งแล้วรันได้ด้วย `npm ci && npm test` โดยไม่ต้องมี credential ใด ๆ

**[qa-automation](https://github.com/NNEWNERR/qa-automation)** · Playwright, TypeScript, GitHub Actions
- จัดโครง **63 tests ใน 8 Playwright projects** แยก API contract, UI, accessibility (axe-core), visual regression, smoke และ auth ตาม role ด้วย `storageState`
- ตั้ง CI ให้รัน **4 shard ขนาน** แล้ว merge blob report กลับเป็นรายงาน HTML ฉบับเดียว เลือกรันทีละชั้นได้ด้วย tag `@smoke` `@regression` `@a11y` `@visual`
- ใช้ **Playwright Test Agents** (planner → generator → healer) จริง: แผน 32 scenario → 31 เทสที่ผ่านการรีวิวตาม flake playbook พร้อมบันทึกว่ามนุษย์แก้อะไร
- เขียนกติกาประจำ repo ว่า healer แก้ locator ได้ แต่ห้ามแก้ค่าที่คาดหวัง ลด assertion หรือเพิ่ม retry/timeout แล้วทดสอบว่ากติกาถูกบังคับจริง

**[sauce-demo-tests](https://github.com/NNEWNERR/sauce-demo-tests)** · Playwright, TypeScript
- เขียน **16 tests** ครอบคลุม login, การเรียงสินค้า, ตะกร้า, checkout พร้อม visual และ accessibility check
- แยก **4 Page Object บน `BasePage` ร่วมกัน** ลดโค้ดซ้ำของ selector และทำให้แก้ที่เดียวเมื่อ UI เปลี่ยน
- เขียน **`TESTING.md`** เอกสารกลยุทธ์การทดสอบ มีขอบเขต, risk matrix และ test pyramid

### Technical Skills
- **Test automation:** Playwright (TypeScript), Cypress, Selenium, Appium (พื้นฐาน), Vitest
- **API & data:** REST API testing, Postman, Firestore security rules testing, Firebase Emulator Suite
- **CI/CD:** GitHub Actions (matrix, sharding, blob report merge, scheduled soak), Discord webhook notification
- **Test design:** Page Object Model, equivalence partitioning / boundary value analysis, decision table, state transition, risk-based testing
- **คุณภาพชุดเทส:** flake playbook, skip-เมื่อ-dependency-ไม่พร้อม แทนการ fail, visual baseline ผูกกับ OS
- **Development:** Angular, Ionic, TypeScript / JavaScript, Tailwind CSS, Firebase, Git

### Work Experience
**Frontend Developer** — สตาร์ทอัพ · 1 ปี
- พัฒนาและส่งมอบฟีเจอร์ด้วย Angular, Ionic, Tailwind CSS บน backend Firebase — เป็นช่วงที่ได้เห็นสาเหตุที่แอปพังจากฝั่งคนเขียน ซึ่งกลายเป็นฐานในการออกแบบเทสตอนนี้

**Event Organizer / Project Coordinator** — ร้านนายกิจสติ๊กเกอร์ · ปัจจุบัน
- จัดทำเอกสารก่อนงาน, รายงานสรุปโปรเจกต์ และดูแลข้อมูลแบบสำรวจ

### Education
**วศ.บ. (ต่อเนื่อง) เทคโนโลยีวิศวกรรมอิเล็กทรอนิกส์** — มหาวิทยาลัยเทคโนโลยีพระจอมเกล้าพระนครเหนือ วิทยาลัยเทคโนโลยีอุตสาหกรรม

---

## English version (1 page)

**Supakorn Sawetwongsakul (New)**
Automation QA Engineer — Playwright + TypeScript
newnertg@gmail.com · github.com/NNEWNERR · nnewnerr.github.io · Nakhon Pathom, Thailand · Open to remote / hybrid / Bangkok

### Summary
- Build E2E and API automation in Playwright + TypeScript — **358 automated tests** across 4 suites covering UI, API contracts, Firestore security rules, accessibility and visual regression
- Structure suites around **10 Page Object classes** and run them through **7 GitHub Actions workflows** that execute on every PR and on a daily schedule
- One year as a frontend developer (Angular / Ionic / Firebase): I read the code I test and know which seams break

### Test Automation Projects
**Firebase queue-booking platform (live client system — private repo)** · Playwright, TypeScript, Firebase, Angular
- Built **96 E2E/API tests across 36 spec files** covering auth, booking, access control, concurrent double-booking and cross-tenant data isolation
- Wrote **90 Firestore security-rules tests** executed against a real emulator on every push, catching over-permissive rules before production
- Maintained **TC-ID traceability for 53 cases** so every automated test maps back to a written test case for reporting
- Set up **4 CI workflows** — a 17-job PR matrix, the rules suite on every push, Discord alerts, and a **daily production soak** that cuts regression detection to under 24 hours

**[multitenant-booking-qa](https://github.com/NNEWNERR/multitenant-booking-qa)** · Firestore Rules, Playwright, Vitest, Firebase Emulator
- Tested one system at two layers — **93 tests** = 76 security-rules tests + 17 Playwright UI tests (desktop + Pixel 7), both against a real emulator rather than mocks
- Designed a **24-case public-boundary suite** from equivalence partitioning, proving the real permission boundary is "no tenant yet", not "not logged in"
- **Found 2 genuine bugs** while writing UI tests: legacy documents invisible to queries although the rules allowed them, and a modal trapped under the topbar for 200 ms during animation
- Kept the repo runnable with `npm ci && npm test` — no credentials required

**[qa-automation](https://github.com/NNEWNERR/qa-automation)** · Playwright, TypeScript, GitHub Actions
- Organised **63 tests into 8 Playwright projects** separating API contract, UI, accessibility (axe-core), visual regression, smoke and per-role auth via `storageState`
- Configured CI to run **4 parallel shards** and merge blob reports into a single HTML report; tags (`@smoke` `@regression` `@a11y` `@visual`) select one layer at a time
- Used **Playwright Test Agents** (planner → generator → healer) in practice: a 32-scenario plan produced 31 reviewed tests, with every human correction recorded
- Wrote the repo rule that the healer may fix locators but never change expected values, weaken assertions or add retries/timeouts — and tested that the rule holds

**[sauce-demo-tests](https://github.com/NNEWNERR/sauce-demo-tests)** · Playwright, TypeScript
- Wrote **16 tests** across login, sorting, cart and checkout with visual and accessibility checks
- Extracted **4 Page Objects on a shared `BasePage`**, removing duplicated selectors so UI changes are a one-place fix
- Authored **`TESTING.md`**, a test-strategy document with scope, risk matrix and test pyramid

### Technical Skills
- **Test automation:** Playwright (TypeScript), Cypress, Selenium, Appium (basic), Vitest
- **API & data:** REST API testing, Postman, Firestore security-rules testing, Firebase Emulator Suite
- **CI/CD:** GitHub Actions (matrix, sharding, blob-report merge, scheduled soak), Discord webhook alerts
- **Test design:** Page Object Model, equivalence partitioning / boundary value analysis, decision tables, state transition, risk-based testing
- **Suite quality:** flake playbook, skip-on-unavailable-dependency instead of fail, OS-bound visual baselines
- **Development:** Angular, Ionic, TypeScript / JavaScript, Tailwind CSS, Firebase, Git

### Work Experience
**Frontend Developer** — startup · 1 year
- Shipped features in Angular, Ionic and Tailwind CSS on a Firebase backend — the year I saw first-hand why apps break, which is what my test design is built on

**Event Organizer / Project Coordinator** — Naikit Sticker · current
- Prepare pre-event documentation and project reports, and maintain survey data

### Education
**B.Eng. (continuing programme), Electronics Engineering Technology** — King Mongkut's University of Technology North Bangkok, College of Industrial Technology
