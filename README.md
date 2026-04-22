# FitTrack ✦ สมุดสุขภาพส่วนตัว

แอปติดตามสุขภาพส่วนตัว — ลดน้ำหนัก 10 kg ใน 6 เดือน พร้อม IF 16:8

---

## 🚀 วิธีติดตั้ง (2 ขั้นตอน)

### ขั้นตอนที่ 1 — Deploy บน GitHub Pages

1. สร้าง Repository ใหม่ที่ [github.com/new](https://github.com/new)
   - ชื่อ: `fittrack` (หรืออะไรก็ได้)
   - ตั้งเป็น **Public**
2. อัปโหลดไฟล์ `index.html` เข้าไปใน repo
3. ไปที่ **Settings → Pages**
4. ตั้ง Source: **Deploy from a branch** → Branch: **main** → folder: **/ (root)**
5. รอ 2-3 นาที แล้วเข้าได้ที่ `https://[username].github.io/fittrack`

---

### ขั้นตอนที่ 2 — เชื่อมต่อ Google Sheets

1. สร้าง **Google Sheet** ใหม่ที่ [sheets.google.com](https://sheets.google.com)
2. คลิก **Extensions → Apps Script**
3. ลบโค้ดเดิมออก แล้ววาง **โค้ดทั้งหมดจากไฟล์ `apps-script.gs`** ลงไป
4. กด **Save** (Ctrl+S)
5. กด **Deploy → New deployment**
   - Type: **Web app**
   - Execute as: **Me**
   - Who has access: **Anyone**
6. กด **Deploy** → **Authorize** → Copy URL

7. เปิดแอปที่ GitHub Pages → กดปุ่ม **"ตั้งค่า Sheets"** (มุมขวาบน)
8. วาง URL ที่ได้ → กด **บันทึก & ซิงค์**

---

## ✨ ฟีเจอร์

| ฟีเจอร์ | รายละเอียด |
|---|---|
| 🎯 Goal Progress | ติดตามการลดน้ำหนัก 57→47 kg ใน 6 เดือน |
| ⏰ IF Window | แสดงช่วงกินข้าว 11:00–19:00 พร้อมนับถอยหลัง |
| 💪 Workout | Checklist ออกกำลังกายเปลี่ยนตามวัน พร้อม % progress |
| 🍽️ Calorie Tracker | บันทึก 4 มื้อ เป้า 1,500 kcal เขียว/แดง |
| 💧 Water | ติดตามน้ำ 8 แก้ว/วัน |
| ⚖️ Weight Log | บันทึกน้ำหนักรายวัน |
| 🥩 Protein | ติดตามโปรตีนเป้า 110g/วัน |
| 📅 Weekly | ปฏิทินสรุปรายสัปดาห์ |
| ☁️ Google Sheets Sync | ซิงค์ข้อมูลข้ามอุปกรณ์ผ่าน Google Sheets |

---

## 📊 โครงสร้าง Google Sheet

ข้อมูลถูกเก็บใน Sheet ชื่อ `FitTrack_Logs` พร้อมคอลัมน์:

```
date | breakfast_kcal | lunch_kcal | snack_kcal | dinner_kcal |
water_glasses | weight_kg | workout_pct | tasks_json | protein_g | notes | updated_at
```
