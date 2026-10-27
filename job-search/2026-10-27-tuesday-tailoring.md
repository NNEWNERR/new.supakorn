# รอบอังคาร 2026-10-27 — ปรับเรซูเม่ + cover letter ให้ตรง 2 ประกาศคะแนนสูงสุด

ข้อควรรู้ก่อนอ่าน: รอบนี้เปิดหน้าประกาศจริงไม่ได้ (network policy บล็อกเว็บหางานทุกแห่ง — ดู `tracker.md`)
คีย์เวิร์ดด้านล่างมาจาก snippet ของผลค้นหา ไม่ใช่ตัวประกาศเต็ม **ต้องเปิดประกาศเองแล้วเช็กซ้ำก่อนส่ง**

ประกาศที่คะแนนสูงสุดจริง ๆ คือ ASCGroup — Automated Tester (Playwright) โซนพระราม 3 (Playwright อยู่ในชื่อตำแหน่ง)
แต่อ่าน requirement ไม่ได้เลยแม้แต่บรรทัดเดียว การปรับเรซูเม่ให้ประกาศนั้นจะเป็นการเดา จึงปรับให้ 2 ประกาศ
ที่มีข้อความ requirement จริงแทน และยก ASCGroup เป็นอันดับแรกที่ต้องไปเปิดอ่าน

---

# ประกาศที่ 1 — AMASS Corporation (Thailand): Automate tester (Playwrite, Cypress)

## 1) กำลังปรับเวอร์ชันไหน ให้ใคร

**เรซูเม่เวอร์ชัน A** → AMASS Corporation (Thailand) · ตำแหน่ง Automate tester
hybrid onsite ≥3 วัน/สัปดาห์ · 40,000–70,000 · เปิด 10 อัตรา
ระดับ **A** · ความตรง **4/5**

## 2) คีย์เวิร์ดจากประกาศ และสถานะในเรซูเม่

| คีย์เวิร์ดจากประกาศ | มีในเรซูเม่ A แล้ว? | ทำอะไร |
| --- | --- | --- |
| Test Engineer ≥2 ปี | ❌ ไม่มีตำแหน่งนี้อย่างเป็นทางการ | ไม่เคลม — ให้ Summary นับเป็น "ownership ของ suite" แทนจำนวนปี |
| เขียน automated test ด้วย Playwright | ✅ มีเยอะ | ดันขึ้นประโยคแรกของ Summary |
| Cypress | ❌ ไม่มีหลักฐานในพอร์ต (ถอดออกแล้วใน commit `9750bb7`) | ไม่ใส่ ประกาศเขียนว่า "Cypress **หรือ** Playwright หรือ Robot หรือ Appium" → Playwright ผ่านเกณฑ์ |
| Robot Framework | ❌ | ไม่ใส่ |
| Appium | ❌ มีแต่ Playwright device emulation (Pixel 7) ซึ่งไม่ใช่ของเดียวกัน | ไม่ใส่ และระบุตรง ๆ ตอนสัมภาษณ์ |
| hybrid onsite ≥3 วัน/สัปดาห์ | — | เพิ่มบรรทัดที่อยู่ว่ารับ hybrid กรุงเทพฯ เพื่อไม่ให้ถูกคัดออกเพราะอยู่ต่างจังหวัด |

## 3) ตารางก่อน / หลัง

| # | ก่อน | หลัง | เหตุผล |
| --- | --- | --- | --- |
| 1 | Summary เปิดด้วย "เขียน end-to-end และ API test automation ด้วย Playwright + TypeScript รวม 358 automated tests ใน 4 repo" | "เขียน automated test ด้วย **Playwright + TypeScript** มาแล้ว **358 tests ใน 4 repo** ที่ดูแล suite เองทั้งหมดตั้งแต่ออกแบบเคส เขียนเทส ไปจนถึง CI ที่รันมันทุกวัน" | ประกาศวัดที่ "เขียน automated test ด้วยเครื่องมือเหล่านี้ได้" ไม่ได้วัดที่ E2E/API — ดันคำที่ตรงขึ้นหน้า และแทนคำว่าปีประสบการณ์ด้วยคำว่า ownership |
| 2 | — (ไม่มี) | เพิ่มบรรทัดใต้ชื่อ: "รับงาน hybrid ในกรุงเทพฯ เดินทางเข้าออฟฟิศได้ตามรอบที่ทีมกำหนด" | ประกาศบังคับ onsite ≥3 วัน/สัปดาห์ และที่อยู่เป็นต่างจังหวัด — ถ้าไม่พูดก่อน HR จะตัดด้วยเหตุผลนี้โดยไม่ถาม |
| 3 | "วาง CI 4 workflow ให้ suite เดียวกัน — matrix 17 ชุดตอน PR, ชุด rules 90 เคสบน emulator ทุก push, แจ้งเตือนเข้า Discord และ daily soak..." | "วาง CI 4 workflow บน GitHub Actions ให้ **เทส 96 ตัวรันเองทุก PR** — matrix 17 ชุด, ชุด rules 90 เคสบน emulator ทุก push, แจ้งเตือน Discord และ daily soak ยิง production ทุกวัน จับ regression ได้ภายใน 24 ชั่วโมง" | ประกาศ 10 อัตราแบบนี้มักเป็นงาน outsource ที่ต้องส่งมอบ suite ให้ลูกค้า — เน้นว่า "รันเองได้" ซึ่งเป็นสิ่งที่ลูกค้าซื้อ |
| 4 | บูลเล็ต Playwright Test Agents (planner → generator → healer) อยู่ลำดับที่ 7 | ย้ายขึ้นเป็นลำดับที่ 3 | เป็นบูลเล็ตเดียวที่พิสูจน์ว่าเขียนเทสเร็วได้แบบมีมาตรฐานกำกับ ซึ่งคือสิ่งที่งาน 10 อัตราต้องการ |
| 5 | บูลเล็ต `public-boundary` 24 เคส | **ตัด** | ประกาศนี้ไม่ได้ขายเรื่องการออกแบบเคสเชิงลึก และต้องเคลียร์พื้นที่ให้เหลือ 1 หน้าหลังเพิ่มบรรทัดที่อยู่ |
| 6 | Technical Skills เรียง "Playwright, POM, API testing, Firebase Emulator, Vitest, Selenium, Postman" | เรียงใหม่เป็น "**Playwright (TypeScript), Selenium**, Page Object Model, API testing, Postman, Firebase Emulator, Vitest" | ประกาศระบุเครื่องมือเป็นแกน — ดันสองตัวที่มีจริงและตรงกับแนวประกาศขึ้นหน้า ไม่เพิ่มของที่ไม่มี |

**แก้ 6 จุด** (เพิ่ม 1, แก้ถ้อยคำ 3, ย้ายลำดับ 1, ตัด 1)

## 4) cover letter — AMASS (169 คำ)

> เรียนทีมสรรหาบริษัท AMASS Corporation (Thailand)
>
> ผมสนใจตำแหน่ง Automate tester ครับ ประกาศของท่านเขียนว่ารับได้ทั้ง Cypress, Playwright, Robot Framework
> หรือ Appium ซึ่งอ่านแล้วเข้าใจว่าทีมมองหาคนที่ออกแบบและดูแล automation suite ได้จริง ไม่ใช่คนที่ผูกกับ
> เครื่องมือตัวใดตัวหนึ่ง และการเปิดถึง 10 อัตราบอกว่างานมีปริมาณจริงที่ต้องส่งมอบ ซึ่งเป็นลักษณะงานที่ผมอยากทำ
>
> หลักฐานของผมคือ automated test 358 ตัวใน 4 repo ที่เขียนด้วย Playwright + TypeScript และผมเป็นเจ้าของ
> ทั้ง suite เอง ตัวที่หนักที่สุดคือแพลตฟอร์มจองคิวบน Firebase ที่เปิดใช้งานจริง — 96 E2E/API tests ใน
> 36 spec files บวก 90 security-rules tests โดยมี 53 test case อ้างอิงกลับด้วย TC-ID และมี CI 4 workflow
> ที่รันทั้งหมดนี้เองทุก PR รวมถึง soak ที่ยิง production ทุกวัน การเขียนเทสชุดนี้ทำให้เจอบั๊กจริง 2 ตัว
> ที่การกดทดสอบด้วยมือไม่เจอ
>
> ก่อนมาสาย QA ผมเป็น frontend developer อยู่ 1 ปี บน Angular และ Firebase จึงอ่านโค้ดที่กำลังทดสอบได้
> และเขียนบั๊กรีพอร์ตที่ dev แก้ได้เลย ขอโอกาสเข้าไปคุยและพาดูโครงสร้างเทสจริงครับ
>
> ขอแสดงความนับถือ
> ศุภากร เศวตวงศ์สกุล

### English version (171 words)

> Dear AMASS Corporation (Thailand) hiring team,
>
> I am writing about your Automate tester opening. Your posting accepts Cypress, Playwright, Robot Framework
> or Appium, which reads as a team looking for someone who can design and own an automation suite rather than
> someone tied to one tool — and ten openings says there is real delivery work behind it. That is the kind of
> work I want.
>
> My evidence is 358 automated tests across 4 repos, written in Playwright and TypeScript, where I own the
> whole suite. The heaviest is a live Firebase queue-booking platform: 96 E2E/API tests across 36 spec files
> plus 90 security-rules tests, with 53 cases traced by TC-ID, and 4 CI workflows that run all of it on every
> PR plus a daily soak against production. Writing that suite surfaced two real bugs manual passes had missed.
>
> Before QA I spent a year as a frontend developer on Angular and Firebase, so I can read the code under test
> and write bug reports a developer can act on. I would welcome the chance to walk you through the suite.
>
> Kind regards,
> Supakorn Sawetwongsakul

## 5) จุดอ่อนที่แก้ด้วยการเขียนไม่ได้

- **ไม่มีตำแหน่ง Test Engineer 2 ปีตามที่ประกาศขอ** — เกณฑ์ที่ตั้งไว้คือสมัครได้ถ้าขอ 1–2 ปีและสแตกตรง
  ข้อนี้เข้าเกณฑ์ แต่ HR อาจคัดที่ขั้นกรองใบ ทางแก้เดียวคือให้ตัวเลขในพอร์ตพูดก่อนในสามบรรทัดแรก
- **ไม่มี Appium** — ถ้าทีมส่งคนไปงานมือถือ ข้อนี้ตัดจบ ไม่ต้องดัดเรซูเม่ให้ดูเหมือนมี
- **onsite ≥3 วัน/สัปดาห์ จากสมุทรสงคราม** — ต้องคิดเรื่องการเดินทางให้จบก่อนตอบสัมภาษณ์ ไม่ใช่เรื่องที่
  เรซูเม่ช่วยได้

---

# ประกาศที่ 2 — Bangkok Bank: QA Engineer (Manual + Automated Testing)

## 1) กำลังปรับเวอร์ชันไหน ให้ใคร

**เรซูเม่เวอร์ชัน B** → ธนาคารกรุงเทพ · QA Engineer (Manual + Automated Testing) · ย่านนาวา กรุงเทพฯ
ระดับ: ชื่อตำแหน่งคาบเกี่ยว — จัดเป็น **B ป้ายเขียว** เพราะมี automation อยู่ในขอบงานตั้งแต่ประกาศ
ความตรง **3/5**

เหตุที่ใช้เวอร์ชัน B ไม่ใช่ A: ประกาศเอา manual มาก่อนในชื่อตำแหน่ง และสแตก automation ที่ระบุ
(Robot Framework, Appium, Espresso) แทบไม่ทับกับพอร์ตเลย ถ้าส่งเวอร์ชัน A จะถูกวัดด้วยไม้บรรทัด
ที่ตัวเองสอบไม่ผ่าน

## 2) คีย์เวิร์ดจากประกาศ และสถานะในเรซูเม่

| คีย์เวิร์ดจากประกาศ | มีในเรซูเม่ B แล้ว? | ทำอะไร |
| --- | --- | --- |
| manual testing | ⚠️ มีโดยนัย แต่ไม่มีคำนี้ | เพิ่มคำตรง ๆ ในบูลเล็ต exploratory |
| functional / regression / system testing | ⚠️ มีแนวคิด ไม่มีคำ | ใส่คำให้ตรงในบูลเล็ต TC-ID |
| test plan + defect tracking | ⚠️ มี `TESTING.md` และ TC-ID | เขียนให้เป็นคำที่ประกาศใช้ |
| black-box / white-box testing | ⚠️ ทำอยู่ ไม่มีคำ | เพิ่มคำใน Test Design |
| Robot Framework / Appium / Espresso | ❌ ไม่มีเลย | ไม่ใส่ ระบุตรง ๆ ว่าพร้อมเรียน |
| Selenium / Cypress | ✅ Selenium มี · ❌ Cypress ไม่มีหลักฐาน | คง Selenium ตัด Cypress |
| mobile app testing iOS / Android | ⚠️ มีแต่ Playwright emulation บน Pixel 7 | เขียนให้ตรงว่าคือ emulation ไม่ใช่เครื่องจริง |
| load / performance testing | ❌ ไม่มีเลย | ไม่ใส่ — นี่คือช่องว่างที่ใหญ่ที่สุดของประกาศนี้ |

## 3) ตารางก่อน / หลัง

| # | ก่อน | หลัง | เหตุผล |
| --- | --- | --- | --- |
| 1 | "ออกแบบชุดเทส 53 test case ที่อ้างอิงกลับด้วย TC-ID ... ครอบคลุม auth, การจอง, สิทธิ์ตาม role..." | "ออกแบบและไล่ **functional, regression และ system test** รวม **53 test case ที่อ้างอิงกลับด้วย TC-ID** ครอบคลุม auth, การจอง, สิทธิ์ตาม role, การจองชนกันแบบ concurrent และการแยกข้อมูลระหว่างลูกค้าแต่ละราย" | ใส่คำสามคำที่ประกาศใช้ลงในงานที่ทำจริงอยู่แล้ว ไม่ได้เพิ่มงานใหม่ |
| 2 | "ใช้เทคนิคออกแบบเคสแบบระบุเหตุผลได้ — EP, BVA, decision table, state transition" | "ใช้เทคนิค **black-box** ที่ระบุเหตุผลได้ — EP, BVA, decision table, state transition — และอ่าน **โค้ดกับ security rules** ประกอบแบบ white-box เพราะเป็นคนเขียนระบบเอง" | ประกาศถามทั้ง black-box และ white-box ตรง ๆ และข้อนี้เป็นจริงเพราะเป็นเจ้าของทั้ง stack |
| 3 | "เขียนเอกสารกลยุทธ์การทดสอบ `TESTING.md` ที่ระบุขอบเขต risk matrix และ test pyramid" | "เขียน **test plan / test strategy** `TESTING.md` ที่ระบุขอบเขต risk matrix และ test pyramid และใช้จัดลำดับว่าเคสไหนต้องมีก่อน" | ใช้คำ "test plan" ที่ประกาศใช้ ให้ ATS และคนอ่านจับได้ |
| 4 | "เขียน case study 8 เคส จากบั๊กในระบบที่เปิดใช้งานอยู่ แต่ละเคสมีอาการ ขั้นตอนทำซ้ำ และสาเหตุราก" | "เขียน **รายงานบั๊ก** แบบ case study **8 เคส** จากระบบที่เปิดใช้งานอยู่ แต่ละเคสมีอาการ ขั้นตอนทำซ้ำ สาเหตุราก และ **ระดับ severity** — มี 1 เคสที่เจอเฉพาะบนมือถือ" | ประกาศเน้น defect tracking และงานมือถือ ดึงสองอย่างนี้ขึ้นมาในบูลเล็ตเดียว |
| 5 | Automation Toolkit: "Playwright + TypeScript (POM), API testing, Firebase Emulator, Selenium, Postman และ CI บน GitHub Actions" | "Playwright + TypeScript (POM), **Selenium**, API testing, Postman, Firebase Emulator และ CI บน GitHub Actions · **ยังไม่ได้ใช้ Robot Framework และ Appium — พร้อมเรียน** โดยพื้นฐาน POM และ CI ที่มีย้ายเข้าสองตัวนี้ได้" | พูดช่องว่างเองดีกว่าให้ถูกจับได้ตอนสัมภาษณ์ และบอกว่าทำไมจะเรียนได้เร็ว |
| 6 | — | **ตัด** วลี "เป้าหมายถัดไป SDET" ออกจากทุกที่ (ยังอยู่ใน README ของ GitHub) | ธนาคารกลัวคนอยู่ไม่ครบปี README เป็นสิ่งที่ผู้สัมภาษณ์เปิดดูแน่ ๆ — ต้องแก้ที่ README ด้วย ไม่ใช่แค่เรซูเม่ |

**แก้ 6 จุด** (แก้ถ้อยคำ 5, ตัด 1 — และมี 1 จุดที่ต้องไปแก้ที่ `README.md` ของโปรไฟล์ GitHub ด้วย)

## 4) cover letter — ธนาคารกรุงเทพ (178 คำ)

> เรียนทีมสรรหาธนาคารกรุงเทพ
>
> ผมสนใจตำแหน่ง QA Engineer (Manual + Automated Testing) ครับ สิ่งที่ทำให้ผมสนใจคือประกาศนี้วางงาน manual
> ไว้คู่กับ automation ตั้งแต่ชื่อตำแหน่ง และระบุทั้ง functional, regression, system ไปจนถึงงานทดสอบ
> แอปมือถือทั้ง iOS และ Android — แปลว่าทีมไม่ได้มองว่า automation แทน manual ได้ ซึ่งผมเห็นด้วย
> งานโมบายแบงก์กิ้งที่คนใช้ทุกวันเป็นงานที่ความผิดพลาดมีราคาจริง
>
> หลักฐานของผมคือวิธีออกแบบเคส ผมออกแบบและไล่เทส 53 test case ที่อ้างอิงกลับด้วย TC-ID ของแพลตฟอร์มจองคิว
> ที่มีผู้ใช้จริง ครอบคลุมสิทธิ์ตาม role การจองชนกันแบบ concurrent และการแยกข้อมูลระหว่างลูกค้าแต่ละราย
> โดยใช้ equivalence partitioning, boundary value analysis, decision table และ state transition
> ที่อธิบายได้ว่าเลือกเพราะอะไร และเขียนรายงานบั๊ก 8 เคสจากระบบที่เปิดใช้งานอยู่ ตั้งแต่อาการถึงสาเหตุราก
> หนึ่งในนั้นเจอเฉพาะบนมือถือ
>
> ผมมาจากสาย frontend developer 1 ปี จึงอ่านโค้ดที่ทดสอบได้และเขียนบั๊กรีพอร์ตที่ dev แก้ได้เลย
> ส่วน Robot Framework และ Appium ผมยังไม่ได้ใช้ แต่พื้นฐาน Page Object Model และ CI ที่มีอยู่ย้ายเข้าได้
> ขอโอกาสเข้าไปคุยครับ
>
> ขอแสดงความนับถือ
> ศุภากร เศวตวงศ์สกุล

### English version (176 words)

> Dear Bangkok Bank hiring team,
>
> I am writing about the QA Engineer (Manual + Automated Testing) position. What drew me is that the posting
> puts manual work alongside automation in the title itself, and spans functional, regression and system
> testing through to mobile testing on both iOS and Android. That reads as a team that does not treat
> automation as a replacement for manual testing, and I agree — in mobile banking that people use daily,
> getting it wrong has a real price.
>
> My evidence is how I design cases. I designed and ran 53 TC-ID-traced test cases for a queue-booking
> platform with real users, covering role-based permissions, concurrent double-booking and per-customer data
> isolation, using equivalence partitioning, boundary value analysis, decision tables and state transition —
> and I can say why each applies. I also wrote 8 bug reports as case studies from systems in use, symptom
> through root cause; one reproduced only on mobile.
>
> A year as a frontend developer means I can read the code under test. I have not used Robot Framework or
> Appium, but my Page Object Model and CI grounding transfers. I would welcome a conversation.
>
> Kind regards,
> Supakorn Sawetwongsakul

## 5) จุดอ่อนที่แก้ด้วยการเขียนไม่ได้

- **ไม่มี load / performance testing เลย** — ประกาศระบุไว้ชัด และพอร์ตไม่มีอะไรรองรับ
  เขียนให้ดูมีไม่ได้ ถ้าข้อนี้เป็น requirement หลัก โอกาสผ่านต่ำ
- **ไม่มี Robot Framework, Appium, Espresso** — สามตัวนี้คือแกน automation ของประกาศ
  พอร์ตมีแต่ Playwright และ Selenium
- **mobile = emulation ไม่ใช่เครื่องจริง** — Pixel 7 ในพอร์ตคือ Playwright device emulation
  ต้องพูดให้ตรงตั้งแต่ใบสมัคร ไม่ปล่อยให้เข้าใจผิดแล้วไปแตกตอนสัมภาษณ์
- **วันที่ประกาศน่าจะราว 25 ก.ย. 69** — เกิน 7 วันไปไกล อาจปิดรับแล้ว ต้องเช็กก่อนลงแรงเขียนใบจริง
- **ความเสี่ยงดู overqualified** — พอร์ต automation 358 tests กับงานที่เอา manual มาก่อน
  ต้องคุมน้ำเสียงให้เป็น "เอามาช่วยทีม" และต้องเอาคำว่า "เป้าหมายถัดไป SDET" ออกจาก README ก่อนส่ง
