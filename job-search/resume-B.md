# เรซูเม่เวอร์ชัน B — Software Tester / QA Analyst / นักทดสอบระบบ

> ฉบับกลาง (master) ห้ามส่งตรง ให้ fork แล้วปรับคีย์เวิร์ดตามประกาศทุกครั้ง
> ตัวเลขทุกตัวตรวจสอบกลับได้ ดูตาราง "ที่มาของตัวเลข" ใน resume-A.md
> อัปเดตล่าสุด 2026-10-28

ลำดับหัวข้อ: Summary › Test Design & QA Practice › Work Experience › Automation Toolkit › Education

**กฎประจำเวอร์ชัน B** — automation อยู่ท้ายเสมอ ในฐานะ "ทำได้ด้วย" ไม่ใช่จุดขาย
ทุกย่อหน้าต้องตอบคำถามเงียบ ๆ ของผู้จ้างว่า "คนนี้จะอยู่กับเราไหม" ได้ ไม่ใช่แค่ "คนนี้เก่งไหม"

---

## ฉบับภาษาไทย

**ศุภากร เศวตวงศ์สกุล (นิว)**
Software Tester / QA Analyst
newnertg@gmail.com · github.com/NNEWNERR · nnewnerr.github.io · สมุทรสงคราม (รับ remote / hybrid / กรุงเทพฯ)

### Summary

ออกแบบและรันเคสทดสอบกับระบบจองคิวที่มีผู้ใช้จริง สืบสาเหตุบั๊กที่ reproduce ยากจนถึงสาเหตุราก
และบันทึกไว้เป็น case study 8 เคส พื้นฐาน frontend developer 1 ปีทำให้คุยกับ dev ได้ตรงจุด
รู้ว่าอาการแบบไหนควรถามอะไรก่อน และเขียนบั๊กรีพอร์ตที่ dev หยิบไปแก้ได้โดยไม่ต้องเดินมาถาม

### Test Design & QA Practice

**การออกแบบเคสอย่างเป็นระบบ ไม่ใช่การไล่คลิก**
- ใช้ decision table ไล่คู่ผสม role × หน้าจอ ตอนระบบเพิ่ม role ใหม่หนึ่งตัว พบจุดที่พังเงียบ 6 จุด
  ที่การทดสอบตามเส้นทางหลักมองไม่เห็น
- ใช้ state-transition testing กับวงจรการจอง ไล่เส้นทางยกเลิกและปฏิเสธ พบที่นั่งค้างในระบบ 640 รายการ
  ทั้งที่งานถูกยกเลิกไปแล้ว พร้อมเสนอวิธีล้างแบบ idempotent ที่รันซ้ำได้ไม่พัง
- ใช้ negative testing กับการแยกข้อมูลระหว่างองค์กร ทดสอบ 3 ชั้นและพบบั๊กครบทั้ง 3 ชั้น
  โดยเคสส่วนใหญ่คือ "สิ่งที่ต้องถูกปฏิเสธ" ไม่ใช่ "สิ่งที่ต้องทำได้"
- ใช้ equivalence partitioning และ boundary value analysis กับฟอร์มและช่วงเวลาจอง
  บันทึกกำกับไว้ทุกเทสว่าเลือกเทคนิคไหนและเพราะอะไร

**การสืบสาเหตุและการเขียนบั๊กรีพอร์ต**
- เขียน [case study 8 เคส](https://github.com/NNEWNERR/new.supakorn/tree/main/case-studies) จากบั๊กในระบบที่ใช้งานจริง
  เรียงเป็นอาการ → วิธีตามรอย → สาเหตุราก → การแก้ → การยืนยัน → บทเรียน
- แยก "เทสไม่นิ่ง" ออกจาก "ระบบไม่นิ่ง" ก่อนเสมอ — เคส login ล้มแบบสุ่มสืบจนพบว่าเป็น
  race condition ของ session สองเส้นในระบบจริง ไม่ใช่ความไม่เสถียรของเทส
- เคสหนึ่งเทสฟ้องว่า "จองซ้อนได้" ตัด UI ทิ้งแล้วยิง API ตรงเพื่อพิสูจน์ที่ระบบก่อน
  ผลคือระบบถูก และบั๊กอยู่ในเทสเอง 4 ชั้น — รายงานออกไปตามนั้น
- ยืนยันด้วยสิ่งที่วัดได้เสมอ — HTTP header ที่ตอบกลับมา, element ที่รับคลิกจริงจาก hit-testing,
  ผลลัพธ์ที่ต้องถูกปฏิเสธ ไม่ใช่ "ลองแล้วดูเหมือนจะหาย"

**การทำงานกับทีม dev**
- เขียนรายงานให้ dev ทำซ้ำได้ด้วยตัวเอง ระบุขอบเขตที่กระทบจริง และแนบข้อเสนอว่า
  แก้อย่างไรไม่ให้กลับมาอีก ไม่ใช่แค่ชี้ว่าตรงไหนผิด
- อ้างอิง test case 53 รายการกลับไปที่ความต้องการด้วย TC-ID ทำให้ตอบได้ว่าข้อไหนมีเทสคุ้มแล้ว

### Work Experience

**Frontend Developer** — สตาร์ทอัพ · 1 ปี
- พัฒนาและส่งมอบฟีเจอร์ด้วย Angular, Ionic และ Tailwind CSS บน backend ที่เป็น Firebase
- ทำงานในรอบ SDLC เต็มรอบตั้งแต่รับ requirement จนขึ้น production
  จึงรู้ว่าบั๊กมักเกิดตอนไหนของรอบ และ dev ต้องการข้อมูลอะไรในตั๋วถึงจะเริ่มแก้ได้ทันที

**Event Organizer / Project Coordinator** — ร้านป้ายนายกฤษสติ๊กเกอร์ *(ปัจจุบัน)*
- จัดทำเอกสารก่อนงาน รายงานสรุปโปรเจกต์ และดูแลข้อมูลแบบสำรวจ
- ดูแลระบบจองคิวของร้านเองตั้งแต่ความต้องการจนถึงการทดสอบก่อนปล่อยให้ลูกค้าใช้

### Automation Toolkit *(ทำได้ด้วย ใช้เมื่องานเริ่มซ้ำจนคุ้มที่จะเขียน)*

- Playwright + TypeScript — ชุดเทสอัตโนมัติรวม 358 เคสใน 4 ระบบ ใช้ Page Object Model
- GitHub Actions — 7 workflow รวม daily soak ที่ยิง production ทุกวันเพื่อจับ regression ภายใน 24 ชั่วโมง
- Postman / REST contract testing, Firestore security rules บน emulator, axe-core, Selenium
- ใช้เป็นเครื่องมือขยายกำลังของการทดสอบด้วยมือ ไม่ใช่สิ่งที่จะมาแทน —
  เคสที่ยังไม่นิ่งหรือรันปีละครั้งยังคุ้มกว่าถ้าทดสอบด้วยมือ

### Education

**วศ.บ. (ต่อเนื่อง) เทคโนโลยีวิศวกรรมอิเล็กทรอนิกส์**
มหาวิทยาลัยเทคโนโลยีพระจอมเกล้าพระนครเหนือ — วิทยาลัยเทคโนโลยีอุตสาหกรรม

---

## English version

**Supakorn Sawetwongsakul (New)**
Software Tester / QA Analyst
newnertg@gmail.com · github.com/NNEWNERR · nnewnerr.github.io · Samut Songkhram, Thailand (open to remote / hybrid / Bangkok)

### Summary

I design and run test cases against a live booking system, chase hard-to-reproduce bugs down to root
cause, and write them up — eight case studies so far. A year as a frontend developer means I ask
developers the right question first and write bug reports they can act on without coming back to me.

### Test Design & QA Practice

**Systematic case design, not click-and-hope**
- Used a decision table over role × screen when the system gained a single new role, and found
  6 silent failures that happy-path testing had missed
- Applied state-transition testing to the booking lifecycle, walking the cancel and reject paths;
  found 640 seats still held after their events were cancelled, and proposed an idempotent cleanup
- Applied negative testing to cross-organization data isolation across three layers and found a bug in
  each — most cases assert what **must be refused**, not what must work
- Applied equivalence partitioning and boundary value analysis to forms and booking time windows,
  recording for each test which technique was chosen and why

**Investigation and bug reporting**
- Wrote [8 case studies](https://github.com/NNEWNERR/new.supakorn/tree/main/case-studies) from bugs in a live
  system, each as symptom → trail → root cause → fix → verification → lesson
- Always separate "the test is unstable" from "the system is unstable" first — an intermittent login
  failure turned out to be a genuine race between two session paths, not test flake
- When a test reported double-booking, I dropped the UI and hit the API directly to test the system
  first: the system was right and the bug was four layers deep in the test. The report said so
- Verify with something measurable — the response header, the element that actually receives the click
  from hit-testing, the operation that must be refused — never "I retried and it seems fine now"

**Working with developers**
- Write reports a developer can reproduce unaided, state the real blast radius, and include a proposal
  for keeping the bug from returning rather than only pointing at the defect
- Traced 53 test cases back to requirements with TC-IDs, so coverage questions have answers

### Work Experience

**Frontend Developer** — startup · 1 year
- Shipped features in Angular, Ionic and Tailwind CSS on a Firebase backend
- Worked the full SDLC from requirement to production, so I know where in the cycle bugs enter and
  what a ticket needs to contain before a developer can start on it

**Event Organizer / Project Coordinator** — Nai Krit Sticker signage shop *(current)*
- Produce pre-event documentation, project close-out reports and survey data
- Own the shop's own booking system from requirements through pre-release testing

### Automation Toolkit *(available when a task repeats often enough to be worth scripting)*

- Playwright + TypeScript — 358 automated tests across four systems, built on the Page Object Model
- GitHub Actions — 7 workflows, including a daily production soak that catches regressions within 24 hours
- Postman / REST contract testing, Firestore security rules on the emulator, axe-core, Selenium
- I treat automation as leverage for manual testing, not a replacement: a case that is still in flux,
  or runs once a year, is cheaper to run by hand

### Education

**B.Eng. (Continuing Programme), Electronics Engineering Technology**
King Mongkut's University of Technology North Bangkok — College of Industrial Technology

---

## กันตกม้าตายตอนสัมภาษณ์เวอร์ชัน B

**"มีพอร์ต automation แล้วทำไมมาสมัคร manual"** — คำตอบที่ใช้ได้ ห้ามให้ฟังเหมือนทางผ่าน

> ผมเขียน automation มาจากฝั่งที่ไม่มีใครบอกว่าต้องทดสอบอะไร ผมเป็นคนตัดสินใจเองทั้งหมด
> และนั่นคือจุดอ่อนของผม — ผมไม่เคยทดสอบระบบที่คนอื่นเขียน ไม่เคยเถียงกับ PO เรื่องขอบเขต
> ไม่เคยรับ requirement ที่กำกวมมาแปลงเป็นเคส งาน tester คือที่ที่ได้ฝึกเรื่องพวกนี้จริง
> ส่วน automation ที่ติดตัวมาจะทำให้ผมเริ่มช่วยทีมเรื่องนั้นได้เร็วขึ้นเมื่อถึงเวลา ไม่ใช่เหตุผลที่ผมจะรีบไป

**กันภาพ overqualified** — ในเวอร์ชัน B ห้ามเขียนว่าเป้าหมายคือ SDET, ห้ามขึ้นต้น summary ด้วยจำนวนเทส,
และให้ automation อยู่ท้ายเสมอ ถ้าถามตรง ๆ ว่าอยากไป automation ไหม ตอบตามจริงว่าอยาก
แต่ผูกกับ "ที่นี่" เช่น อยากช่วยทีมตั้งชุด regression เมื่อเข้าใจระบบพอแล้ว
