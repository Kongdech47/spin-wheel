# Commit Message Convention

ใช้รูปแบบ:

```text
<type>: <สรุปการเปลี่ยนแปลงแบบสั้น>
```

## Types

- `feat:` เพิ่มความสามารถใหม่
- `fix:` แก้ bug หรือพฤติกรรมที่ทำงานผิด
- `refactor:` ปรับโครงสร้างโค้ดโดยไม่เปลี่ยนความสามารถ
- `style:` ปรับ CSS, layout หรือ formatting โดยไม่เปลี่ยน logic
- `docs:` แก้ไข README, AGENTS หรือเอกสาร
- `test:` เพิ่มหรือแก้ไขการทดสอบ
- `chore:` งานดูแลโปรเจกต์ เช่น ปรับ config หรือ cleanup
- `perf:` ปรับปรุงประสิทธิภาพ

## ตัวอย่าง

```text
feat: add character image upload
fix: prevent spinning with empty slots
style: improve fantasy wheel colors
docs: update local setup guide
refactor: simplify IndexedDB helpers
chore: remove unused Docker files
```

## กติกา

- ใช้ภาษาอังกฤษแบบสั้นและชัดเจน
- เขียนเป็นคำกริยา เช่น `add`, `fix`, `update`, `remove`
- ไม่ใส่จุดปิดท้ายข้อความ
- หนึ่ง commit ควรมีหนึ่งเรื่องหลัก
- ห้ามใช้ข้อความกว้างเกินไป เช่น `update code` หรือ `แก้หลายอย่าง`
