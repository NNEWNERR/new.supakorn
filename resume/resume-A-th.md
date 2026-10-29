# ศุภากร เศวตวงศ์สกุล (นิว) — Automation QA Engineer
สมุทรสงคราม · รับ remote / hybrid / กรุงเทพฯ · newnertg@gmail.com
github.com/NNEWNERR · nnewnerr.github.io

> เรซูเม่เวอร์ชัน A — สำหรับประกาศ Automation Tester / QA Engineer (Automation) /
> Test Automation Engineer / SDET · ตัวเลขทุกตัวในไฟล์นี้มาจาก repo จริงเท่านั้น

## Summary
เขียน end-to-end และ API automation ด้วย Playwright + TypeScript บน Page Object Model
รวม 358 automated tests และ 7 CI workflow ใน 4 ระบบ โดย 1 ระบบเป็นแพลตฟอร์มที่เปิดใช้งานจริง
ก่อนมาสาย QA เป็น frontend developer 1 ปี — อ่านโค้ดที่กำลังทดสอบได้ และรู้ว่าแอปพังด้วยสาเหตุอะไร

## Test Automation Projects

**Krungthon Air — QA suite** *(private · แพลตฟอร์มจองคิวบน Firebase ที่ใช้งานจริง)*
- ออกแบบและดูแลชุดเทส E2E/API 96 เทสใน 36 spec file ด้วย Playwright + TypeScript
  ครอบคลุม auth, การจอง, สิทธิ์การเข้าถึง, การจองชนกันแบบ concurrent, การแยกข้อมูลระหว่าง tenant,
  a11y และ mobile responsive โดยอ้างอิงกลับด้วย TC-ID 53 รายการ
- เขียน Firestore security rules test 90 เคส รันบน emulator จริงทุก push ไม่ใช้ mock
- วาง CI 4 workflow บน GitHub Actions — matrix 17 ชุดตอน PR, ชุด rules 90 เคสทุก push,
  แจ้งผลเข้า Discord และ daily soak ยิงกับ production ทุกวัน เพื่อจับ regression ภายใน 24 ชั่วโมง
  แทนที่จะรอ PR ถัดไป

**multitenant-booking-qa** — github.com/NNEWNERR/multitenant-booking-qa
- เขียนเทสสองชั้นของระบบเดียวกัน 93 เทส: Firestore rules 76 เคส + Playwright UI 17 เคส
  (desktop และ Pixel 7) รันกับ Firebase Emulator ทั้งคู่ `npm ci && npm test` จบ ไม่ต้องมี credential
- พบบั๊กจริง 2 ตัวจากการเขียน UI test: เอกสารรุ่นเก่าที่ query มองไม่เห็นทั้งที่ rules ยอม
  และ modal ที่ถูกขังใต้ topbar 200 ms ระหว่าง animation
- ออกแบบชุด `public-boundary` 24 เคส พิสูจน์ว่าเส้นแบ่งสิทธิ์จริงคือ "ยังไม่มีสังกัด" ไม่ใช่ "ยังไม่ล็อกอิน"

**qa-automation** — github.com/NNEWNERR/qa-automation
- โครงสร้าง 63 เทสใน 8 Playwright project แยกชั้น API contract, UI, accessibility (axe-core),
  visual regression, smoke และ auth ตาม role ด้วย `storageState`
- ตั้ง CI ให้รัน 4 shard ขนาน แล้ว merge blob report กลับเป็นรายงาน HTML ฉบับเดียว
  ติด tag (`@smoke` `@regression` `@a11y` `@visual`) ให้เลือกรันทีละชั้นได้
- ใช้ Playwright Test Agents (planner → generator → healer) จริง: แผน 32 scenario → 31 เทส
  ที่ผ่านการรีวิวตาม flake playbook และตั้งกติกาประจำ repo ว่า healer ซ่อม locator ได้
  แต่ห้ามแก้ค่าที่คาดหวัง ลด assertion หรือเพิ่ม retry/timeout — ทดสอบแล้วว่ามันทำตาม

**sauce-demo-tests** — github.com/NNEWNERR/sauce-demo-tests
- 16 เทสครอบคลุม login, การเรียงสินค้า, ตะกร้า และ checkout พร้อม visual + accessibility check
- Page Object 4 ตัวบน `BasePage` ร่วมกัน (รวมทุก repo 10 ตัว) และ `TESTING.md` —
  เอกสารกลยุทธ์การทดสอบที่มีขอบเขต, risk matrix และ test pyramid

**Case Studies** — new.supakorn/case-studies · 8 เคสจากระบบที่ใช้งานอยู่
เล่าตั้งแต่อาการถึงสาเหตุราก เช่น ที่นั่งค้างในคิว 640 รายการจากเส้นทางยกเลิก,
tenant isolation ที่เจอช่องรั่วครบทั้ง 3 ชั้น และกฎสิทธิ์รุ่นเก่าที่ทำให้ rules test เดิมแดง 15 เคส

## Technical Skills
**Automation:** Playwright, TypeScript, Selenium, Postman / API testing, Vitest, axe-core
**CI & Infra:** GitHub Actions (matrix, sharding, blob report merge), Firebase Emulator, Git
**ระบบที่เคยทดสอบ:** Firebase / Firestore Rules / Cloud Functions, Angular, Ionic
**Test design:** EP/BVA, decision table, state transition, risk-based, negative testing

## Work Experience
**Frontend Developer** — startup · 1 ปี
พัฒนาและส่งมอบฟีเจอร์ด้วย Angular, Ionic และ Tailwind CSS บน backend ที่เป็น Firebase —
เข้าใจสิ่งที่ทดสอบเพราะเคยเขียนมันมาก่อน รู้ว่า state ค้างและ race condition เกิดที่ชั้นไหน

**Event Organizer / Project Coordinator** — ร้านป้ายนายกฤษสติ๊กเกอร์ · ปัจจุบัน
จัดทำเอกสารก่อนงาน, รายงานสรุปโปรเจกต์ และดูแลข้อมูลแบบสำรวจ

## Education
วศ.บ. (ต่อเนื่อง) เทคโนโลยีวิศวกรรมอิเล็กทรอนิกส์ —
มหาวิทยาลัยเทคโนโลยีพระจอมเกล้าพระนครเหนือ วิทยาลัยเทคโนโลยีอุตสาหกรรม
