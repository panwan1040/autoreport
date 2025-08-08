# 📸 ระบบใส่รูปลงรายงานก่อสร้าง (Site Photo Reporter)

ระบบจัดการรูปภาพสำหรับงานก่อสร้างที่ช่วยให้คุณอัปโหลดรูปภาพตามโปรเจ็กต์/จุด/ขั้นตอน และสร้างรายงาน Word (.docx) ได้อย่างง่ายดาย

## ✨ ฟีเจอร์ใหม่

### 🎯 Drag & Drop อัปโหลด
- **ลากวางไฟล์** - ลากไฟล์รูปภาพมาวางในพื้นที่ที่กำหนดได้เลย
- **Preview ไฟล์** - ดูไฟล์ที่เลือกก่อนอัปโหลด
- **อัปโหลดแบบ AJAX** - ไม่ต้องรีเฟรชหน้าเว็บ

### 🎨 UI/UX ที่ทันสมัย
- **Design ที่สวยงาม** - ใช้ Tailwind CSS และ Feather Icons
- **Animation** - การเคลื่อนไหวที่นุ่มนวลและสวยงาม
- **Responsive** - ใช้งานได้ดีทั้งมือถือและคอมพิวเตอร์

### 📊 แกลเลอรีที่สมบูรณ์
- **Filter และ Sort** - กรองตามจุด/ขั้นตอน และเรียงลำดับ
- **Modal ดูรูป** - คลิกดูรูปขนาดใหญ่
- **Lazy Loading** - โหลดรูปตามที่ต้องการ

### 📈 Dashboard สถิติ
- **สถิติแบบ Real-time** - จำนวนโปรเจ็กต์ รูปภาพ และโปรเจ็กต์ใหม่
- **ค้นหาและเรียงลำดับ** - หาโปรเจ็กต์ที่ต้องการได้ง่าย

## 🚀 การติดตั้ง

1. **ติดตั้ง Dependencies**
```bash
pip install -r requirements.txt
```

2. **รันแอปพลิเคชัน**
```bash
python app.py
```

3. **เปิดเบราว์เซอร์**
```
http://localhost:5000
```

## 📋 วิธีการใช้งาน

### 1. สร้างโปรเจ็กต์
- ใส่ชื่อโปรเจ็กต์ เช่น "อาคาร 4 โครงสร้างชั้น 3"
- คลิก "สร้างโปรเจ็กต์"

### 2. อัปโหลดรูปภาพ
- เลือกโปรเจ็กต์ (หรือสร้างใหม่)
- ระบุจุด (Point) เช่น "1", "คาน-01"
- เลือกขั้นตอน (Step) จากรายการ
- **ลากวางไฟล์รูปภาพ** หรือคลิกเลือกไฟล์
- คลิก "อัปโหลดรูป"

### 3. ดูแกลเลอรี
- ไปที่หน้า "โปรเจ็กต์ทั้งหมด"
- คลิก "ดูรูป" ที่โปรเจ็กต์ที่ต้องการ
- ใช้ Filter และ Sort เพื่อจัดการรูปภาพ

### 4. สร้างรายงาน
- เลือกโปรเจ็กต์ที่ต้องการ
- คลิก "ดาวน์โหลด .docx"
- ไฟล์รายงานจะถูกดาวน์โหลด

## 🎯 ขั้นตอนการทำงาน (Steps)

1. **ก่อนการดำเนินงาน** - รูปก่อนเริ่มงาน
2. **สกัดคอนกรีตที่เสียหาย ตรวจวัดขนาดเหล็กเสริม** - ขั้นตอนการซ่อมแซม
3. **ขัดสนิมเหล็ก ทาน้ำยากันสนิมและน้ำยาประสานคอนกรีต** - การเตรียมพื้นผิว
4. **เทหุ้มด้วย NONSHRINK GROUTING MATERIAL** - การเทวัสดุ
5. **ทาวัสดุป้องกันผิว** - การป้องกัน
6. **ดำเนินงานแล้วเสร็จ** - รูปงานเสร็จ

## 📁 โครงสร้างไฟล์

```
autoreport/
├── app.py              # Flask application
├── data.sqlite         # SQLite database
├── requirements.txt     # Python dependencies
├── templates/          # HTML templates
│   ├── layout.html     # Base template
│   ├── index.html      # Main page
│   ├── browse.html     # Gallery page
│   └── projects.html   # Projects list
├── uploads/           # Uploaded images
└── generated/         # Generated reports
```

## 🔧 เทคโนโลยีที่ใช้

- **Backend**: Flask, SQLite
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **UI Framework**: Tailwind CSS
- **Icons**: Feather Icons
- **File Processing**: python-docx, Pillow

## 🎨 ฟีเจอร์ UI/UX

### Drag & Drop
- พื้นที่ลากวางที่ชัดเจน
- Visual feedback เมื่อลากไฟล์
- Preview ไฟล์ที่เลือก
- การแสดงขนาดไฟล์

### Animation
- Fade-in effects
- Slide-in animations
- Hover effects
- Loading states

### Responsive Design
- Mobile-first approach
- Grid layouts
- Flexible components
- Touch-friendly

## 📊 API Endpoints

- `GET /` - หน้าหลัก
- `POST /create_project` - สร้างโปรเจ็กต์
- `POST /upload` - อัปโหลดแบบปกติ
- `POST /upload_ajax` - อัปโหลดแบบ AJAX
- `GET /report/<project>` - สร้างรายงาน
- `GET /browse/<project>` - ดูแกลเลอรี
- `GET /projects` - รายการโปรเจ็กต์
- `GET /api/stats` - สถิติ

## 🔒 ความปลอดภัย

- **File Validation** - ตรวจสอบประเภทไฟล์
- **Secure Filenames** - ป้องกัน path traversal
- **Path Sanitization** - ให้บริการไฟล์อัปโหลดอย่างปลอดภัย
- **File Size Limits** - จำกัดขนาดไฟล์
- **SQL Injection Protection** - ใช้ parameterized queries

## 🚀 การพัฒนาต่อ

### ฟีเจอร์ที่อาจเพิ่ม
- [ ] การจัดการผู้ใช้ (User Management)
- [ ] การแชร์โปรเจ็กต์
- [ ] การ Export เป็น PDF
- [ ] การ Backup/Restore
- [ ] การแจ้งเตือน (Notifications)
- [ ] การทำงานแบบ Offline

### การปรับปรุงประสิทธิภาพ
- [ ] Image compression
- [ ] Caching
- [ ] Database optimization
- [ ] CDN integration

---

**สร้างโดย**: Flask + python-docx • **ใช้งานในเครื่องได้** • **ไม่ต้องติดตั้งเซิร์ฟเวอร์**