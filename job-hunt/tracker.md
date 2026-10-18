# Job Hunt Tracker — ศุภากร เศวตวงศ์สกุล

ไฟล์สถานะต่อเนื่องของรูทีนหางาน แยกระดับ A / B ตลอด
อัปเดตล่าสุด: 2026-10-18 (อาทิตย์) — รอบแรกของระบบ

---

## 1. สรุปสะสม

| ตัวชี้วัด | ระดับ A | ระดับ B | รวม |
| --- | --- | --- | --- |
| รอบค้นที่ทำ | 1 | 1 | 2 |
| ตำแหน่งที่เจอและคัดผ่าน | 3 | 2 | 5 |
| ใบที่ส่ง | 0 | 0 | 0 |
| ตอบกลับ | 0 | 0 | 0 |
| สัมภาษณ์ | 0 | 0 | 0 |

ยังไม่มีประวัติการส่งใบสมัครในระบบนี้ ตัวเลขทั้งหมดเริ่มนับจาก 2026-10-18

---

## 2. ใบที่ส่งแล้ว

| วันที่ส่ง | บริษัท | ตำแหน่ง | ระดับ | เรซูเม่เวอร์ชัน | สถานะ | ครบ 7 วันเมื่อ |
| --- | --- | --- | --- | --- | --- | --- |
| — | — | — | — | — | ยังไม่มี | — |

---

## 3. ประกาศที่เจอแล้ว (กันเสนอซ้ำ)

บันทึกไว้เพื่อไม่เสนอซ้ำในรอบวันถัดไป

| บริษัท | ตำแหน่ง | ระดับ | ป้าย (B) | ความตรง | สถานะ |
| --- | --- | --- | --- | --- | --- |
| Bank of Ayudhya / Krungsri Nimble | Junior Automation QA Engineer / Junior SDET | A | — | 5 | รอตรวจว่ายังเปิดอยู่ไหม |
| Quantium Technology | QA Automation Engineer (Junior-Mid) | A | — | 4 | รอยืนยันชื่อนายจ้าง |
| PERSOL Thailand | QA Automation (contract) | A | — | 4 | ยังไม่สมัคร |
| SS&C FinTech Services (Thailand) | Automation QA Tester (.NET Playwright) | A | — | 3 | ยังไม่สมัคร |
| Data Wow | Senior QA Automation | A | — | — | ตัดทิ้ง — ระดับ senior |
| Bangkok Bank | QA Engineer (manual + Robot Framework) | B | เขียว | 3 | ยังไม่สมัคร |
| G-Able | Software Tester (contract, hybrid) | B | เหลือง | 3 | ยังไม่สมัคร |
| Synergy Global Network | Tester (Lead) 50–65K | B | เหลือง | — | ตัดทิ้ง — ระดับ lead |

---

## 4. ข้อมูลพอร์ตที่ใช้อ้างอิง (ตัวเลขจริงจาก repo เท่านั้น)

ยืนยันจาก `README.md` ของ repo `nnewnerr/new.supakorn` ณ 2026-10-18

- 358 automated tests รวมทุก repo
- 10 Page Objects
- 7 CI workflows
- case study บั๊กจริง 8 เคส
- Test Strategy Document 1 ฉบับ (`TESTING.md` ใน sauce-demo-tests)

แยกรายโปรเจกต์

| repo | tests | หมายเหตุ |
| --- | --- | --- |
| Krungthon Air (private) | 96 E2E/API ใน 36 spec + 90 Firestore rules tests | 53 TC-ID, CI 4 workflow, daily soak กับ production |
| multitenant-booking-qa | 76 rules tests + 17 Playwright UI tests | เจอบั๊กจริง 2 ตัว, ชุด public-boundary 24 เคส |
| qa-automation | 63 tests ใน 8 Playwright projects | CI 4 shard, Playwright Test Agents, tag แยกชั้น |
| sauce-demo-tests | 16 tests | 4 Page Object บน BasePage, TESTING.md |

> หมายเหตุสำคัญ: บริบทในโปรไฟล์รูทีนระบุ "24 tests, 6 Page Objects, CI badge 2 อัน"
> ซึ่งเก่ากว่าของจริงมาก ทุก bullet ในเรซูเม่ให้ใช้ตัวเลขจากตารางนี้แทน

---

## 5. เรื่องค้างที่ต้องเคลียร์

1. **ยังไม่มีไฟล์เรซูเม่ในระบบ** — ทำให้ทำตาราง before/after ราย bullet ไม่ได้ ต้องได้ไฟล์ต้นฉบับ (เวอร์ชัน A และ B) ก่อนรอบอังคาร/พุธ
2. **จังหวัดฐานไม่ตรงกัน** — โปรไฟล์รูทีนว่า "นครปฐม" แต่ README ว่า "สมุทรสงคราม" มีผลกับการคัดงาน onsite กรุงเทพฯ
3. **เปิดหน้าประกาศโดยตรงไม่ได้** — network policy ของ session บล็อก th.jobsdb.com, jobthai.com, linkedin.com (CONNECT tunnel 403) ยืนยันวันที่ลงประกาศและลิงก์รายตัวไม่ได้ ต้องเปิดเองหรือวางลิงก์ประกาศมาให้
