# เรซูเม่เวอร์ชัน A — Automation QA Engineer / SDET

> ฉบับกลาง (master) ห้ามส่งตรง ให้ fork แล้วปรับคีย์เวิร์ดตามประกาศทุกครั้ง
> ตัวเลขทุกตัวในไฟล์นี้ตรวจสอบกลับได้ที่ repo จริง ดูตาราง "ที่มาของตัวเลข" ท้ายไฟล์
> อัปเดตล่าสุด 2026-10-28

ลำดับหัวข้อ: Summary › Test Automation Projects › Technical Skills › Work Experience › Education

---

## ฉบับภาษาไทย

**ศุภากร เศวตวงศ์สกุล (นิว)**
Automation QA Engineer — Playwright + TypeScript
newnertg@gmail.com · github.com/NNEWNERR · nnewnerr.github.io · สมุทรสงคราม (รับ remote / hybrid / กรุงเทพฯ)

### Summary

สร้างชุดทดสอบอัตโนมัติ 358 เคสด้วย Playwright + TypeScript ครอบคลุม 4 ระบบ ตั้งแต่ E2E, API contract,
security rules, accessibility ไปจนถึง visual regression และรันทั้งหมดผ่าน GitHub Actions 7 workflow
พื้นฐาน frontend developer 1 ปีบน Angular/Ionic/Firebase ทำให้อ่านโค้ดที่กำลังทดสอบออก
และแยกได้ว่าความล้มเหลวอยู่ที่ชั้น UI, API หรือกฎสิทธิ์ ก่อนจะเปิดบั๊ก

### Test Automation Projects

**Krungthon Air — QA suite** *(ระบบจองคิวบน Firebase ที่ใช้งานจริง · repo private — ร้านของผมเอง)*
- เขียนชุดทดสอบ E2E และ API 96 เคสใน 36 spec file ด้วย Playwright + TypeScript ครอบคลุม auth,
  การจอง, สิทธิ์การเข้าถึง, การจองชนกันแบบ concurrent, การแยกข้อมูลระหว่าง tenant, a11y และ mobile
- เขียนชุดทดสอบ Firestore security rules 90 เคสบน emulator รันทุก push จับกฎที่กว้างเกินจำเป็น
  ก่อนขึ้น production ได้ 15 เคสตอนรีวิวกฎรุ่นเก่า
- อ้างอิง test case 53 รายการกลับด้วย TC-ID ทำให้ชี้ได้ว่าความต้องการข้อไหนมีเทสคุ้มแล้วหรือยัง
- วาง CI 4 workflow บน GitHub Actions — matrix 17 ชุดตอน PR, rules suite ทุก push,
  แจ้งเตือนเข้า Discord และ daily soak ยิง production ทุกวัน ลดเวลาเจอ regression เหลือภายใน 24 ชั่วโมง

**[multitenant-booking-qa](https://github.com/NNEWNERR/multitenant-booking-qa)** — Firestore Rules · Playwright · Vitest
- ทดสอบระบบเดียวกันสองชั้น 93 เคส — security rules 76 เคส + Playwright UI 17 เคส
  (desktop และ Pixel 7) รันกับ Firebase emulator จริงทั้งคู่ ไม่ใช่ mock
- เจอบั๊กจริง 2 ตัวจากการเพิ่มชั้น UI test ที่ชั้น rules มองไม่เห็น — เอกสารรุ่นเก่าที่ query มองไม่เห็น
  ทั้งที่ rules อนุญาต และ modal ที่ถูกขังใต้ topbar 200 ms ระหว่าง animation
- ออกแบบชุด `public-boundary` 24 เคสเพื่อพิสูจน์ว่าเส้นแบ่งสิทธิ์จริงคือ "ยังไม่มีสังกัด" ไม่ใช่ "ยังไม่ล็อกอิน"
- ตั้ง repo ให้รันได้ด้วย `npm ci && npm test` โดยไม่ต้องใช้ credential ใด ๆ

**[qa-automation](https://github.com/NNEWNERR/qa-automation)** — Playwright · TypeScript · GitHub Actions
- จัดโครงสร้าง 63 เทสเป็น 8 Playwright project แยกตามชั้น — API contract, UI, accessibility (axe-core),
  visual regression, smoke และ auth รายบทบาทด้วย `storageState`
- ตั้ง CI ให้รัน 4 shard ขนานแล้ว merge blob report กลับเป็นรายงาน HTML ฉบับเดียว
- ติด tag `@smoke` `@regression` `@a11y` `@visual` ให้เลือกรันทีละชั้นได้ตามรอบ deploy
- ใช้ Playwright Test Agents (planner → generator → healer) จริง — แผน 32 scenario ออกมาเป็น
  31 เทสที่ผ่านการรีวิวตาม flake playbook พร้อมบันทึกว่ามนุษย์แก้อะไรบ้าง
- กำหนดกติกาประจำ repo ว่า healer ซ่อม locator ได้ แต่ห้ามแก้ค่าที่คาดหวัง ลด assertion หรือเพิ่ม
  retry/timeout แล้วทดสอบย้อนว่ากติกานี้ถูกบังคับจริง

**[sauce-demo-tests](https://github.com/NNEWNERR/sauce-demo-tests)** — Playwright · TypeScript
- เขียน 16 เทสครอบคลุม login, การเรียงสินค้า, ตะกร้า และ checkout พร้อม visual และ a11y check
- แยก 4 Page Object บน `BasePage` ร่วมกัน ให้การแก้ selector หน้าหนึ่งไม่ลามไปทั้งชุด
- เขียน `TESTING.md` เป็นเอกสารกลยุทธ์การทดสอบ ระบุขอบเขต, risk matrix และ test pyramid

### Technical Skills

- **Test automation** Playwright, TypeScript, Page Object Model, Selenium
- **API & data** Postman, REST contract testing, Firestore security rules, SQL พื้นฐาน
- **ชั้นทดสอบเฉพาะทาง** accessibility (axe-core), visual regression, mobile viewport, concurrency
- **CI/CD** GitHub Actions (matrix, sharding, blob report merge, scheduled soak), Firebase Emulator Suite
- **เทคนิคออกแบบเทส** equivalence partitioning, boundary value analysis, decision table,
  state transition, risk-based, negative testing
- **พื้นฐานจากฝั่ง dev** Angular, Ionic, Tailwind CSS, JavaScript, Firebase, Git

### Work Experience

**Frontend Developer** — สตาร์ทอัพ · 1 ปี
- พัฒนาและส่งมอบฟีเจอร์ด้วย Angular, Ionic และ Tailwind CSS บน backend ที่เป็น Firebase
- ปีนั้นคือที่มาของข้อได้เปรียบตอนทดสอบ — เคยเขียนชั้นที่กำลังทดสอบอยู่ จึงเดาได้ว่า
  state ไหนไม่ถูก reset, ที่ไหนมี race และบั๊กมักซ่อนอยู่ตรงเส้นทางย้อนกลับ

**Event Organizer / Project Coordinator** — ร้านป้ายนายกฤษสติ๊กเกอร์ *(ปัจจุบัน)*
- จัดทำเอกสารก่อนงาน รายงานสรุปโปรเจกต์ และดูแลข้อมูลแบบสำรวจ

### Education

**วศ.บ. (ต่อเนื่อง) เทคโนโลยีวิศวกรรมอิเล็กทรอนิกส์**
มหาวิทยาลัยเทคโนโลยีพระจอมเกล้าพระนครเหนือ — วิทยาลัยเทคโนโลยีอุตสาหกรรม

---

## English version

**Supakorn Sawetwongsakul (New)**
Automation QA Engineer — Playwright + TypeScript
newnertg@gmail.com · github.com/NNEWNERR · nnewnerr.github.io · Samut Songkhram, Thailand (open to remote / hybrid / Bangkok)

### Summary

Built 358 automated tests across four systems with Playwright and TypeScript, covering E2E, API contract,
security rules, accessibility and visual regression, all running on 7 GitHub Actions workflows.
One year as a frontend developer on Angular/Ionic/Firebase means I can read the code under test and
tell whether a failure sits in the UI, the API or the permission rules before filing the bug.

### Test Automation Projects

**Krungthon Air — QA suite** *(live Firebase booking platform · private repo — my own shop)*
- Wrote 96 E2E and API tests across 36 spec files in Playwright + TypeScript, covering auth, booking,
  access control, concurrent double-booking, tenant isolation, accessibility and mobile layouts
- Wrote 90 Firestore security-rules tests on the emulator, running on every push; a review of the
  legacy ruleset failed 15 of them and caught over-broad permissions before they reached production
- Traced 53 test cases back to requirements with TC-IDs, making coverage gaps answerable rather than assumed
- Built 4 GitHub Actions workflows — a 17-way matrix on PRs, the rules suite on every push, Discord
  alerts, and a daily production soak that cuts regression detection to within 24 hours

**[multitenant-booking-qa](https://github.com/NNEWNERR/multitenant-booking-qa)** — Firestore Rules · Playwright · Vitest
- Tested one system at two layers with 93 tests — 76 security-rules tests plus 17 Playwright UI tests
  (desktop and Pixel 7), both against a real Firebase emulator rather than mocks
- Found 2 real bugs that the rules layer could not see: legacy documents invisible to the query although
  the rules allowed them, and a modal trapped under the topbar for 200 ms during its animation
- Designed a 24-case `public-boundary` suite proving the real authorization edge is "no organization yet",
  not "not logged in"
- Kept the repo runnable with `npm ci && npm test` and no credentials

**[qa-automation](https://github.com/NNEWNERR/qa-automation)** — Playwright · TypeScript · GitHub Actions
- Structured 63 tests into 8 Playwright projects by layer — API contract, UI, accessibility (axe-core),
  visual regression, smoke, and per-role auth via `storageState`
- Configured CI to run 4 parallel shards and merge the blob reports back into a single HTML report
- Tagged tests `@smoke` `@regression` `@a11y` `@visual` so a deploy can run one layer at a time
- Used Playwright Test Agents (planner → generator → healer) in anger: a 32-scenario plan became
  31 reviewed tests under a flake playbook, with every human correction recorded
- Set a repo rule that the healer may repair locators but may not change expected values, weaken
  assertions or add retries/timeouts — and tested that the rule actually holds

**[sauce-demo-tests](https://github.com/NNEWNERR/sauce-demo-tests)** — Playwright · TypeScript
- Wrote 16 tests across login, product sorting, cart and checkout with visual and accessibility checks
- Split 4 Page Objects over a shared `BasePage` so a selector change stays local to one page
- Wrote `TESTING.md`, a test strategy document with scope, a risk matrix and a test pyramid

### Technical Skills

- **Test automation** Playwright, TypeScript, Page Object Model, Selenium
- **API & data** Postman, REST contract testing, Firestore security rules, basic SQL
- **Specialised layers** accessibility (axe-core), visual regression, mobile viewports, concurrency
- **CI/CD** GitHub Actions (matrix, sharding, blob-report merge, scheduled soak), Firebase Emulator Suite
- **Test design** equivalence partitioning, boundary value analysis, decision tables,
  state transition, risk-based, negative testing
- **Developer background** Angular, Ionic, Tailwind CSS, JavaScript, Firebase, Git

### Work Experience

**Frontend Developer** — startup · 1 year
- Shipped features in Angular, Ionic and Tailwind CSS on a Firebase backend
- That year is where the testing edge comes from: having written the layer under test, I know which
  state fails to reset, where the races are, and that bugs cluster on the paths back out

**Event Organizer / Project Coordinator** — Nai Krit Sticker signage shop *(current)*
- Produce pre-event documentation, project close-out reports and survey data

### Education

**B.Eng. (Continuing Programme), Electronics Engineering Technology**
King Mongkut's University of Technology North Bangkok — College of Industrial Technology

---

## ที่มาของตัวเลข (ห้ามแก้ตัวเลขโดยไม่แก้ที่นี่ด้วย)

| ตัวเลข | ที่มา |
|---|---|
| 358 automated tests | 96 + 90 (Krungthon) + 93 (multitenant) + 63 (qa-automation) + 16 (sauce-demo) |
| 7 CI workflows | 4 ของ Krungthon + อีก 3 ในที่เหลือ |
| 10 Page Objects | รวมทุก repo (sauce-demo 4 บน BasePage) |
| 53 TC-ID / 90 rules tests / 15 เคสแดง | README หลักของโปรไฟล์ และ CS-04, CS-07 |
| บั๊กจริง 2 ตัวใน multitenant | CS-02-style legacy docs + CS-06 modal 200 ms |
| 32 scenario → 31 tests | Playwright Test Agents ใน qa-automation |

**ห้ามใส่ในเรซูเม่**
- Cypress — commit `9750bb7` ถอดออกเพราะไม่มีหลักฐานในพอร์ต ถ้าประกาศไหนขอ Cypress
  ให้เขียนว่า "Playwright/Selenium, ปรับไป Cypress ได้" ไม่ใช่เคลมว่าใช้เป็น
- คำว่าเคยดำรงตำแหน่ง QA มาก่อน — ทุกอย่างเล่าเป็นโปรเจกต์และงานจริงเท่านั้น
