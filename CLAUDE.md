# P2W INTERPLUS - Engineering Website

## Architecture รวม
ดู `C:\Users\witta\OneDrive\Claude AI Backup\P2W-ARCHITECTURE.md`

## Project Overview
เว็บไซต์บริษัทวิศวกรรม P2W INTERPLUS CO.,LTD. — เป็นส่วนหนึ่งของ P2W Hub
- **Live URL**: https://p2winterplus-oss.github.io/P2W-Engineer/
- **URL หลัง domain พร้อม**: https://p2winterplus.com/engineer
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
2. **Hero** — Background image (Unsplash) + overlay + Headline + metrics (15+ ปี / 45+ วิศวกร / 1,200+ โครงการ) + verification card
3. **Services (5 Pillars)** — Tab switcher: โยธา / โซล่า / เครื่องกล / ที่ปรึกษา / รับรอง + pricing cards
4. **How We Work** — 5-step process with circle icons + connecting line
5. **Why Choose Us** — Full-width bg image (`WhyChooseUs.png`) + gradient overlay + 4 จุดเด่น (2x2 grid)
6. **CTA Banner** — Dark bg + "มีโครงการที่ต้องการคำปรึกษา?" + ปุ่ม "ขอคำปรึกษา" → `#consultation-wizard`
7. **Consultation Wizard** — id=`consultation-wizard`, 3-step form (service → project details → contact + file upload)
8. **Portfolio** — 3 project cards (placeholder gradients, no real photos yet)
9. **Footer** — Logo (w-24) + links + contact info + Line OA

## Key Files
- `index.html` — entire website (single file)
- `logo.png` — P2W INTERPLUS logo (dark navy on white, dark mode: CSS class `.logo-glow` — outer stroke 1px สีบรอนซ์ `#C5A880` ด้วย drop-shadow 8 ทิศทาง, ใช้ทั้ง header w-16 และ footer w-24)
- `WhyChooseUs.png` — background image สำหรับ section Why Choose Us

## Email Integration
- **Service**: Web3Forms (free, 250 submissions/month)
- **API Key**: `c5363896-f578-4dd8-ad46-f481f5514982`
- **Destination**: `pm.p2w.interplus@gmail.com`
- **Trigger**: Wizard form step 3 submit → sends name, phone, email, service type, project details, attachment

## Contact Info (in footer)
- Phone: 088-788-8364
- Email: p2w.interplus@gmail.com
- Address: 49/306 ซ.นิมิตใหม่40 ถ.นิมิตใหม่ แขวงสามวาตะวันออก เขตคลองสามวา กรุงเทพฯ
- Line OA: https://lin.ee/QJax26d

## What's Done ✅
- Full page layout with all sections
- Dark/Light mode toggle
- 5-service tab switcher with pricing
- How We Work 5-step section (fixed step 4 hover state)
- Why Choose Us section — full-width bg image + text overlay
- CTA banner — ปุ่ม "ขอคำปรึกษา" link ไป `#consultation-wizard`
- 3-step consultation wizard with file upload + email notification
- Responsive mobile menu
- Logo uploaded to repo + bronze 1px outer stroke dark mode (`.logo-glow` CSS class, drop-shadow 8 ทิศทาง)
- Hero section background image with overlay
- ปุ่ม "ขอคำปรึกษา" ทุกจุด (header, mobile, CTA) scroll ไป wizard
- Deployed on GitHub Pages
- Portfolio อัปเดตเป็น 4 cards (2x2 grid) พร้อมรูปจริง:
  - Card 01: Structural Civil — ต่อเติมคฤหาสน์ราชพฤกษ์ (gradient placeholder)
  - Card 02: Solar Rooftop 50kW โรงงาน (`public/solar-factory.png`) คืนทุน 3-4 ปี
  - Card 03: Solar Rooftop 5kW บ้าน (`public/solar-home.png`) ลดค่าไฟ 60-80%
  - Card 04: รับออกแบบ/วิเคราะห์/ตรวจสอบโครงสร้าง (`public/engineering-design.png`)

## Tracking & Data Plan
- **Visitor tracking**: Google Analytics (เพิ่ม script tag ใน `<head>`) — ฟรี ดู dashboard ได้
- **Form → Google Sheet**: ใช้ Google Apps Script แทน Zapier — ฟรีไม่จำกัด ส่ง form submission เข้า Sheet อัตโนมัติ
- **Form email**: Web3Forms (มีอยู่แล้ว) คงไว้ควบคู่กัน

## Phase 2 (หลังซื้อ domain p2winterplus.com)
- เพิ่ม link กลับ Main Hub (`/`) ใน Header
- เพิ่ม link ไปหน้าอื่นๆ ของ P2W ใน Footer
- เปลี่ยน URL เป็น p2winterplus.com/engineer ผ่าน Cloudflare

## What's Missing / TODO ❌
- รูปจริงสำหรับ Card 01 Structural Civil (ยังเป็น gradient placeholder)
- "เกี่ยวกับเรา" (About Us) section — team, company background
- Testimonials / client reviews section
- Custom domain (currently on .github.io) — รอซื้อ p2winterplus.com
- Google Analytics — เพิ่ม script tag (ยังไม่ได้ทำ)
- Google Apps Script — เชื่อม form → Google Sheet (ยังไม่ได้ทำ)
- SEO meta tags (og:image, description, keywords)
- Line OA chat widget (floating button)
- Portfolio filter buttons (โยธา/โซล่า) not yet functional
- Mobile nav auto-close after link click
- Header: link กลับ P2W Main (รอ domain พร้อม)
