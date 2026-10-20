# AGENTS.md — P2W Engineer website

> สำหรับ Codex / AI agent อื่นๆ — **อ่าน `CLAUDE.md` ก่อนเริ่มงานทุกครั้ง** (มีรายละเอียดเต็ม: โครงสร้างหน้า, บทความ, SEO, TODO)
> ไฟล์นี้สรุปกฎที่ห้ามพลาด ถ้าอัปเดตข้อมูลโปรเจกต์ ให้แก้ทั้ง `CLAUDE.md` และไฟล์นี้ให้ตรงกัน

## โปรเจกต์
- เว็บวิศวกรรมของ P2W INTERPLUS CO.,LTD. — static site (HTML + Tailwind CDN + Vanilla JS) ไม่มี build step ไม่มี backend
- Live: https://p2winterplus.com/engineer (ผ่าน Cloudflare Worker) · Origin: GitHub Pages `p2winterplus-oss/P2W-Engineer` branch `main`
- Deploy = `git push origin main` แล้วรอ ~1 นาที

## ไฟล์หลัก
- `index.html` — หน้าเว็บหลักทั้งหมด (single file)
- `articles/index.html` — หน้ารวม + หน้าอ่านบทความ (`?id=<id>`)
- `articles/articles.json` — ข้อมูลบทความ `{id, title, category, date, author, cover, excerpt, content:[{type:p|h|img, text|src, caption}]}`
- `articles/editor.html` — editor ภายใน (มีรหัสผ่าน, noindex) เผยแพร่ผ่าน GitHub Contents API
- `llms.txt`, `robots.txt` — สำหรับ SEO / AI crawler

## ⚠️ กฎที่ต้องทำตาม
1. **Cloudflare Worker rewrite `src="`**: ทุก `src="X"` ที่ไม่ขึ้นต้น `http` จะโดนแปะ `https://p2winterplus-oss.github.io/P2W-Engineer/` ข้างหน้า — รวมถึงข้อความใน `<script>` ด้วย
   - รูปใน repo บนหน้าแรก: ใช้ `src="logo.png"` (relative จาก root repo)
   - รูปที่สร้างด้วย JS: **ห้ามมีข้อความ `src="` ในโค้ด** ใช้ `data-cover="..."` แล้วตั้ง `img.src = ...` (ดู `hydrateImages()` ใน `articles/index.html`)
2. **ลิงก์ข้ามหน้า** ต้องเป็น absolute `/engineer/...` (หน้าแรกโหลดที่ `/engineer` ไม่มี `/` ท้าย ลิงก์ relative จะหลุดเป็น 404)
3. **ห้ามใส่/ขอ secret ในไฟล์หรือแชท** — GitHub token ของ editor เก็บใน localStorage ของเครื่องผู้ใช้เท่านั้น
4. **เนื้อหาบทความ**: ออกในนามวิศวกรมีใบ กว. — ตัวเลขกฎหมาย/โครงการรัฐต้องอ้างแหล่งทางการ ถ้าไม่แน่ใจให้เขียนให้ผู้อ่านเช็คกับหน่วยงาน อย่าแต่งตัวเลขเอง
5. หลังแก้ `articles.json` ให้ validate JSON (`python -c "import json;json.load(open('articles/articles.json',encoding='utf-8'))"`) และเช็คว่า `id` ไม่ซ้ำ
6. Commit แล้ว push ทุกครั้ง ก่อนเริ่มงานให้ `git pull` (ทำงานหลายเครื่อง)

## ข้อมูลติดต่อปัจจุบัน
- โทร 088-788-8364 · อีเมลบนเว็บ adm.p2winterplus@gmail.com
- Line OA (ฝั่งวิศวกรรม): https://lin.ee/5u6O7cw
- ฟอร์มส่งอีเมลผ่าน Web3Forms → pm.p2w.interplus@gmail.com

## ภาษา
ผู้ใช้สื่อสารภาษาไทย — ตอบเป็นภาษาไทย
