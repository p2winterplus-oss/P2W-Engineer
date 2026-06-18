# P2W INTERPLUS - Engineering Website

## Project Overview
เว็บไซต์บริษัทวิศวกรรม P2W INTERPLUS CO.,LTD.
- **Live URL**: https://p2winterplus-oss.github.io/P2W-Engineer/
- **Repo**: https://github.com/p2winterplus-oss/P2W-Engineer.git
- **Hosted**: GitHub Pages (free, static)
- **Stack**: HTML + Tailwind CSS CDN + Vanilla JavaScript (single file: index.html)

## Design System
- **Theme**: Dark/Light mode toggle (localStorage)
- **Primary color**: Bronze/Champagne `#C5A880` (`brand-bronze`)
- **Dark bg**: Obsidian `#0D0D0C` (`brand-dark`)
- **Light bg**: Warm stone `#F9F8F6` (`brand-lightBg`)
- **Fonts**: Playfair Display (serif headings) + Prompt (body)
- **Style**: Luxury architectural fine-line aesthetic

## Page Structure (Top → Bottom)
1. **Header** — Logo (w-16) + nav + dark mode toggle + "ขอคำปรึกษา" CTA button
2. **Hero** — Headline + metrics (15+ ปี / 45+ วิศวกร / 1,200+ โครงการ) + verification card
3. **Services (5 Pillars)** — Tab switcher: โยธา / โซล่า / เครื่องกล / ที่ปรึกษา / รับรอง + pricing cards
4. **How We Work** — 5-step process with circle icons + connecting line
5. **CTA Banner** — Dark bg + "มีโครงการที่ต้องการคำปรึกษา?" + button
6. **Consultation Wizard** — 3-step form (service → project details → contact + file upload)
7. **Portfolio** — 3 project cards (placeholder gradients, no real photos yet)
8. **Footer** — Logo (w-24) + links + contact info + Line OA

## Key Files
- `index.html` — entire website (single file)
- `logo.png` — P2W INTERPLUS logo (dark navy on white, needs dark mode handling)

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
- How We Work 5-step section
- CTA banner
- 3-step consultation wizard with file upload + email notification
- Responsive mobile menu
- Logo uploaded to repo
- Deployed on GitHub Pages

## What's Missing / TODO ❌
- Real project photos for portfolio cards (currently placeholder gradients)
- Logo visibility fix on dark mode (dark navy logo on dark bg)
- "เกี่ยวกับเรา" (About Us) section — team, company background
- Testimonials / client reviews section
- Custom domain (currently on .github.io)
- Google Analytics / tracking
- SEO meta tags (og:image, description, keywords)
- Line OA chat widget (floating button)
- Portfolio filter buttons (โยธา/โซล่า) not yet functional
- Mobile nav auto-close after link click
