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
8. **Portfolio** — 5 cards (2x2 + 1) พร้อมรูปจริง
9. **Footer** — Logo (w-24) + links + contact info + Line OA

## Key Files
- `index.html` — เว็บไซต์หลัก (single file)
- `logo.png` — P2W INTERPLUS logo (dark navy on white, dark mode: CSS class `.logo-glow` — outer stroke 1px สีบรอนซ์ `#C5A880` ด้วย drop-shadow 8 ทิศทาง, ใช้ทั้ง header w-16 และ footer w-24)
- `WhyChooseUs.png` — background image สำหรับ section Why Choose Us
- `robots.txt` — อนุญาต bot ทุกเจ้า รวม AI crawlers ✅
- `llms.txt` — สรุปข้อมูลบริษัทสำหรับ LLM/AI อ่านโดยตรง ✅

## Portfolio Cards (5 ใบ — 2x2 + 1)
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

## บทความ & ข่าวสาร (`articles/`)
- **หน้ารวม + หน้าอ่าน**: `articles/index.html` — URL `https://p2winterplus.com/engineer/articles/` (อ่านบทความ = `?id=<id>`)
- **ข้อมูล**: `articles/articles.json` — array ของบทความ `{id, title, category, date, author, cover, excerpt, content:[{type:p|h|img, text|src, caption}]}` เรียงใหม่สุดขึ้นก่อนอัตโนมัติ, อันใหม่สุดเป็น "บทความแนะนำ"
- **หมวด**: งานโครงสร้าง / โซล่าร์เซลล์ / ความรู้วิศวกรรม / งานออกแบบ / ต่อเติม & รีโนเวท / ข่าวบริษัท
- **ลิงก์ในเมนู**: "บทความ" อยู่ระหว่าง ผลงาน กับ เกี่ยวกับเรา (desktop + mobile)
- **Editor** 🔒: `articles/editor.html` — รหัส `Chev9872`, `noindex`, ไม่มีลิงก์สาธารณะชี้ไป
  - ปุ่ม **"🚀 เผยแพร่ทันที"** — เขียน `articles.json` ผ่าน GitHub Contents API (GET sha → unshift → PUT) ขึ้นเว็บใน 1-2 นาที
  - ต้องมี **GitHub fine-grained token** (Contents = Read and write, เฉพาะ repo P2W-Engineer) เก็บใน `localStorage` key `p2w_gh_token` ของเครื่องที่ใช้ — ตั้งค่าแล้วบนเครื่องของ user (อย่าให้ user วาง token ในแชท)
  - ปุ่ม "สร้างโค้ด (วางเอง)" เป็นทางสำรองไม่ต้องใช้ token
  - พิมพ์เนื้อหา: เว้นบรรทัด = ย่อหน้า, `##` = หัวข้อ, `[รูป]URL | คำบรรยาย` = แทรกรูป
- **วิธีเพิ่มบทความ 3 ทาง**: editor เผยแพร่เอง / editor สร้างโค้ดวางเอง / user พิมพ์ในแชทให้ Claude เขียน+push
- คู่มือ: `articles/README.md`
- ⚠️ 2 บทความ `solar-tax-deduction` และ `solar-government-subsidy` ยังมี `⚠️ [ต้องเติมข้อมูลจริง]` — ตัวเลข/เงื่อนไขโครงการรัฐต้องเช็คกับประกาศทางการก่อน

## BOQ / Quotation Tool — ย้ายออกจากโปรเจกต์นี้แล้ว 📦
- เคยอยู่ที่ `boq/index.html` (commit `d7a1f0d`) — **ลบออกแล้ว** เพราะจะย้ายไปโฮสต์ที่เว็บอื่น
- สำเนาไฟล์: `C:\Users\BD\OneDrive\Claude AI Backup\P2W-BOQ-Tool-backup.html`
- กู้จาก git ได้: `git show d7a1f0d:boq/index.html > boq.html`
- ระบบที่มีในไฟล์นั้น: login password, 6 templates (civil / solarFactory / solarHome / hvac / renovate / blank), คำนวณ Overhead+Profit+VAT, Solar payback calculator, save draft ลง localStorage, export PDF ผ่าน `window.print()`

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
- Line OA: https://lin.ee/5u6O7cw

## Domain & Routing
- **Cloudflare Worker**: `p2w-engineer` — route `p2winterplus.com/engineer*` → GitHub Pages
- Worker rewrite `src="..."` ให้ชี้กลับ GitHub Pages origin อัตโนมัติ

### ⚠️ กับดัก Worker (สำคัญมาก — เจอจริงแล้ว)
Worker ทำ **text-replace ดิบๆ ทั้งไฟล์ HTML**: ทุก `src="X"` ที่ X **ไม่ได้ขึ้นต้นด้วย `http`** จะถูกแปะ `https://p2winterplus-oss.github.io/P2W-Engineer/` ข้างหน้า — **รวมถึงใน `<script>` ด้วย**
- ❌ `src="${a.cover}"` ใน JS template → กลายเป็น `.../P2W-Engineer/${a.cover}` → รูปพัง
- ❌ `src="/engineer/logo.png"` → กลายเป็น `.../P2W-Engineer//engineer/logo.png` → พัง
- ✅ `src="logo.png"` (relative จาก root repo) → `.../P2W-Engineer/logo.png` ใช้ได้ (แบบที่หน้าแรกใช้)
- ✅ `src="https://..."` (URL เต็ม) → Worker ไม่แตะ
- ✅ **รูปที่สร้างด้วย JS** → ห้ามเขียน `src="` ในโค้ด ให้ใช้ `data-cover="..."` แล้ว set `img.src = ...` (property) แทน — ดู `hydrateImages()` ใน `articles/index.html`

### ลิงก์ข้ามหน้า
หน้าแรกโหลดที่ `/engineer` (ไม่มี `/` ท้าย) → ลิงก์ relative อย่าง `articles/` จะหลุดไป `/articles/` (404) — **ลิงก์ข้ามหน้าต้องใช้ `/engineer/...` แบบ absolute** (ใช้ได้บน custom domain เท่านั้น ลิงก์ github.io ตรงๆ ข้ามหน้าจะไม่ทำงาน ไม่เป็นไรเพราะลูกค้าใช้ domain)

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
- หน้าบทความ & ข่าวสาร + editor เผยแพร่เองผ่าน GitHub API (5 บทความตัวอย่าง)

## What's Missing / TODO ❌
- เติมข้อมูลจริงใน 2 บทความโครงการรัฐโซล่าร์ (ตอนนี้มี ⚠️ placeholder)
- ยังไม่ได้ลองกด "เผยแพร่ทันที" จาก editor จริงสักครั้ง
- "เกี่ยวกับเรา" (About Us) section — team, company background
- Testimonials / client reviews section
- Google Analytics — เพิ่ม script tag
- Google Apps Script — เชื่อม form → Google Sheet
- Line OA chat widget (floating button)
- Portfolio filter buttons (โยธา/โซล่า) not yet functional
- Mobile nav auto-close after link click
- Header/Footer: link กลับ P2W Main (`/`) — ยังไม่ได้ใส่
- Submit Google Search Console (ต้องทำเองใน browser)
