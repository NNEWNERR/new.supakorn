# เรซูเม่ — เวอร์ชัน A (Automation QA / SDET) · ไทย
> ฉบับกลาง ห้ามแก้ไฟล์นี้เพื่อบริษัทเดียว ให้ copy ออกไปก่อน
> ลำดับหัวข้อตายตัว: Summary → Test Automation Projects → Technical Skills → Work Experience → Education
> ตัวเลขทุกตัวในนี้อ้างได้จาก repo จริง ห้ามปัดขึ้น

**ศุภากร เศวตวงศ์สกุล (นิว)**
Automation QA Engineer — Playwright + TypeScript
สมุทรสงคราม · รับ Remote / Hybrid / กรุงเทพฯ
newnertg@gmail.com · github.com/NNEWNERR · nnewnerr.github.io

## Summary
frontend developer ที่ย้ายมาสาย test automation มี 358 automated tests ใน 4 โปรเจกต์
ครอบคลุม Playwright E2E, API contract และ Firestore security rules วางอยู่บน 10 Page Object
และ 7 GitHub Actions workflow โดยหนึ่งในนั้นเป็น daily soak ที่ยิงกับ production จริงทุกวัน
ประสบการณ์เขียน Angular/Ionic บน Firebase 1 ปี ทำให้ทดสอบชั้นเดียวกับที่เคยเขียนมาเอง

## Test Automation Projects

**Krungthon Air — Booking QA suite** *(repo private — ร้านของผมเอง)*
- สร้าง 96 E2E/API tests ใน 36 spec files ให้แพลตฟอร์มจองคิวบน Firebase ที่ใช้งานจริง ครอบคลุม auth, การจอง, สิทธิ์การเข้าถึง, การจองชนกันแบบ concurrent, การแยกข้อมูลระหว่าง tenant, a11y และ mobile responsive
- เขียน 90 Firestore security-rules tests รันบน emulator ทุก push โดย assert สิ่งที่ **ต้องถูกปฏิเสธ** ไม่ใช่เฉพาะสิ่งที่ต้องผ่าน
- อ้างอิง 53 test case กลับด้วย TC-ID ทำให้ coverage ตรวจสอบได้จริง ไม่ใช่การประมาณ
- วาง 4 GitHub Actions workflow: matrix 17 ชุดตอน PR, ชุด rules 90 เคสทุก push, แจ้งเตือนเข้า Discord และ daily soak ยิง production ที่จับ regression ได้ภายใน 24 ชั่วโมง ไม่ต้องรอ PR ถัดไป

**multitenant-booking-qa** — github.com/NNEWNERR/multitenant-booking-qa
- ออกแบบ 93 tests สองชั้นบนระบบเดียว: 76 Firestore rules tests + 17 Playwright UI tests บน desktop และ Pixel 7 รันกับ emulator จริงทั้งคู่ ไม่ใช่ mock
- เจอบั๊กจริง 2 ตัวจากการเขียนชั้น UI: เอกสารรุ่นเก่าที่ query มองไม่เห็นทั้งที่ rules ยอม และ modal ที่ถูกขังใต้ topbar 200ms ระหว่าง animation
- พิสูจน์ด้วยชุด `public-boundary` 24 เคส ว่าเส้นแบ่งสิทธิ์จริงคือ "ยังไม่มีสังกัด" ไม่ใช่ "ยังไม่ล็อกอิน"
- ทำให้ชุดเทสไม่ต้องใช้ credential ผู้รีวิวรัน `npm ci && npm test` ได้เลย

**qa-automation** — github.com/NNEWNERR/qa-automation
- จัดโครง 63 tests เป็น 8 Playwright projects: API contract, UI, accessibility (axe-core), visual regression, smoke และ auth แยกตาม role ด้วย `storageState`
- ลดเวลารอผล CI ด้วยการรัน 4 shard ขนาน แล้ว merge blob report กลับเป็นรายงาน HTML ฉบับเดียว
- ติด tag `@smoke` `@regression` `@a11y` `@visual` ให้เลือกรันทีละชั้นได้ ไม่ต้องรันทั้งชุด
- ใช้ Playwright Test Agents จริงทั้งสาย (planner → generator → healer): แผน 32 scenario → 31 เทสที่ generator สร้าง ผ่านการรีวิวตาม flake playbook พร้อมบันทึกว่ามนุษย์แก้อะไร กติกาประจำ repo คือ healer ซ่อม locator ได้ แต่ห้ามแก้ค่าที่คาดหวัง ลด assertion หรือเพิ่ม retry — และผมทดสอบแล้วว่ามันทำตาม

**sauce-demo-tests** — github.com/NNEWNERR/sauce-demo-tests
- ครอบคลุม login, การเรียงสินค้า, ตะกร้า และ checkout ใน 16 tests หลัง 4 Page Object บน `BasePage` ร่วมกัน พร้อม visual และ accessibility check
- เขียน `TESTING.md` เอกสารกลยุทธ์การทดสอบที่มีขอบเขต, risk matrix และ test pyramid

## Technical Skills
**Automation** Playwright (TypeScript), Selenium, Page Object Model, API/contract testing, Postman, axe-core accessibility, visual regression, Firebase Emulator, Vitest
**CI/CD** GitHub Actions (matrix, sharding, blob-report merge, scheduled soak), Discord notification, Git
**Development** TypeScript, JavaScript, Angular, Ionic, Tailwind CSS, Firebase/Firestore
**Test design** equivalence partitioning, boundary value analysis, decision table, state transition, risk-based testing

## Work Experience
**Frontend Developer** — startup · 1 ปี
- พัฒนาและส่งมอบฟีเจอร์ด้วย Angular, Ionic และ Tailwind CSS บน backend ที่เป็น Firebase ซึ่งเป็นสแตกเดียวกับที่ตอนนี้ผมเขียนเทสจับ จึงรู้ว่ามันพังตรงไหน

**Event Organizer / Project Coordinator** — ร้านป้ายนายกฤษสติ๊กเกอร์ · ปัจจุบัน
- จัดทำเอกสารก่อนงาน, รายงานสรุปโปรเจกต์ และดูแลข้อมูลแบบสำรวจ

## Education
**วศ.บ. (ต่อเนื่อง) เทคโนโลยีวิศวกรรมอิเล็กทรอนิกส์**
มหาวิทยาลัยเทคโนโลยีพระจอมเกล้าพระนครเหนือ — วิทยาลัยเทคโนโลยีอุตสาหกรรม

---
### ถ้าเกิน 1 หน้า ให้ตัดตามลำดับนี้
1. `sauce-demo-tests` bullet แรก — 16 tests เป็นตัวเลขที่เล็กที่สุดในหน้า ส่วนที่ควรเก็บไว้คือเอกสารกลยุทธ์
2. bullet ของ Event Organizer — เป็นงานปัจจุบันแต่ไม่เกี่ยวกับ QA ชื่อตำแหน่งอย่างเดียวพอปิดช่องว่างการทำงานแล้ว
3. `qa-automation` bullet 3 (tag) — เป็นรายละเอียดการออกแบบที่ดี แต่ bullet sharding แสดงวิจารณญาณเรื่อง CI ไปแล้ว
ห้ามตัด: 90 rules tests, daily soak, บั๊กจริง 2 ตัว — สามอย่างนี้คือสิ่งที่พอร์ตจากคอร์สเรียนไม่มี
