# เรซูเม่เวอร์ชัน B — Software Tester / QA Analyst

ฉบับกลาง สำหรับตำแหน่งสะพาน
ลำดับหัวข้อ: Summary → Test Design & QA Practice → Work Experience → Automation Toolkit → Education

หลักการของเวอร์ชันนี้: ขายวิธีคิดแบบ tester ก่อน automation วางไว้ท้ายในฐานะ "ทำได้ด้วย"
และ **ต้องไม่ดู overqualified** จนบริษัทคิดว่าจะอยู่ไม่ถึงหกเดือน — จึงเล่า automation
เป็นเครื่องมือที่เอามาช่วยทีม ไม่ใช่เหตุผลที่ควรข้ามขั้น

---

## ภาษาไทย

**ศุภากร เศวตวงศ์สกุล (นิว)**
Software Tester / QA Analyst
newnertg@gmail.com · github.com/NNEWNERR
สมุทรสงคราม — รับ remote / hybrid / กรุงเทพฯ

### Summary

ทดสอบระบบที่เปิดใช้งานจริงด้วยการออกแบบเคสเป็นหลัก ไม่ใช่การกดไปเรื่อย ๆ — ออกแบบและไล่เทส
แพลตฟอร์มจองคิวที่มีผู้ใช้จริง ตั้งแต่ auth, การจอง, สิทธิ์การเข้าถึง ไปจนถึงเคสที่คนจองชนกัน
และเขียน **case study 8 เคสจากบั๊กจริง** ไล่จากอาการถึงสาเหตุราก มาจากสาย frontend developer 1 ปี
จึงคุยกับ dev ด้วยภาษาเดียวกัน รู้ว่าควรแนบอะไรในบั๊กรีพอร์ตให้แก้ได้เลย และถามอะไรก่อนตอน requirement ยังคลุมเครือ

### Test Design & QA Practice

- ออกแบบชุดเทส **53 test case ที่อ้างอิงกลับด้วย TC-ID** สำหรับแพลตฟอร์มจองคิวที่ใช้งานจริง
  ครอบคลุม auth, การจอง, สิทธิ์ตาม role, การจองชนกันแบบ concurrent, การแยกข้อมูลระหว่างลูกค้าแต่ละราย,
  a11y และการใช้งานบนมือถือ
- ใช้เทคนิคออกแบบเคสแบบระบุเหตุผลได้ — **equivalence partitioning, boundary value analysis, decision table
  และ state transition** โดยใน repo `qa-automation` ทุกเทสมีคอลัมน์กำกับว่าใช้เทคนิคอะไรและเพราะอะไร
- เขียนเอกสารกลยุทธ์การทดสอบ `TESTING.md` ที่ระบุขอบเขต **risk matrix** และ test pyramid —
  ใช้จัดลำดับว่าเคสไหนต้องมีก่อน ไม่ใช่เขียนเคสตามลำดับหน้าจอ
- เขียน **case study 8 เคส** จากบั๊กในระบบที่เปิดใช้งานอยู่ แต่ละเคสมีอาการ ขั้นตอนทำซ้ำ และสาเหตุราก
  เช่น เอกสารรุ่นเก่าที่ระบบมองไม่เห็นทั้งที่สิทธิ์อนุญาต และปุ่มที่กดไม่ได้เฉพาะบนมือถือ
  เพราะ modal ถูกขังใต้ topbar 200 ms ระหว่าง animation
- หาเส้นแบ่งสิทธิ์ที่แท้จริงของระบบด้วยการไล่เคส **24 เคส** แล้วพบว่าเงื่อนไขจริงคือ "ผู้ใช้ยังไม่มีสังกัด"
  ไม่ใช่ "ผู้ใช้ยังไม่ล็อกอิน" ตามที่เข้าใจกันไว้ก่อน — เป็นเคสที่ถ้าไม่แยกตัวแปรจะมองไม่เห็น
- แยก **บั๊กของระบบกับเทสที่เขียนผิดเอง** ให้ได้ก่อนยื่นให้ dev — มี 1 เคสที่เทสฟ้องว่าระบบพัง
  แต่ไล่แล้วพบว่าเทสเองผิด จึงบันทึกไว้เป็น case study เพื่อไม่ให้ทีมเสียเวลากับ false alarm ซ้ำ
- ถือหลักว่าเทสที่ **skip แทนที่จะ fail** เมื่อ dependency ไม่พร้อม ดีกว่าเทสที่แดงเพราะสภาพแวดล้อม —
  เพื่อให้ "จอแดง" หมายถึงบั๊กจริงเสมอ และ flake จากระบบภายนอกต้องบันทึกไว้ให้ชัด ไม่กลบด้วย retry

### Work Experience

**Frontend Developer** — สตาร์ทอัพ · 1 ปี
พัฒนาและส่งมอบฟีเจอร์ด้วย Angular, Ionic และ Tailwind CSS บน Firebase
ได้เห็นวงจรตั้งแต่ requirement ถึง production จึงรู้ว่าบั๊กมักเกิดตรงรอยต่อไหน และบั๊กรีพอร์ตแบบไหน
ที่ dev เอาไปแก้ได้ทันทีโดยไม่ต้องถามกลับ

**Event Organizer / Project Coordinator** — ร้านป้ายนายกฤษสติ๊กเกอร์ · ปัจจุบัน
จัดทำเอกสารก่อนงาน, รายงานสรุปโปรเจกต์ และดูแลข้อมูลแบบสำรวจ — งานที่ต้องเก็บรายละเอียดให้ครบ
และสื่อสารกับหลายฝ่ายให้ตรงกัน

### Automation Toolkit

ทำได้ด้วย และยินดีใช้ช่วยทีมเท่าที่งานต้องการ: Playwright + TypeScript (Page Object Model),
API testing, Firebase Emulator, Selenium, Postman และ CI บน GitHub Actions
พอร์ตรวม **358 automated tests ใน 4 repo** — เขียนไว้เพื่อให้ regression ที่ต้องกดซ้ำทุกรอบ
กลายเป็นงานที่รันเองได้ ไม่ใช่เพื่อแทนการออกแบบเคส

### Education

วศ.บ. (ต่อเนื่อง) เทคโนโลยีวิศวกรรมอิเล็กทรอนิกส์
มหาวิทยาลัยเทคโนโลยีพระจอมเกล้าพระนครเหนือ — วิทยาลัยเทคโนโลยีอุตสาหกรรม

---

## English

**Supakorn Sawetwongsakul (New)**
Software Tester / QA Analyst
newnertg@gmail.com · github.com/NNEWNERR
Samut Songkhram, Thailand — open to remote / hybrid / Bangkok

### Summary

I test live systems by designing cases, not by clicking around. I designed and ran the test coverage for a
queue-booking platform with real users — auth, booking, access control, and the cases where two people book
the same slot — and wrote **8 case studies of real bugs** from symptom through root cause. A year as a frontend
developer means I speak the same language as the devs: I know what to attach to a bug report so it can be fixed
without a round trip, and what to ask first when a requirement is still vague.

### Test Design & QA Practice

- Designed **53 TC-ID-traced test cases** for a live queue-booking platform, covering auth, booking,
  role-based permissions, concurrent double-booking, per-customer data isolation, accessibility and mobile use
- Apply test design techniques I can justify — **equivalence partitioning, boundary value analysis, decision
  tables and state transition**; in the `qa-automation` repo every test carries a column saying which technique
  it uses and why
- Wrote a `TESTING.md` test strategy document with scope, a **risk matrix** and a test pyramid, used to decide
  which cases must exist first rather than writing cases screen by screen
- Wrote **8 case studies** of bugs in systems in use, each with symptom, reproduction steps and root cause —
  among them legacy documents the system could not see even though permissions allowed it, and a button
  unclickable only on mobile because a modal sat under the topbar for 200 ms during its animation
- Found a system's real permission boundary by working through **24 cases**: the condition was "the user has no
  tenant yet", not "the user is not logged in" as previously assumed — a distinction invisible without isolating
  the variables
- **Tell a system bug from a bug in my own test** before handing anything to a dev: in one case the test
  reported the system was broken and the test itself turned out to be wrong, so I wrote it up as a case study
  to keep the team from spending time on the same false alarm twice
- Hold that a test which **skips rather than fails** when a dependency is unavailable beats one that goes red
  on the environment — so red always means a real bug — and that flake from external systems should be recorded
  plainly, not buried under retries

### Work Experience

**Frontend Developer** — startup · 1 year
Built and shipped features in Angular, Ionic and Tailwind CSS on Firebase. Seeing the cycle from requirement
to production taught me which seams break, and what a bug report needs to be actionable on the first read.

**Event Organizer / Project Coordinator** — Nai Krit Sticker signage shop · current
Pre-event documentation, project wrap-up reports and survey data handling — work that lives on catching every
detail and keeping several parties aligned.

### Automation Toolkit

Also comfortable with, and happy to use where the work calls for it: Playwright + TypeScript (Page Object
Model), API testing, Firebase Emulator, Selenium, Postman, and CI on GitHub Actions. My portfolio holds
**358 automated tests across 4 repos** — written so the regression passes that need repeating every cycle run
themselves, not to replace case design.

### Education

B.Eng. (continuing programme), Electronics Engineering Technology
King Mongkut's University of Technology North Bangkok — College of Industrial Technology

---

## ถ้าต้องบีบให้เหลือ 1 หน้า ตัดบรรทัดไหน

ฉบับนี้อยู่ที่ประมาณ 1 หน้าพอดีถึงเกินเล็กน้อย ลำดับการตัด:

1. **ตัดบูลเล็ตเรื่อง skip แทน fail** — เป็นความเห็นเชิงหลักการ ไม่ใช่ผลงาน เก็บไปตอบตอนสัมภาษณ์
   เรื่อง flaky test ได้ดีกว่า
2. **ย่อบูลเล็ต 24 เคสเหลือหนึ่งบรรทัด** — ตัดคำอธิบายท้าย เหลือแค่ข้อค้นพบ
3. **ย่อ Automation Toolkit เหลือสองบรรทัด** — คงเลข 358 tests ไว้ แต่ตัดรายชื่อเครื่องมือให้สั้น

ห้ามตัด: บูลเล็ต 53 TC-ID, บูลเล็ตเทคนิคออกแบบเคส และบูลเล็ต "แยกบั๊กของระบบกับเทสที่เขียนผิดเอง" —
ตัวสุดท้ายคือสิ่งที่ hiring manager สาย manual ให้น้ำหนักมากที่สุด เพราะมันบอกว่าจะไม่ส่ง false alarm ให้ dev

## เตือนตัวเองก่อนส่งเวอร์ชัน B

- อย่าใส่ "เป้าหมายถัดไป SDET" หรือ "ต้องการขยับไป automation" ลงในเรซูเม่ B
  เก็บไว้ตอบตอนสัมภาษณ์เมื่อถูกถาม และตอบด้วยกรอบ "อยากโตไปกับทีม" ไม่ใช่ "ใช้ที่นี่เป็นทางผ่าน"
- ถ้าประกาศไม่พูดถึง automation เลย ให้ย่อ Automation Toolkit ลงอีก เหลือบรรทัดเดียว
  ไม่ใช่ลบทิ้ง — ลบทิ้งแล้วจะอธิบาย GitHub ที่มีแต่ repo automation ไม่ได้
- คำตอบประจำสำหรับ "มีพอร์ต automation แล้วทำไมมาสมัคร manual":
  automation ที่เขียนบนเคสที่ออกแบบไม่ดีคือการรันเคสห่วย ๆ ให้เร็วขึ้น งานที่อยากทำให้แน่นก่อน
  คือการออกแบบเคสและไล่บั๊กในระบบที่มีผู้ใช้จริงและมีคนอื่นในทีมรีวิวงานให้ — ซึ่งพอร์ตส่วนตัวให้ไม่ได้
