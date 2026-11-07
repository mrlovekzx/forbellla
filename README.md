# 🎟️ Love Ticket

เว็บตั๋วพิเศษให้แฟน กด "ใช้ตั๋ว" แล้วตั๋วจะถูกฉีกและหายไป
มีหลังบ้านสำหรับสร้าง / แก้ไข / คืน / ลบตั๋ว

- หน้าของเธอ: `/`
- หลังบ้าน: `/admin.html` (ใช้รหัสผ่านจาก `ADMIN_PASSWORD`)

## รันในเครื่อง
```bash
npm install
ADMIN_PASSWORD=รหัสของคุณ npm start      # Windows: ดับเบิลคลิก start.bat
```
เปิด http://localhost:3000

## อัพขึ้น GitHub
```bash
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/ชื่อคุณ/love-ticket.git
git push -u origin main
```
(หรือสร้าง repo บนเว็บ GitHub แล้วกด Add file → Upload files ลากไฟล์ทั้งหมดในโฟลเดอร์นี้ไปวาง)

## เปิดให้แฟนใช้จากมือถือ
GitHub Pages รันฝั่งหลังบ้าน (Node) ไม่ได้ ให้ deploy repo นี้ที่ [Render](https://render.com):
1. New → Blueprint → เลือก repo นี้ (อ่านค่าจาก `render.yaml`)
2. ตั้ง `ADMIN_PASSWORD` เป็นรหัสของคุณ
3. ได้ลิงก์แล้วส่งให้แฟนได้เลย

> ดิสก์ถาวรของ Render เป็นแผนเสียเงิน ถ้าใช้แผนฟรีข้อมูลอาจรีเซ็ตเมื่อ redeploy

## หมายเหตุ
- ข้อมูลตั๋วจริงเก็บที่ `data/tickets.json` (ไม่ถูกอัพขึ้น GitHub) ตั๋วตัวอย่างอยู่ใน `data/seed.json`
- ถ้าไม่ตั้ง `ADMIN_PASSWORD` จะใช้ `admin1234` ซึ่งควรเปลี่ยนก่อนใช้งานจริง
