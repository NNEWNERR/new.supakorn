# Cover letter — โครงระดับ A และ B (ไทย + EN)

กติกา: ไม่เกิน 200 คำ · 3 ย่อหน้า · ย่อหน้า 1 ต้องอ้างสิ่งที่บริษัททำจริง
ช่อง `[...]` คือจุดที่ **ต้องเปิดประกาศจริงมาเติม** ห้ามเดาชื่อสินค้าหรือสิ่งที่บริษัททำ
ถ้าเติมย่อหน้า 1 ไม่ได้ ยังไม่ต้องส่ง — จดหมายที่ชมแบบกลวงแย่กว่าไม่มีจดหมาย

หมายเหตุ: ฉบับอังกฤษนับแล้วอยู่ใต้ 200 คำ (ไม่รวมคำขึ้นต้นและลงท้าย)
ฉบับไทยนับคำด้วยเครื่องมือในเครื่องนี้ไม่ได้ (ภาษาไทยไม่เว้นวรรคระหว่างคำ) ให้วัดตอนวางลงเอกสารจริง
ความยาวทั้งสองฉบับไทยคุมไว้เท่าฉบับอังกฤษโดยนับย่อหน้าและบรรทัด

---

## ระดับ A — ไทย

เรียน ทีม[ชื่อทีม/ฝ่าย] [ชื่อบริษัท]

ผมขอสมัครตำแหน่ง [ชื่อตำแหน่งตามประกาศ] ครับ ผมสนใจบริษัทนี้เพราะ [สิ่งที่บริษัททำจริง — ชื่อผลิตภัณฑ์
หรือระบบที่เห็นจากประกาศ/เว็บบริษัท] ซึ่งเป็นงานที่ความถูกต้องของสิทธิ์และข้อมูลสำคัญกว่าความเร็วของฟีเจอร์
และเป็นโจทย์แบบเดียวกับที่ผมทำมาเอง

หลักฐานของผมเป็นโค้ดที่รันได้ ไม่ใช่คำบรรยาย: 358 automated tests ใน 4 โปรเจกต์ บน Playwright + TypeScript
วางหลัง 10 Page Object ชุดใหญ่ที่สุดเป็น 96 E2E/API tests ใน 36 spec ของแพลตฟอร์มจองคิวบน Firebase
ที่ใช้งานจริง คู่กับ 90 เคสระดับ security rules ที่ assert ว่าระบบต้องปฏิเสธอะไร มี CI 7 workflow
รวมถึง matrix 17 ชุดตอน PR และ daily soak ที่ยิง production ทุกวันเพื่อให้ regression ปรากฏภายใน 24 ชั่วโมง
การเขียนชั้น UI ชุดหนึ่งทำให้เจอบั๊กจริง 2 ตัวที่ชั้น rules มองไม่เห็น

ก่อนย้ายมาสาย QA ผมเป็น frontend developer 1 ปีบน Angular/Ionic + Firebase ซึ่งเป็นสแตกเดียวกับที่ตอนนี้
ผมเขียนเทสจับ ผมจึงอ่าน PR ได้ว่าของใหม่เสี่ยงทำอะไรพัง ไม่ใช่รอให้เทสบอก
ขอโอกาสคุยเพื่อเล่าโครงสร้างชุดเทสและ soak workflow ให้ฟังละเอียดครับ

ขอแสดงความนับถือ
ศุภากร เศวตวงศ์สกุล · newnertg@gmail.com · github.com/NNEWNERR

---

## Level A — English

Dear [team/hiring manager], [Company],

I am applying for the [exact job title from posting] role. What drew me to [Company] is
[a named product or system from the posting]:
work where correct permissions and correct data matter more than feature velocity — the problem
I have been testing on my own systems.

My evidence is code that runs. 358 automated tests across four projects in Playwright and
TypeScript, behind 10 Page Objects. The largest is 96 E2E/API tests in 36 spec files for a Firebase
booking platform in daily production use, paired with 90 security-rules cases asserting what the
system must refuse. Seven CI workflows back it, including a 17-config matrix on pull requests and a
daily soak against production, so a regression surfaces within 24 hours. Writing one UI layer found
2 real defects the rules layer could not see.

Before QA I spent a year as a frontend developer on Angular/Ionic and Firebase — the stack I now
test — so I read a PR for risk instead of waiting for a suite to tell me. I would welcome the chance to walk
through the suite and the soak workflow.

Sincerely,
Supakorn Sawetwongsakul · newnertg@gmail.com · github.com/NNEWNERR

---

## ระดับ B — ไทย

เรียน ทีม[ชื่อทีม/ฝ่าย] [ชื่อบริษัท]

ผมขอสมัครตำแหน่ง [ชื่อตำแหน่งตามประกาศ] ครับ เหตุผลที่สนใจบริษัทนี้คือ [สิ่งที่บริษัททำจริง
— ระบบหรือลูกค้าที่ระบุไว้ในประกาศ] งานแบบนี้คนใช้จริงเจอผลทันทีเมื่อมีอะไรผิด
และเป็นงานที่การออกแบบเคสให้ครบมีค่ามากกว่าการกดตามสคริปต์

สิ่งที่ผมทำได้ตั้งแต่สัปดาห์แรกคือการออกแบบเคส ผมใช้ equivalence partitioning, boundary value analysis,
decision table และ state transition แล้วบันทึกกำกับไว้ว่าเคสไหนใช้เทคนิคอะไรเพราะอะไร เพื่อให้คนอื่นรีวิวการเลือกเคสได้
เส้นแบ่งสิทธิ์จุดเดียวในระบบจองคิวของผมกินไป 24 เคส และทำให้พบว่ากฎจริงคือ "ผู้ใช้ยังไม่มีสังกัด"
ไม่ใช่ "ยังไม่ล็อกอิน" ซึ่งเป็นจุดที่ requirement เดิมกำกวม ผมยังเขียนรายงานบั๊กที่เจอจากระบบที่ใช้งานจริง
ไว้ 8 เคส ไล่ตั้งแต่อาการถึงสาเหตุราก ให้ developer แก้ได้โดยไม่ต้องย้อนมาถาม

ก่อนหน้านี้ผมเป็น frontend developer 1 ปีบน Angular/Ionic + Firebase ผมจึงรู้ว่าบั๊กมักเกิดตรงไหน
และควรถามอะไรก่อนเปิดใบ แทนที่จะเขียนว่า "ใช้งานไม่ได้" งาน automation ที่ผมทำไว้มีด้วย
และพร้อมหยิบมาใช้เมื่อทีมเห็นว่าชุดไหนคุ้มจะ automate แต่สิ่งที่ผมอยากทำให้ดีในตำแหน่งนี้
คือการทดสอบให้ครบและสื่อสารกับ dev ให้แก้ได้เร็ว ขอโอกาสเข้าไปคุยครับ

ขอแสดงความนับถือ
ศุภากร เศวตวงศ์สกุล · newnertg@gmail.com · github.com/NNEWNERR

---

## Level B — English

Dear [team/hiring manager], [Company],

I am applying for the [exact job title from posting] role. [Company] interested me because of
[a system or customer base named in the posting]: work users feel
immediately when something is wrong, where designing the right cases matters more than running a
script.

What I bring from week one is test design. I use equivalence partitioning, boundary value analysis,
decision tables and state transition, and I record which technique each case applies and why, so my
selection can be reviewed. One access-control boundary in my own booking
system took 24 cases, and showed the real rule was "no tenant yet", not "not logged in" — the point
the requirement left ambiguous. I have written up 8 defects from a
system in daily use, symptom through root cause, so a developer can fix them without asking back.

A year as a frontend developer on Angular/Ionic and Firebase taught me where defects originate and
what to ask before filing. I have automation work ready when a suite earns
it, but what I want to do well here is thorough coverage and reports developers can act on.

Sincerely,
Supakorn Sawetwongsakul · newnertg@gmail.com · github.com/NNEWNERR

