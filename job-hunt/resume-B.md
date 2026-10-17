# เรซูเม่เวอร์ชัน B — Software Tester / QA Analyst (ตำแหน่งสะพาน)

> เวอร์ชันกลาง (master) สำหรับระดับ B — เป้าหมายคือทำให้คำว่า QA เข้าไปอยู่ในเรซูเม่ แล้วขยับเป็น automation ภายใน 1-2 ปี
> ลำดับหัวข้อ: Summary > Test Design & QA Practice > Work Experience > Automation Toolkit > Education
> กติกาคุมโทน: automation อยู่ท้ายในฐานะ "ทำได้ด้วย" ห้ามเล่าเป็นจุดขายหลัก และห้ามโชว์ตัวเลข 358 เทสใน Summary
> (เหตุผล: ถ้าดู overqualified บริษัทจะกลัวว่าจ้างแล้วลาออกภายในหกเดือน)

---

## ฉบับภาษาไทย (1 หน้า)

**ศุภากร เศวตวงศ์สกุล (นิว)**
Software Tester / QA Analyst
newnertg@gmail.com · github.com/NNEWNERR · nnewnerr.github.io · นครปฐม · รับ remote / hybrid / กรุงเทพฯ

### Summary
- ออกแบบเทสเคสด้วยเทคนิคที่ระบุชื่อได้ — equivalence partitioning, boundary value analysis, decision table, state transition และ risk-based testing ไม่ใช่การไล่คลิกแล้วบันทึก
- สืบสาเหตุรากของบั๊กและเขียนรายงานที่ dev เอาไปแก้ได้ทันที มี **case study 8 เคส** จากระบบที่ใช้งานจริง เล่าตั้งแต่อาการจนถึงสาเหตุราก
- มาจากฝั่ง dev (frontend 1 ปี) จึงคุยกับ dev ด้วยภาษาเดียวกัน ถามคำถามที่ตรงจุด และประเมินได้ว่าบั๊กน่าจะอยู่ชั้นไหนของระบบ

### Test Design & QA Practice
**การออกแบบเทสเคส**
- แบ่ง equivalence class ของสิทธิ์การเข้าถึงจนได้ชุดเทส **24 เคส** ที่พิสูจน์ว่าเส้นแบ่งสิทธิ์จริงของระบบคือ "ยังไม่มีสังกัด" ไม่ใช่ "ยังไม่ล็อกอิน" — เงื่อนไขที่สเปกเดิมเขียนไว้คลาดกัน
- ทำ **traceability ด้วย TC-ID 53 เคส** บนระบบจองคิวที่ใช้งานจริง ให้ผลเทสแต่ละรอบอ้างกลับไปที่ test case ได้ตรงเคส
- ออกแบบเคสครอบคลุมทั้ง **positive, negative และเคสที่ต้องถูกปฏิเสธ** — ทดสอบ 90 เงื่อนไขของกฎความปลอดภัยว่าปฏิเสธจริงตามที่ออกแบบ

**การหาบั๊กและรายงานบั๊ก**
- เขียน **case study 8 เคส** จากบั๊กจริงบนระบบที่ใช้งานอยู่ ไล่จากอาการ → ขั้นตอนทำซ้ำ → สาเหตุราก → วิธีป้องกันไม่ให้หลุดอีก
- จับบั๊กที่เครื่องมืออัตโนมัติมองไม่เห็นด้วยตัวเอง 2 ตัว: เอกสารรุ่นเก่าที่ query มองไม่เห็นแม้สิทธิ์อนุญาต และปุ่มบนมือถือที่กดไม่ได้ช่วง 200 ms ของ animation
- แยกได้ว่าอาการไหนเป็นบั๊กของระบบ และอาการไหนเป็นปัญหาสภาพแวดล้อมของชุดเทสเอง (มีเคสที่สรุปว่า "เทสโทษระบบผิด" บันทึกไว้เป็นเคสหนึ่ง)

**การทำงานกับทีม**
- เขียน **เอกสารกลยุทธ์การทดสอบ** ที่มีขอบเขต, risk matrix และ test pyramid ใช้ตกลงกับทีมว่าจะทดสอบอะไรก่อน
- ตั้งกติกาว่าเทสที่ dependency ไม่พร้อมให้ **skip แทนที่จะ fail** เพื่อให้ "จอแดง" หมายถึงบั๊กจริงเสมอ — ลดการเสียเวลาไล่ปัญหาที่ไม่ใช่บั๊ก
- บันทึก flake จากระบบภายนอกไว้ให้ชัดแทนการกลบด้วย retry เพราะ retry ที่ใส่เพื่อให้ผ่านจะบังบั๊กจริงในเทสตัวเดียวกัน

### Work Experience
**Frontend Developer** — สตาร์ทอัพ · 1 ปี
- พัฒนาและส่งมอบฟีเจอร์ด้วย Angular, Ionic, Tailwind CSS บน backend Firebase
- ได้เห็นวงจร SDLC จากฝั่งคนเขียนโค้ด — รู้ว่าบั๊กมักเกิดที่รอยต่อไหน และรู้ว่า dev ต้องได้ข้อมูลอะไรจึงจะแก้ได้เลยโดยไม่ต้องถามกลับ

**Event Organizer / Project Coordinator** — ร้านนายกิจสติ๊กเกอร์ · ปัจจุบัน
- จัดทำเอกสารก่อนงาน, รายงานสรุปโปรเจกต์ และดูแลข้อมูลแบบสำรวจ — งานที่ต้องตรวจความถูกต้องของข้อมูลเป็นรอบ ๆ และสื่อสารกับหลายฝ่าย

### Automation Toolkit
ทำได้ด้วย ไม่ใช่งานหลักที่ขอ แต่ช่วยลดงานซ้ำของทีมได้ตั้งแต่เดือนแรก
- **Playwright + TypeScript** — เขียน E2E และ API test พร้อม Page Object Model, ดูแลชุดเทสของตัวเองบน GitHub Actions
- **Cypress, Selenium, Postman** — ใช้ได้ในระดับเขียนและแก้ชุดเทสที่มีอยู่
- พอร์ตโฟลิโอโค้ดเปิดให้ดูได้ที่ github.com/NNEWNERR และ nnewnerr.github.io

### Education
**วศ.บ. (ต่อเนื่อง) เทคโนโลยีวิศวกรรมอิเล็กทรอนิกส์** — มหาวิทยาลัยเทคโนโลยีพระจอมเกล้าพระนครเหนือ วิทยาลัยเทคโนโลยีอุตสาหกรรม

---

## English version (1 page)

**Supakorn Sawetwongsakul (New)**
Software Tester / QA Analyst
newnertg@gmail.com · github.com/NNEWNERR · nnewnerr.github.io · Nakhon Pathom, Thailand · Open to remote / hybrid / Bangkok

### Summary
- Design test cases with named techniques — equivalence partitioning, boundary value analysis, decision tables, state transition and risk-based testing — rather than clicking through and recording what happened
- Root-cause defects and write reports a developer can act on immediately; **8 written case studies** from live systems trace each one from symptom to root cause
- Came from the development side (1 year frontend), so I speak the developers' language, ask the questions that narrow a bug down, and can judge which layer it probably lives in

### Test Design & QA Practice
**Test case design**
- Partitioned access-control equivalence classes into a **24-case suite** proving the system's real permission boundary is "no tenant assigned", not "not signed in" — a condition the original spec stated incorrectly
- Maintained **TC-ID traceability for 53 cases** on a live queue-booking system, so each test run maps results back to specific written cases
- Cover positive, negative and **must-be-denied** cases — 90 security-rule conditions verified to reject exactly as designed

**Finding and reporting defects**
- Wrote **8 case studies** on real defects in production systems: symptom → reproduction steps → root cause → how to stop it recurring
- Found 2 defects by hand that tooling missed: legacy documents invisible to queries despite permissions allowing them, and a mobile button unclickable during a 200 ms animation window
- Distinguish genuine product defects from test-environment problems — one case study documents a suite that blamed the system incorrectly

**Working with the team**
- Authored a **test strategy document** with scope, risk matrix and test pyramid, used to agree with the team on what gets tested first
- Established that tests with unavailable dependencies **skip rather than fail**, so a red run always means a real defect — less time spent chasing non-bugs
- Record external flakiness explicitly instead of masking it with retries, because a retry added to get green hides real defects in the same test

### Work Experience
**Frontend Developer** — startup · 1 year
- Shipped features in Angular, Ionic and Tailwind CSS on a Firebase backend
- Saw the SDLC from the developer's side — which seams break, and what information a developer needs to fix a bug without asking follow-up questions

**Event Organizer / Project Coordinator** — Naikit Sticker · current
- Prepare pre-event documentation and project reports and maintain survey data — work that requires repeated data-accuracy checks and coordination across parties

### Automation Toolkit
Available if useful, not the main ask — but it removes repetitive work from the team from month one
- **Playwright + TypeScript** — E2E and API tests with the Page Object Model, maintained in GitHub Actions
- **Cypress, Selenium, Postman** — able to write and maintain existing suites
- Code portfolio open at github.com/NNEWNERR and nnewnerr.github.io

### Education
**B.Eng. (continuing programme), Electronics Engineering Technology** — King Mongkut's University of Technology North Bangkok, College of Industrial Technology
