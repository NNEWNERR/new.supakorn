# เรซูเม่เวอร์ชัน A — Automation QA Engineer / SDET

ฉบับกลาง ใช้เป็นต้นแบบก่อนปรับรายประกาศ
ลำดับหัวข้อ: Summary → Test Automation Projects → Technical Skills → Work Experience → Education

ตัวเลขทุกตัวในไฟล์นี้มาจาก `README.md` และ `case-studies/` ของรีโปนี้ ไม่มีการปัดขึ้น

---

## ภาษาไทย

**ศุภากร เศวตวงศ์สกุล (นิว)**
Automation QA Engineer — Playwright + TypeScript
newnertg@gmail.com · github.com/NNEWNERR · nnewnerr.github.io
สมุทรสงคราม — รับ remote / hybrid / กรุงเทพฯ

### Summary

เขียน end-to-end และ API test automation ด้วย Playwright + TypeScript รวม **358 automated tests ใน 4 repo**
ที่เป็นเจ้าของทั้ง stack — ตัวแอป, security rules และเทสทั้งสองชั้น ดูแล **CI 7 workflow บน GitHub Actions**
ที่รันจริงทุก push/PR รวมถึง daily soak ที่ยิงกับ production ทุกวัน ก่อนหน้านี้เป็น frontend developer 1 ปี
(Angular / Ionic / Firebase) จึงอ่านโค้ดที่กำลังทดสอบได้ และรู้ว่าบั๊กมักเกิดตรงรอยต่อไหน

### Test Automation Projects

- ออกแบบและเขียน QA suite ของแพลตฟอร์มจองคิวบน Firebase ที่เปิดใช้งานจริง — **96 E2E/API tests ใน 36 spec files
  + 90 Firestore security-rules tests** ครอบคลุม auth, การจอง, สิทธิ์การเข้าถึง, การจองชนกันแบบ concurrent,
  การแยกข้อมูลระหว่าง tenant, a11y และ mobile responsive โดยมี **53 test case ที่อ้างอิงกลับด้วย TC-ID**
- วาง **CI 4 workflow** ให้ suite เดียวกัน — matrix 17 ชุดตอน PR, ชุด rules 90 เคสบน emulator ทุก push,
  แจ้งเตือนเข้า Discord และ **daily soak ยิง production ทุกวัน** ทำให้จับ regression ได้ภายใน 24 ชั่วโมง
  แทนที่จะรอ PR ถัดไป
- เขียนเทสสองชั้นของระบบ multi-tenant เดียวกันใน `multitenant-booking-qa` — **76 rules tests + 17 Playwright
  UI tests** (desktop + Pixel 7) รันกับ Firebase emulator จริงทั้งคู่ ไม่ใช่ mock, `npm ci && npm test` จบ
  ไม่ต้องมี credential
- การเขียน UI test ชุดนั้น **เจอบั๊กจริง 2 ตัว**: เอกสารรุ่นเก่าที่ query มองไม่เห็นทั้งที่ rules อนุญาต
  และ modal ที่ถูกขังใต้ topbar 200 ms ระหว่าง animation
- พิสูจน์เส้นแบ่งสิทธิ์ด้วยชุด `public-boundary` **24 เคส** ว่าเงื่อนไขจริงคือ "ยังไม่มีสังกัด"
  ไม่ใช่ "ยังไม่ล็อกอิน" ซึ่งเป็นสมมติฐานที่ทีมเข้าใจผิดกันบ่อย
- แยก **63 tests เป็น 8 Playwright projects** ใน `qa-automation` — API contract, UI, accessibility (axe-core),
  visual regression, smoke และ auth แยกตาม role ด้วย `storageState`; CI รัน **4 shard ขนาน** แล้ว merge
  blob report กลับเป็นรายงาน HTML ฉบับเดียว เทสติด tag (`@smoke` `@regression` `@a11y` `@visual`)
  เลือกรันทีละชั้นได้
- ใช้ **Playwright Test Agents** (planner → generator → healer) กับ suite จริง: แผน **32 scenario → 31 เทส**
  ที่ generator สร้างและผ่านการรีวิวตาม flake playbook พร้อมบันทึกว่ามนุษย์แก้อะไร และตั้งกติกาประจำ repo
  ว่า healer ซ่อม locator ได้ แต่ห้ามแก้ค่าที่คาดหวัง ลด assertion หรือเพิ่ม retry/timeout — ทดสอบแล้วว่ามันทำตาม
- เขียน **4 Page Object บน BasePage ร่วมกัน** ใน `sauce-demo-tests` ครอบคลุม login, การเรียงสินค้า, ตะกร้า
  และ checkout รวม **16 tests** พร้อม visual + accessibility check และเอกสาร `TESTING.md` ที่มีขอบเขต,
  risk matrix และ test pyramid
- เขียน **case study 8 เคส** จากบั๊กจริงในระบบที่ใช้งานอยู่ ไล่ตั้งแต่อาการถึงสาเหตุราก เพื่ออธิบายงาน
  ในส่วนที่ repo เป็น private ได้

### Technical Skills

- **Automation:** Playwright (TypeScript), Page Object Model, API testing, Firebase Emulator, Vitest, Selenium, Postman
- **CI/CD:** GitHub Actions — matrix, sharding, blob report merge, scheduled soak, Discord notification
- **Test practice:** test strategy document, TC-ID traceability, risk matrix, EP/BVA, decision table,
  state transition, flake triage
- **Development:** Angular, Ionic, TypeScript/JavaScript, Tailwind CSS, Firebase/Firestore, Git

### Work Experience

**Frontend Developer** — สตาร์ทอัพ · 1 ปี
พัฒนาและส่งมอบฟีเจอร์ด้วย Angular, Ionic และ Tailwind CSS บน backend ที่เป็น Firebase
เป็นช่วงที่เห็นกับตาว่าแอปพังด้วยสาเหตุอะไร ซึ่งกลายเป็นฐานของวิธีออกแบบเทสตอนนี้ —
เข้าใจสิ่งที่ทดสอบเพราะเคยเขียนมันมาก่อน

**Event Organizer / Project Coordinator** — ร้านป้ายนายกฤษสติ๊กเกอร์ · ปัจจุบัน
จัดทำเอกสารก่อนงาน, รายงานสรุปโปรเจกต์ และดูแลข้อมูลแบบสำรวจ

### Education

วศ.บ. (ต่อเนื่อง) เทคโนโลยีวิศวกรรมอิเล็กทรอนิกส์
มหาวิทยาลัยเทคโนโลยีพระจอมเกล้าพระนครเหนือ — วิทยาลัยเทคโนโลยีอุตสาหกรรม

---

## English

**Supakorn Sawetwongsakul (New)**
Automation QA Engineer — Playwright + TypeScript
newnertg@gmail.com · github.com/NNEWNERR · nnewnerr.github.io
Samut Songkhram, Thailand — open to remote / hybrid / Bangkok

### Summary

I write end-to-end and API test automation in Playwright + TypeScript — **358 automated tests across 4 repos**
where I own the whole stack: the app, its security rules, and both layers of tests. I keep **7 GitHub Actions
workflows** running on every push and PR, including a daily soak against production. Before QA I spent a year
as a frontend developer (Angular / Ionic / Firebase), so I can read the code under test and I know which seams
break first.

### Test Automation Projects

- Designed and built the QA suite for a live Firebase queue-booking platform — **96 E2E/API tests across
  36 spec files plus 90 Firestore security-rules tests** covering auth, booking, access control, concurrent
  double-booking, tenant isolation, a11y and mobile responsiveness, with **53 test cases traced back by TC-ID**
- Built **4 CI workflows** for that suite: a 17-way matrix on PRs, the 90-case rules suite on an emulator on
  every push, Discord alerts, and a **daily production soak** that catches regressions within 24 hours instead
  of waiting for the next PR
- Wrote two layers of tests for the same multi-tenant system in `multitenant-booking-qa` — **76 rules tests
  plus 17 Playwright UI tests** (desktop + Pixel 7), both against a real Firebase emulator rather than mocks;
  `npm ci && npm test` runs the lot with no credentials
- Writing that UI layer **surfaced 2 real bugs**: legacy documents the query could not see even though the
  rules allowed them, and a modal trapped under the topbar for 200 ms during its animation
- Proved the real permission boundary with a **24-case `public-boundary` suite**: the line is "no tenant yet",
  not "not logged in" — the assumption the team had been making
- Split **63 tests into 8 Playwright projects** in `qa-automation` — API contract, UI, accessibility (axe-core),
  visual regression, smoke, and per-role auth via `storageState`; CI runs **4 parallel shards** and merges the
  blob reports into a single HTML report, with tags (`@smoke` `@regression` `@a11y` `@visual`) to run one layer
  at a time
- Used **Playwright Test Agents** (planner → generator → healer) on a real suite: a **32-scenario plan → 31
  generated tests** reviewed against a flake playbook with every human edit recorded, under a repo rule that
  the healer may repair locators but must not change expected values, weaken assertions, or add retries and
  timeouts — and I verified it holds to that
- Built **4 Page Objects on a shared BasePage** in `sauce-demo-tests` covering login, sorting, cart and
  checkout in **16 tests** with visual and accessibility checks, plus a `TESTING.md` strategy document with
  scope, risk matrix and test pyramid
- Wrote **8 case studies** of real bugs from systems in use, symptom through root cause, so I can walk through
  work whose repo stays private

### Technical Skills

- **Automation:** Playwright (TypeScript), Page Object Model, API testing, Firebase Emulator, Vitest, Selenium, Postman
- **CI/CD:** GitHub Actions — matrix, sharding, blob report merge, scheduled soak, Discord notifications
- **Test practice:** test strategy documents, TC-ID traceability, risk matrices, EP/BVA, decision tables,
  state transition, flake triage
- **Development:** Angular, Ionic, TypeScript/JavaScript, Tailwind CSS, Firebase/Firestore, Git

### Work Experience

**Frontend Developer** — startup · 1 year
Built and shipped features in Angular, Ionic and Tailwind CSS on a Firebase backend. This is where I saw
first-hand what makes an app break, and it underpins how I design tests now — I understand what I am testing
because I used to write it.

**Event Organizer / Project Coordinator** — Nai Krit Sticker signage shop · current
Pre-event documentation, project wrap-up reports, and survey data handling.

### Education

B.Eng. (continuing programme), Electronics Engineering Technology
King Mongkut's University of Technology North Bangkok — College of Industrial Technology

---

## ถ้าต้องบีบให้เหลือ 1 หน้า ตัดบรรทัดไหน

ฉบับนี้ยาวเกิน 1 หน้าอยู่ประมาณ 4 บรรทัด ลำดับการตัด:

1. **ตัดบูลเล็ต `public-boundary` 24 เคส** — เป็นรายละเอียดที่ซ้อนอยู่ใน repo เดียวกับบูลเล็ต 76+17 tests
   อยู่แล้ว เก็บไว้เล่าตอนสัมภาษณ์ได้เต็มกว่า
2. **ตัดบูลเล็ต case study 8 เคส** — ย้ายไปเป็นลิงก์เดียวใต้ชื่อแทน ไม่เสียน้ำหนัก
3. **ย่อ Event Organizer เหลือบรรทัดเดียว** — ไม่เกี่ยวกับ QA แต่ต้องคงไว้เพื่อไม่ให้ timeline มีช่องว่าง
4. **ถ้ายังเกิน** รวมบูลเล็ต Krungthon Air สองตัว (suite + CI) เป็นตัวเดียว โดยคงเลข 96/90/53/17 ไว้ทั้งหมด

ห้ามตัด: ตัวเลขรวม 358 tests, บูลเล็ตบั๊กจริง 2 ตัว, และบรรทัดกติกา healer — สามอย่างนี้คือสิ่งที่
แยกพอร์ตนี้ออกจากพอร์ตที่ทำตาม tutorial

## จุดอ่อนที่แก้ด้วยการเขียนไม่ได้

- **ยังไม่เคยมีตำแหน่ง QA อย่างเป็นทางการ** — เรซูเม่นี้เลยไม่เคลมว่าเคยเป็น QA เลย
  ทุกอย่างเล่าเป็นโปรเจกต์ที่เป็นเจ้าของและงาน dev จริง
- **ไม่มี Appium / mobile native automation** — Pixel 7 ในพอร์ตคือ Playwright device emulation ไม่ใช่ของเดียวกัน
- **ไม่มี Robot Framework** ซึ่งธนาคารไทยถามบ่อย
- **ไม่มีประสบการณ์ในทีม QA ที่มีคนอื่น** — ยังไม่เคยรีวิวเทสของคนอื่นหรือรับ handover จาก manual tester
