# P2W INTERPLUS - Engineering Website

## Architecture รวม
ดู `C:\Users\witta\OneDrive\Claude AI Backup\P2W-ARCHITECTURE.md`

## Project Overview
เว็บไซต์บริษัทวิศวกรรม P2W INTERPLUS CO.,LTD. — เป็นส่วนหนึ่งของ P2W Hub
- **Live URL**: https://p2winterplus.com/engineer ✅
- **GitHub Pages**: https://p2winterplus-oss.github.io/P2W-Engineer/ (origin)
- **Repo**: https://github.com/p2winterplus-oss/P2W-Engineer.git
- **Hosted**: GitHub Pages (free, static) — ไม่ย้ายไป Railway เพราะไม่มี backend
- **Stack**: HTML + Tailwind CSS CDN + Vanilla JavaScript (single file: index.html)

## Design System
- **Theme**: Dark/Light mode toggle (localStorage)
- **Primary color**: Bronze/Champagne `#C5A880` (`brand-bronze`)
- **Dark bg**: Obsidian `#0D0D0C` (`brand-dark`)
- **Light bg**: Warm stone `#F9F8F6` (`brand-lightBg`)
- **Fonts**: Playfair Display (serif headings) + Prompt (body)
- **Style**: Luxury architectural fine-line aesthetic

## Page Structure (Top → Bottom)
1. **Header** — Logo (w-16) + nav + dark mode toggle + "ขอคำปรึกษา" CTA button → `#consultation-wizard`
2. **Hero** — Background image + overlay + Headline + metrics (15+ ปี / 45+ วิศวกร / 1,200+ โครงการ) + verification card
3. **Services (5 Pillars)** — Tab switcher: โยธา / โซล่า / เครื่องกล / ที่ปรึกษา / รับรอง + pricing cards
4. **How We Work** — 5-step process with circle icons + connecting line
5. **Why Choose Us** — Full-width bg image (`WhyChooseUs.png`) + gradient overlay + 4 จุดเด่น (2x2 grid)
6. **CTA Banner** — Dark bg + "มีโครงการที่ต้องการคำปรึกษา?" + ปุ่ม "ขอคำปรึกษา" → `#consultation-wizard`
7. **Consultation Wizard** — id=`consultation-wizard`, 3-step form (service → project details → contact + file upload)
8. **Portfolio** — 4 cards (2x2 grid) พร้อมรูปจริง
9. **Footer** — Logo (w-24) + links + contact info + Line OA

## Key Files
- `index.html` — เว็บไซต์หลัก (single file)
- `boq/index.html` — **ระบบ BOQ / ใบเสนอราคา ภายในองค์กร** (ดูหัวข้อ BOQ Tool ด้านล่าง)
- `logo.png` — P2W INTERPLUS logo (dark navy on white, dark mode: CSS class `.logo-glow` — outer stroke 1px สีบรอนซ์ `#C5A880` ด้วย drop-shadow 8 ทิศทาง, ใช้ทั้ง header w-16 และ footer w-24)
- `WhyChooseUs.png` — background image สำหรับ section Why Choose Us
- `robots.txt` — อนุญาต bot ทุกเจ้า รวม AI crawlers ✅
- `llms.txt` — สรุปข้อมูลบริษัทสำหรับ LLM/AI อ่านโดยตรง ✅

## Portfolio Cards (2x2 grid)
- **Card 01**: อาคารสำนักงาน 8 ชั้น (`public/engineer-01.png`) — STRUCTURAL CIVIL
- **Card 02**: บ้านพักอาศัยหรู 3 ชั้น (`public/engineer-02.png`) — STRUCTURAL CIVIL
- **Card 03**: Solar Rooftop 50kW โรงงาน (`public/solar-factory.png`) — GREEN ENERGY SOLAR, คืนทุน 3-4 ปี
- **Card 04**: Solar Rooftop 5kW บ้าน (`public/solar-home.png`) — GREEN ENERGY SOLAR, ลดค่าไฟ 60-80%
- **Card 05**: รับออกแบบ/วิเคราะห์/ตรวจสอบโครงสร้าง (`public/engineering-design.png`) — STRUCTURAL DESIGN

## Copy / ข้อความสำคัญ (ล่าสุด)
- **Service Tab 3**: "วิศวกรรมเครื่องกลและระบบอุตสาหกรรม" — ออกแบบ ตรวจสอบ ติดตั้งระบบอาคาร โรงงาน HVAC และยานยนต์
- **How We Work ขั้นตอน 2**: "สำรวจ & วิเคราะห์ (Site Survey & Feasibility Study)"
- **How We Work ขั้นตอน 5**: "ตรวจสอบ & ส่งมอบ (QA/QC & Commissioning)"
- **Why Choose Us**: "ทุกขั้นตอนผ่านการประเมินความเสี่ยงและออกแบบโครงสร้างโดย วิศวกรวิชาชีพ (สามัญ/วุฒิวิศวกร) ที่ได้รับใบอนุญาตอย่างถูกต้อง"

## Consultation Wizard (3 steps)
**Step 1 — เลือกบริการ**
- งานโยธาและโครงสร้าง
- ระบบพลังงานโซล่าร์เซลล์
- ออกแบบและติดตั้งระบบเครื่องกล / ระบบอุตสาหกรรม ← อัปเดตแล้ว
- ที่ปรึกษาโครงการ
- รับรองแบบและตรวจสอบ

**Step 2 — รายละเอียดโครงการ** ← ชื่อหัวข้ออัปเดตแล้ว
- placeholder: "เช่น ก่อสร้างอาคารพาณิชย์ 3 ชั้น, ติดตั้ง Solar Rooftop โรงงาน 50kW, ตรวจสอบโครงสร้างอาคารเก่า"

**Step 3 — ข้อมูลติดต่อ** ← อัปเดตเพิ่ม 2 ช่อง
- ผู้ติดต่อ * (เดิม: "นามผู้ติดต่อ")
- หมายเลขโทรศัพท์ *
- บริษัท/หน่วยงาน ← ใหม่
- Line ID ← ใหม่
- อีเมล (ถ้ามี)
- แนบไฟล์รูปภาพ/แบบแปลน (ถ้ามี)

## BOQ / Quotation Tool (ระบบภายใน) 🔒
ไฟล์: `boq/index.html` — หน้าเดียวจบ (HTML + Tailwind CDN + Vanilla JS)

**URL**
- Live: https://p2winterplus.com/engineer/boq/
- GitHub Pages: https://p2winterplus-oss.github.io/P2W-Engineer/boq/

**การเข้าถึง (ซ่อนจากลูกค้า)**
- **ปุ่มลับ**: ในหน้าเว็บหลัก footer บรรทัดลิขสิทธิ์ — คลิกที่ตัวเลข **"2026"** (`&copy; 2026 P2W INTERPLUS...` บรรทัด ~1167 ใน index.html) เป็น `<a href="boq/">` แบบไม่มีเส้นใต้/ไม่เปลี่ยนสี/`cursor:default`
- `<meta name="robots" content="noindex, nofollow">` — ไม่ขึ้นใน Google
- ไม่มี link อื่นชี้เข้าหน้านี้เลย

**Login & Session**
- รหัสผ่าน: `#Aveo9872` (hardcode ตัวแปร `PASSWORD` ในไฟล์)
- ไม่ใช้ localStorage/sessionStorage เก็บสถานะ login → **รีเฟรช / วาง URL ใหม่ / ปิดแท็บ = ต้อง login ใหม่ทุกครั้ง**
- Auto logout เมื่อไม่มี activity 30 นาที (`IDLE_LIMIT_MS`) — reset timer เมื่อ click/keydown/mousemove/input
- มีนาฬิกานับถอยหลังนาทีที่เหลือบน top bar

**Templates 6 แบบ** (ตัวแปร `TEMPLATES` — มีรายการ + ราคาต่อหน่วยตัวอย่างครบทุกอัน)
| key | ชื่อ | หมายเหตุ |
|---|---|---|
| `civil` | งานโครงสร้าง / อาคาร | 4 หมวด: ฐานราก, เสา-คาน, พื้น-หลังคา, สถาปัตยกรรม |
| `solarFactory` | Solar Rooftop โรงงาน | default 50 kWp, 3 หมวด |
| `solarHome` | Solar Rooftop บ้าน | default 5 kWp, 2 หมวด |
| `hvac` | ระบบ HVAC / เครื่องกล | Chiller, AHU, ท่อลม, BMS |
| `renovate` | ซ่อมแซม / ต่อเติม | รื้อถอน, เสริมกำลัง, ต่อเติม |
| `blank` | เอกสารเปล่า | เริ่มจากศูนย์ |

**ฟีเจอร์**
- ตาราง BOQ แก้ไข/เพิ่ม/ลบ ได้ทั้งรายการและหมวดงาน คำนวณ real-time
- สูตรราคา: Overhead % + Profit % + VAT % (ปรับได้ทุกช่อง, default 10 / 8 / 7)
- **Solar calculator** (แสดงเฉพาะ template โซล่าร์): กรอก kWp + ค่าไฟ/หน่วย → ผลิตไฟ/เดือน, ประหยัด/ปี, ระยะเวลาคืนทุน (สูตร: kWp × 4.2 ชม./วัน × 30 วัน)
- บันทึก draft ลง `localStorage` key `p2w_boq_drafts` (เก็บเฉพาะเครื่องนั้น ไม่ sync ข้ามเครื่อง) → เปิดย้อนหลัง/ลบได้จากหน้า template
- **Export PDF** ผ่าน `window.print()`

**เอกสาร Print (สำคัญ)**
- ตอน print จะซ่อน `#loginScreen`, `#templateScreen`, `#editorScreen`, `.no-print` ทั้งหมด แล้วโชว์เฉพาะ `#printArea`
- ขนาด A4, margin 16mm 14mm
- **ซ่อนกำไรจากลูกค้า** — ไม่แสดง Profit แยก แต่รวมเข้ากับ Overhead เป็นบรรทัดเดียวชื่อ "ค่าดำเนินการ" (`fmt(overhead + profit)`)
- Layout: letterhead P2W + เลขที่/วันที่ → โครงการ/ลูกค้า → ตารางรายการ → สรุปราคา (รวมเป็นเงิน / ค่าดำเนินการ / VAT / ราคารวมสุทธิ) → ช่องลายเซ็น ผู้เสนอราคา + ผู้อนุมัติ

## Email Integration
- **Service**: Web3Forms (free, 250 submissions/month)
- **API Key**: `c5363896-f578-4dd8-ad46-f481f5514982`
- **Destination**: `pm.p2w.interplus@gmail.com`
- **Trigger**: Wizard form step 3 submit → sends name, phone, company, lineId, email, service type, project details, attachment

## SEO (ทำแล้วครบ ✅)
- `<title>` — มีคีย์เวิร์ดหลัก
- `<meta name="description">` + `<meta name="keywords">`
- `<link rel="canonical">`
- Open Graph (og:title, og:description, og:image, og:url)
- Twitter Card
- `<meta name="ai-content-declaration">` + link to llms.txt
- JSON-LD Structured Data (ProfessionalService + OfferCatalog 4 บริการ)

## Contact Info (in footer)
- Phone: 088-788-8364
- Email: p2w.interplus@gmail.com
- Address: 49/306 ซ.นิมิตใหม่40 ถ.นิมิตใหม่ แขวงสามวาตะวันออก เขตคลองสามวา กรุงเทพฯ
- Line OA: https://lin.ee/QJax26d

## Domain & Routing
- **Cloudflare Worker**: `p2w-engineer` — route `p2winterplus.com/engineer*` → GitHub Pages
- Worker rewrite `src="..."` ให้ชี้กลับ GitHub Pages origin อัตโนมัติ
- ⚠️ ต้องเช็คว่า Worker route ครอบ `/engineer/boq/` ด้วยหรือไม่ (pattern `engineer*` ควรครอบอยู่แล้ว แต่ยังไม่ได้ verify)

## Tracking & Data Plan
- **Visitor tracking**: Google Analytics — ยังไม่ได้ทำ (ต้องเพิ่ม script tag)
- **Form → Google Sheet**: Google Apps Script — ยังไม่ได้ทำ
- **Form email**: Web3Forms ✅ ทำงานอยู่แล้ว

## What's Done ✅
- Full page layout with all sections
- Dark/Light mode toggle
- 5-service tab switcher with pricing (tab 3 อัปเดต copy เป็น HVAC/Industrial)
- How We Work 5-step section + English subtitle ขั้นตอน 2 และ 5
- Why Choose Us section — อัปเดตข้อความวิศวกรวิชาชีพ
- CTA banner → `#consultation-wizard`
- 3-step consultation wizard (step 3 เพิ่มช่อง บริษัท/หน่วยงาน + Line ID)
- Responsive mobile menu
- Logo `.logo-glow` — bronze 1px outer stroke dark mode
- Hero section background image with overlay
- Deployed on GitHub Pages + Live via Cloudflare Worker
- Portfolio 5 cards (2x2+1) พร้อมรูปจริง (engineer-01, engineer-02, solar-factory, solar-home, engineering-design)
- `robots.txt` — allow all bots + AI crawlers (GPTBot, ClaudeBot, PerplexityBot, Meta AI)
- `llms.txt` — AI-readable site summary (บริการ ราคา ผลงาน ติดต่อ)
- SEO meta tags ครบ (description, keywords, OG, Twitter Card, JSON-LD structured data)
- **ระบบ BOQ / ใบเสนอราคา ภายในองค์กร** (`boq/index.html`) — login, 6 templates, คำนวณราคา, Solar payback, save draft, export PDF
- ปุ่มลับเข้าหน้า BOQ ที่ตัวเลข "2026" ใน footer

## What's Missing / TODO ❌
- "เกี่ยวกับเรา" (About Us) section — team, company background
- Testimonials / client reviews section
- Google Analytics — เพิ่ม script tag
- Google Apps Script — เชื่อม form → Google Sheet
- Line OA chat widget (floating button)
- Portfolio filter buttons (โยธา/โซล่า) not yet functional
- Mobile nav auto-close after link click
- Header/Footer: link กลับ P2W Main (`/`) — ยังไม่ได้ใส่
- Submit Google Search Console (ต้องทำเองใน browser)

### TODO ฝั่ง BOQ Tool
- ยังไม่ได้ทดสอบ print จริงบนเบราว์เซอร์ (ลองกด Export PDF ดูว่า layout ตรงไหม)
- Draft เก็บเฉพาะเครื่อง — ถ้าอยาก sync ข้ามเครื่องต้องต่อ Google Sheets / Firebase
- ยังไม่มีระบบเลขที่ใบเสนอราคาแบบ running number (ตอนนี้ random 4 หลัก)
- ยังไม่มีหน้า "สรุปค่าใช้จ่าย" / "วิเคราะห์คืนทุน" แยก (Solar calc อยู่ในหน้า editor แล้ว)
- ราคาต่อหน่วยใน template เป็นราคาตัวอย่าง — ควรอัปเดตเป็นราคาจริงของบริษัท
- ยังไม่มี logo P2W ในหัวเอกสาร print (ตอนนี้เป็นข้อความอย่างเดียว)
