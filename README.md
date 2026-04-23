# 🎡 ระบบวงล้อสุ่มชื่อผู้โชคดี
## Lucky Draw Wheel System

ระบบสุ่มชื่อผู้โชคดีแบบวงล้อ พร้อมระบบจัดการ Event และฐานข้อมูล Supabase

![Lucky Draw Wheel](https://img.shields.io/badge/version-1.0.0-blue)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?logo=supabase&logoColor=white)

---

## ✨ Features

### 🎯 ฟีเจอร์หลัก
- ✅ **วงล้อสุ่มชื่อแบบ Interactive** - Animation ที่ smooth พร้อม Confetti effect
- ✅ **จัดการผู้เข้าร่วม** - เพิ่ม/ลบ/แสดงรายชื่อผู้เข้าร่วม
- ✅ **จัดการ Event** - สร้าง/แก้ไข/ลบ Event พร้อมรายละเอียด
- ✅ **บันทึกผลการสุ่ม** - เก็บประวัติผู้โชคดีในฐานข้อมูล
- ✅ **Export รูปภาพ** - ดาวน์โหลดข้อมูลผู้โชคดีเป็น PNG
- ✅ **Responsive Design** - รองรับทุกขนาดหน้าจอ (Desktop, Tablet, Mobile)

### 🎨 Design Highlights
- Gradient ม่วง-ฟ้าสวยงาม
- วงล้อ 8 สีสลับกัน
- Animation แบบ Cubic Ease-out
- Confetti effect เมื่อได้ผู้โชคดี
- Modal popup แสดงผลผู้ชนะ

---

## 🚀 Quick Start

### 1. ติดตั้ง Supabase

#### สร้าง Project ใน Supabase
1. ไปที่ [Supabase.com](https://supabase.com)
2. สร้าง account และ project ใหม่
3. รอจนกว่า project จะพร้อมใช้งาน

#### รัน SQL Script
1. ไปที่ **SQL Editor** ใน Supabase Dashboard
2. คัดลอกโค้ดจากไฟล์ `setup-database.sql`
3. รัน script เพื่อสร้างตารางทั้ง 3 ตาราง

#### ดึง Credentials
1. ไปที่ **Settings** → **API**
2. คัดลอก:
   - `Project URL`
   - `anon/public key`

### 2. แก้ไขไฟล์ HTML

เปิดไฟล์ `lucky-draw-wheel.html` และแก้ไขบรรทัดที่ 659-660:

```javascript
const SUPABASE_URL = 'YOUR_SUPABASE_URL_HERE';
const SUPABASE_KEY = 'YOUR_SUPABASE_ANON_KEY_HERE';
```

### 3. เปิดใช้งาน

#### วิธีที่ 1: เปิดไฟล์โดยตรง
- Double-click ไฟล์ `lucky-draw-wheel.html`
- เว็บบราวเซอร์จะเปิดขึ้นมาพร้อมใช้งาน

#### วิธีที่ 2: Deploy บน GitHub Pages
1. สร้าง repository ใหม่บน GitHub
2. อัปโหลดไฟล์ `lucky-draw-wheel.html`
3. ไปที่ **Settings** → **Pages**
4. เลือก **main branch** และ **root folder**
5. เข้าใช้งานที่: `https://[username].github.io/[repo]/lucky-draw-wheel.html`

---

## 📖 วิธีใช้งาน

### สร้าง Event และสุ่มผู้โชคดี

#### 1. สร้าง Event
1. กรอก **ชื่อการแข่งขัน/กิจกรรม** (เช่น "งานสุ่มรางวัล Q1/2024")
2. กรอก **รายละเอียด Event** (optional)
3. กดปุ่ม **💾 บันทึก Event**

#### 2. เพิ่มผู้เข้าร่วม
1. กรอก **ชื่อ**, **นามสกุล**, **หน่วยงาน**
2. กดปุ่ม **➕ เพิ่มผู้เข้าร่วม**
3. ทำซ้ำจนครบทุกคน
4. ชื่อจะแสดงบนวงล้ออัตโนมัติ

#### 3. หมุนวงล้อ
1. กดปุ่ม **🎲 หมุนวงล้อ**
2. รอ 5 วินาทีให้วงล้อหมุน
3. Confetti จะระเบิดเมื่อได้ผู้โชคดี
4. Modal จะแสดงข้อมูลผู้ชนะ

#### 4. Export ผลลัพธ์
1. กดปุ่ม **📸 Export เป็นรูปภาพ**
2. ไฟล์ PNG จะถูกดาวน์โหลดอัตโนมัติ
3. ชื่อไฟล์: `ผู้โชคดี_[ชื่อ]_[นามสกุล].png`

### จัดการข้อมูล

#### แก้ไข Event
1. เลือก Event จาก dropdown
2. แก้ไขข้อมูลที่ต้องการ
3. กดปุ่ม **💾 บันทึก Event**

#### ลบ Event
1. เลือก Event ที่ต้องการลบ
2. กดปุ่ม **🗑️ ลบ Event**
3. ยืนยันการลบ (จะลบผลการสุ่มที่เกี่ยวข้องด้วย)

#### ลบผู้เข้าร่วม
1. หาชื่อในรายการผู้เข้าร่วม
2. กดปุ่ม **ลบ** ด้านขวา
3. ยืนยันการลบ

#### สร้าง Event ใหม่
1. กดปุ่ม **➕ Event ใหม่**
2. ฟอร์มจะถูกเคลียร์
3. เริ่มกรอกข้อมูล Event ใหม่

---

## 🗄️ Database Schema

### ตาราง 1: `participants`
เก็บข้อมูลผู้เข้าร่วมทั้งหมด

| Column | Type | Description |
|--------|------|-------------|
| id | UUID | Primary Key (auto-generated) |
| first_name | TEXT | ชื่อ (required) |
| last_name | TEXT | นามสกุล (required) |
| department | TEXT | หน่วยงาน (required) |
| created_at | TIMESTAMP | วันเวลาที่สร้าง (auto) |

### ตาราง 2: `events`
เก็บข้อมูล Event/กิจกรรม

| Column | Type | Description |
|--------|------|-------------|
| id | UUID | Primary Key (auto-generated) |
| event_name | TEXT | ชื่อ Event (required) |
| event_description | TEXT | รายละเอียด Event |
| created_at | TIMESTAMP | วันเวลาที่สร้าง (auto) |

### ตาราง 3: `draw_results`
เก็บประวัติผลการสุ่ม

| Column | Type | Description |
|--------|------|-------------|
| id | UUID | Primary Key (auto-generated) |
| event_id | UUID | Foreign Key → events.id (CASCADE) |
| participant_id | UUID | Foreign Key → participants.id (CASCADE) |
| drawn_at | TIMESTAMP | วันเวลาที่สุ่ม (auto) |

---

## 🎨 Customization

### เปลี่ยนสีวงล้อ
แก้ไขบรรทัดที่ 662 ในไฟล์ HTML:

```javascript
const WHEEL_COLORS = [
    '#FF6B6B',  // แดง
    '#4ECDC4',  // เขียวมิ้นท์
    '#45B7D1',  // ฟ้า
    '#FFA07A',  // ส้ม
    '#98D8C8',  // เขียวอ่อน
    '#F7DC6F',  // เหลือง
    '#BB8FCE',  // ม่วง
    '#85C1E2'   // ฟ้าอ่อน
];
```

### ปรับเวลาหมุนวงล้อ
แก้ไขบรรทัดที่ 663:

```javascript
const SPIN_DURATION = 5000; // เวลาเป็น milliseconds (5000 = 5 วินาที)
```

### ปรับจำนวนรอบการหมุน
แก้ไขบรรทัดที่ 664-665:

```javascript
const MIN_SPINS = 5;  // รอบขั้นต่ำ
const MAX_SPINS = 8;  // รอบสูงสุด
```

---

## 📱 Mobile Support

### Optimized for Mobile
- ✅ Touch-friendly buttons (44px minimum)
- ✅ ป้องกัน iOS auto-zoom
- ✅ Safe area support
- ✅ Responsive canvas sizing
- ✅ No tap highlight

### Tested on
- iPhone (Safari)
- Android (Chrome)
- iPad (Safari)
- Desktop browsers (Chrome, Edge, Firefox)

---

## 🔒 Security Notes

### ⚠️ สำคัญ
- ระบบนี้เหมาะสำหรับ**ใช้งานภายในองค์กร**เท่านั้น
- `SUPABASE_KEY` ถูกฝังในโค้ด (anon key)
- RLS enabled แต่ allow all operations
- **ไม่แนะนำ**ให้เปิดให้สาธารณะเข้าถึง

### Recommendations
- ใช้งานบน intranet หรือ VPN
- เปลี่ยน RLS policies ถ้าต้องการความปลอดภัยสูงขึ้น
- ใช้ environment variables สำหรับ production

---

## 🛠️ Technical Stack

| Technology | Version | Purpose |
|------------|---------|---------|
| HTML5 | - | Structure & Canvas |
| CSS3 | - | Styling & Animations |
| JavaScript | ES6+ | Logic & Interactions |
| Supabase | v2 | Database (PostgreSQL) |
| Canvas Confetti | v1.6.0 | Celebration effect |
| html2canvas | v1.4.1 | Image export |

---

## 📂 Project Structure

```
lucky-draw-wheel/
├── lucky-draw-wheel.html    # Main application (single file)
├── setup-database.sql        # Supabase SQL script
└── README.md                 # This file
```

---

## 🐛 Troubleshooting

### ปัญหา: วงล้อไม่แสดง
- ตรวจสอบว่าเชื่อมต่อ Supabase สำเร็จหรือไม่
- เปิด Console (F12) ดู error messages
- ตรวจสอบว่า URL และ Key ถูกต้อง

### ปัญหา: ไม่สามารถบันทึกข้อมูล
- ตรวจสอบว่ารัน SQL script แล้วหรือยัง
- ตรวจสอบ RLS policies ใน Supabase
- ตรวจสอบว่า anon key มีสิทธิ์เพียงพอ

### ปัญหา: Export ไม่ทำงาน
- ตรวจสอบว่า html2canvas โหลดสำเร็จหรือไม่
- ลอง refresh หน้าเว็บ
- ตรวจสอบ popup blocker ของบราวเซอร์

---

## 📝 License

MIT License - ใช้งานและแก้ไขได้อย่างอิสระ

---

## 👨‍💻 Author

Created with ❤️ for your organization

---

## 🙏 Credits

- **Supabase** - Database as a Service
- **Canvas Confetti** - Celebration effects
- **html2canvas** - Screenshot capability
- **Anthropic Claude** - Development assistance

---

## 📞 Support

หากพบปัญหาหรือต้องการความช่วยเหลือ:
1. ตรวจสอบ Troubleshooting section
2. เปิด Issue บน GitHub
3. ติดต่อทีม IT ภายในองค์กร

---

**Happy Drawing! 🎉**
