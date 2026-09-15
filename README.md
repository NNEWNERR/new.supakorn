# สวัสดีครับ 👋 ผมศุภากร เศวตวงศ์สกุล (นิว)

### Automation QA Engineer | Playwright + TypeScript

ผมเขียน end-to-end test automation ที่ดูแลต่อได้จริงด้วย Page Object Model และให้ความสำคัญกับ **การออกแบบเทส** พอๆ กับโค้ดเทส ก่อนย้ายมาสาย QA ผมเป็น frontend developer อยู่ 1 ปี ซึ่งเป็นช่วงที่ได้เห็นกับตาว่าแอปพังด้วยสาเหตุอะไรบ้าง

- 🌍 อยู่จังหวัดสมุทรสงคราม
- 🎓 วศ.บ. (ต่อเนื่อง) เทคโนโลยีวิศวกรรมอิเล็กทรอนิกส์ — มจพ. วิทยาลัยเทคโนโลยีอุตสาหกรรม
- 🧪 ถนัด E2E automation, API testing, CI pipeline และการวางกลยุทธ์การทดสอบ
- 🎯 เป้าหมายถัดไป: SDET / QA Lead
- ✉️ newnertg@gmail.com

---

### 🛠 Tech Stack

**Testing & Automation**

![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat&logo=playwright&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Cypress](https://img.shields.io/badge/Cypress-17202C?style=flat&logo=cypress&logoColor=white)
![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=flat&logo=selenium&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat&logo=postman&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white)

**Development**

![Angular](https://img.shields.io/badge/Angular-DD0031?style=flat&logo=angular&logoColor=white)
![Ionic](https://img.shields.io/badge/Ionic-3880FF?style=flat&logo=ionic&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat&logo=tailwindcss&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat&logo=firebase&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)

---

### 🧪 ผลงานด้าน QA

| โปรเจกต์ | ครอบคลุมอะไร | Stack |
| --- | --- | --- |
| Krungthon Air — QA suite *(private — ระบบลูกค้า)* | **99 tests ใน 37 spec files** สำหรับแพลตฟอร์มจองคิวบน Firebase ที่ใช้งานจริง มี **53 test case ที่อ้างอิงกลับด้วย TC-ID** ครอบคลุม auth, การจอง, สิทธิ์การเข้าถึง, การจองชนกันแบบ concurrent, การแยกข้อมูลระหว่าง tenant, a11y, mobile responsive และการยิง API ตรงไปที่ Cloud Functions มี CI 3 workflow — รันตอน PR, แจ้งเตือนเข้า Discord และ **daily soak ยิงกับ production ทุกวัน** เพื่อจับ regression ภายใน 24 ชั่วโมง ไม่ต้องรอ PR ถัดไป | Playwright, TypeScript, Firebase, Angular |
| [qa-automation](https://github.com/NNEWNERR/qa-automation) | **31 tests ใน 7 Playwright projects** — API contract, UI, accessibility (axe-core), visual regression, smoke และ auth แยกตาม role ด้วย `storageState` CI รัน **4 shard ขนาน** แล้ว merge blob report กลับเป็นรายงาน HTML ฉบับเดียว เทสติด tag (`@smoke` `@regression` `@a11y` `@visual`) เลือกรันทีละชั้นได้ | Playwright, TypeScript, GitHub Actions |
| [sauce-demo-tests](https://github.com/NNEWNERR/sauce-demo-tests) | **16 tests** ครอบคลุม login, การเรียงสินค้า, ตะกร้า และ checkout พร้อม visual + accessibility check มี 4 Page Object บน `BasePage` ร่วมกัน และมี `TESTING.md` — เอกสารกลยุทธ์การทดสอบที่มีขอบเขต, risk matrix และ test pyramid | Playwright, TypeScript |

repo ของ Krungthon Air เก็บเป็น private เพราะเป็นระบบลูกค้าที่ใช้งานจริง — ยินดีเปิดให้ดูและอธิบายโครงสร้างเทส, การอ้างอิง TC-ID และ soak workflow ตอนสัมภาษณ์ครับ

**ภาพรวมผลงาน:** 146 automated tests · 10 Page Object · 5 CI workflow · เอกสารกลยุทธ์การทดสอบ 1 ฉบับ

**สิ่งที่ผมให้ความสำคัญมากกว่าจำนวนเทส**

- เทสที่ **skip แทนที่จะ fail** เมื่อ dependency ไม่พร้อม — เพื่อให้ "จอแดง" หมายถึงบั๊กจริงเสมอ ไม่ใช่ปัญหาสภาพแวดล้อม
- flake จากระบบภายนอก **บันทึกไว้ให้ชัด ไม่กลบด้วย retry** เพราะ retry ที่ใส่เพื่อให้ผ่านจะบังบั๊กจริงในเทสตัวเดียวกัน
- screenshot baseline ถือว่าผูกกับ OS เสมอ เพราะมันเป็นแบบนั้นจริงๆ

---

### 💼 ประสบการณ์

**Frontend Developer** — startup, 1 ปี
พัฒนาและส่งมอบฟีเจอร์ด้วย Angular, Ionic และ Tailwind CSS บน backend ที่เป็น Firebase

**Event Organizer / Project Coordinator** — ร้านนายกิจสติ๊กเกอร์
จัดทำเอกสารก่อนงาน, รายงานสรุปโปรเจกต์ และดูแลข้อมูลแบบสำรวจ

---

### 📚 กำลังศึกษาเพิ่มเติม

เทคนิคการออกแบบเทส — equivalence partitioning และ boundary value analysis, decision table และ state transition, risk-based testing, การเขียนรายงานบั๊ก และ exploratory testing

ใช้จริงไม่ใช่แค่ท่องจำ: เทสทุกตัวในชุดของผมเขียนขึ้นจากเทคนิคที่ระบุชื่อได้ ไม่ใช่การไล่คลิกไปเรื่อยๆ แล้วบันทึกไว้

---

### 🌐 ติดต่อ

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/NNEWNERR)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:newnertg@gmail.com)
[![Facebook](https://img.shields.io/badge/Facebook-1877F2?style=flat&logo=facebook&logoColor=white)](https://www.facebook.com/tgtongja)
