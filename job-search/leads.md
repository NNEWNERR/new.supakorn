# Leads — ประกาศที่เห็นแล้วแต่ยังไม่ผ่านเกณฑ์ 7 วัน

ไฟล์นี้กันไม่ให้เสนอซ้ำ และกันไม่ให้ขุดประกาศเก่ามานับเป็นโควตา
**ยังไม่มีรายการใดในนี้ผ่านเกณฑ์ "ลงหรืออัปเดตภายใน 7 วัน"**

ตรวจเมื่อ 2026-10-28

| บริษัท | ตำแหน่ง | ระดับ | ที่ตั้ง / รูปแบบ | วันที่ประกาศ | ทำไมยังไม่เสนอ | แหล่ง |
|---|---|---|---|---|---|---|
| Synergy Global Network | Automated Tester (Playwright) | A | พระราม 3 · hybrid | **ไม่ระบุ** | ตรงมาก แต่ยืนยันวันที่ไม่ได้ เปิดหน้าประกาศตรงไม่ได้ | [JobThai company 180087](https://www.jobthai.com/en/company/180087) |
| Synergy Global Network | Tester (Lead) · 50,000–65,000 | — | ดินแดง | ไม่ระบุ | เป็นระดับ Lead เกินช่วงที่ควรสมัครตอนนี้ | JobThai |
| PERSOL Thailand | QA Automation Engineer (Cypress & Playwright) | A | จตุจักร · contract | 17 ก.ย. 2026 (41 วัน) | เกิน 7 วัน และ JD ระบุหน้าที่คุมทีม QA | [freehire](https://freehire.me/jobs/qa-automation-engineer-cypress-playwright-persol-wra3fqbm) |
| ISM Technologies | Senior QA Automation Engineer | A | กรุงเทพฯ | 1 ก.ค. 2026 (119 วัน) | เก่ามาก และเป็นระดับ Senior | [ismtech.net](https://www.ismtech.net/job/senior-qa-automation-engineer/) |
| ATA IT Limited | Senior QA Automation (SDET) | A | สาทร · hybrid | ไม่ระบุ | ระดับ Senior ยืนยันวันที่ไม่ได้ | JobsDB (เปิดไม่ได้) |
| EY Corporate Services | Automation QA Engineer — Mobile Banking (สัญญา 1 ปี) | A | กรุงเทพฯ | ไม่ระบุ | ยืนยันวันที่และ requirement ไม่ได้ | JobsDB (เปิดไม่ได้) |
| QA Hive | QA / Software Tester · 20,000–45,000 | B | ราชเทวี / บางนา / บางรัก | ไม่ระบุ | ยังไม่รู้ว่ามีทีม automation ไหม ติดป้ายไม่ได้ | JobsDB (เปิดไม่ได้) |
| เอพพิค คอนซัลติ้ง | Software QA / Software Tester · 25,500–53,500 | B | กรุงเทพฯ | ไม่ระบุ | เดียวกัน ยังติดป้ายเขียว/เหลือง/แดงไม่ได้ | JobBKK (เปิดไม่ได้) |
| (ไม่ระบุชื่อ) | Software Tester / QA บางกอกน้อย | B | บางกอกน้อย | 13 ต.ค. 2026 (15 วัน) | เกิน 7 วัน | [JobThai](https://www.jobthai.com/jobsearch/computer-it,qa-tester-software-tester/3) |

## ข้อจำกัดที่เจอในรอบนี้

session นี้เปิดเว็บไซต์หางานตรงไม่ได้ — `th.jobsdb.com`, `www.linkedin.com`, `www.glassdoor.com`
คืนค่า `ENOTFOUND` (โดเมนไม่อยู่ในรายการที่อนุญาตของ environment) เหลือแต่ผลค้นหาแบบรวม
ซึ่งบอกวันที่ลงประกาศไม่ได้ จึงยืนยันเกณฑ์ 7 วันไม่ได้เลยแม้แต่รายการเดียว

**ทางแก้ที่ต้องให้เจ้าของ session ทำ** — เพิ่มโดเมนเหล่านี้ใน network settings ของ environment:
`th.jobsdb.com`, `www.jobthai.com`, `www.linkedin.com`, `www.jobtopgun.com`,
`www.jobbkk.com`, `www.workventure.com`, `blognone.com`
