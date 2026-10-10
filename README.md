# Student Management (Next.js CRUD)

ระบบจัดการข้อมูลนักศึกษา สร้างด้วย Next.js, Prisma และ SQLite
ทำได้ครบ 4 ฟังก์ชัน: ดูรายการ, เพิ่ม, แก้ไข, ลบ

## เทคโนโลยีที่ใช้

- Node.js
- Next.js (App Router) + TypeScript
- Tailwind CSS
- Prisma 7.10.0
- SQLite (better-sqlite3)

## วิธีการติดตั้ง

ต้องติดตั้ง Node.js (แนะนำเวอร์ชัน LTS) และ Git ก่อน

1. ดาวน์โหลดโปรเจกต์

```bash
git clone <URL ของ repository นี้>
cd <ชื่อโฟลเดอร์โปรเจกต์>
```

2. ติดตั้งแพ็กเกจ

```bash
npm install
```

3. สร้างไฟล์ `.env` ไว้ที่โฟลเดอร์นอกสุด (ระดับเดียวกับ package.json) แล้วใส่

```
DATABASE_URL="file:./dev.db"
```

4. สร้างฐานข้อมูลและ Prisma Client

```bash
npx prisma migrate dev
npx prisma generate
```

5. เปิดเซิร์ฟเวอร์

```bash
npm run dev
```

## วิธีการใช้งาน

เปิดเบราว์เซอร์ไปที่ http://localhost:3000/students

- ดูรายการ: เปิดหน้า /students จะเห็นตารางนักศึกษาทั้งหมด
- เพิ่มนักศึกษา: กดปุ่ม "เพิ่มนักศึกษา" กรอกข้อมูลแล้วกด "บันทึก"
- แก้ไข: กดปุ่ม "แก้ไข" ที่แถวของนักศึกษา แก้ข้อมูลแล้วกด "บันทึกการแก้ไข"
- ลบ: กดปุ่ม "ลบ" แล้วกดยืนยันในกล่องข้อความ

หมายเหตุ: รหัสนักศึกษาต้องไม่ซ้ำกัน