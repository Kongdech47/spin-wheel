# AGENTS.md

## ภาพรวมโปรเจกต์

Starlight Spin เป็นเว็บ static สำหรับสุ่มตัวละครด้วยวงล้อ ใช้เฉพาะ HTML, CSS และ Vanilla JavaScript ไม่มี build step, framework, backend หรือ Docker

## โครงสร้างและขอบเขต

- `index.html` เป็น markup หลักและส่วน modal
- `app.js` เป็น logic การหมุน การอัปโหลดภาพ การตั้งค่า และ IndexedDB
- `src/styles.css` เป็น visual design และ responsive layout
- ข้อมูลภาพเก็บใน browser IndexedDB ไม่ควรเพิ่ม backend โดยไม่จำเป็น

## แนวทางแก้ไข

- รักษาการใช้งานบน desktop และ mobile
- ใช้ภาษาและข้อความใน UI เป็นภาษาไทย เว้นแต่เป็น label ทางเทคนิคหรือ branding
- ตรวจสอบ input จำนวนช่องให้อยู่ในช่วง 2–24 และรอบหมุนอยู่ในช่วง 1–20
- ห้ามเปิดให้หมุนจนกว่าทุกช่องจะมีภาพ
- ตรวจสอบชนิดไฟล์และขนาดไฟล์ก่อนอ่านภาพ
- หลีกเลี่ยง dependency ใหม่ หากทำได้ด้วย browser API มาตรฐาน
- หลังแก้ไข `app.js` ให้ตรวจ syntax ด้วย `node --check app.js`
- ห้าม commit `node_modules`, `dist`, ไฟล์ชั่วคราว หรือข้อมูลส่วนตัว

## การทดสอบขั้นต่ำ

```bash
node --check app.js
python3 -m http.server 8000
```

ตรวจด้วย browser ว่าเพิ่ม/ลบภาพ, refresh แล้วยังมีข้อมูล, เปลี่ยนจำนวนช่อง, เปลี่ยนรอบหมุน และหมุนหาผู้ชนะได้

## Commit message

ใช้รูปแบบ Conventional Commits ตามรายละเอียดใน `COMMIT_CONVENTION.md` ตัวอย่างเช่น `feat: add character upload` หรือ `fix: prevent spinning with empty slots`
