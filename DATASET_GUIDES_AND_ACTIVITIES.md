# 📊 Dataset สำหรับการบรรยาย 3 ชั่วโมง
## เทคโนโลยี AI และ Big Data เพื่อการสืบค้น วิเคราะห์ และนำเสนอข้อมูล

---

## 📁 Dataset ที่มี (4 ชุด)

### **Dataset 1: ข้อมูลผลผลิตข้าว (30 แปลง)**
**ชื่อไฟล์:** `rice_yield_dataset.csv`

**ประเด็นหลัก:**
- ข้อมูลจริง 30 แปลงจาก 9 จังหวัด (ตะวันออกเฉียงเหนือ)
- ตัวแปร: ปริมาณน้ำฝน, อุณหภูมิ, pH ดิน, ปุ๋ยธาตุ, การรดน้ำ, ผลผลิด
- ใช้สำหรับ: การวิเคราะห์ความสัมพันธ์, การคาดการณ์ผลผลิต, การจัดเรียงลำดับความสำคัญ

**กิจกรรม Hands-on (30 นาที):**

#### **Activity 1A: การสำรวจข้อมูล (Google Sheets/Excel)**
1. เปิด `rice_yield_dataset.csv` ใน Google Sheets
2. ให้ผู้เรียนตอบคำถาม:
   - จังหวัดไหนให้ผลผลิตสูงสุด? (คำตอบ: Udon_Thani, Nakhon_Ratchasima)
   - ความสัมพันธ์ระหว่าง Rainfall กับ Yield เป็นอย่างไร? 
   - ปุ๋ยชนิด NPK vs Organic ให้ผลต่างหรือไม่?

**วิธีสอน:**
- ใช้ Filter → ให้ผู้เรียนจัดเรียงแปลงตามผลผลิด (สูงสุด → ต่ำสุด)
- สังเกตรูปแบบ: ผลผลิดสูง มักมี Rainfall สูงและการรดน้ำมากกว่า
- สรุป: "ข้อมูลที่มี Rainfall 2,200+ mm และ Irrigation 130+ วัน = ผลผลิด 650+ kg/rai"

#### **Activity 1B: สร้างกราฟ (Google Sheets/Excel)**
**Pivot Table + Chart:**
```
ขั้นตอน:
1. Insert → Pivot Table
2. Row: Province, Value: Yield (Average)
3. ดูว่าจังหวัดไหนให้ผลผลิดเฉลี่ยสูงสุด
4. Insert → Chart → Bar Chart
5. เห็นความต่างระหว่างจังหวัด
```

**ผลลัพธ์ที่คาดหวัง:**
- Udon_Thani: 686.7 kg/rai (สูงสุด)
- Yasothon: 565 kg/rai (ต่ำสุด)

---

### **Dataset 2: ข้อมูลการจำแนกโรคพืช (48 ตัวอย่าง)**
**ชื่อไฟล์:** `rice_disease_classification_dataset.csv`

**ประเด็นหลัก:**
- ข้อมูล 48 ใบไม้ (Healthy, Leaf_Spot, Blast)
- ตัวแปร: สี, รูปร่าง, ลักษณะจุด, ความมัน, ความหยาบ
- ใช้สำหรับ: วิจารณ์ Classification Model, เห็นความสำคัญของลักษณะเฉพาะ

**กิจกรรม Hands-on (25 นาที):**

#### **Activity 2A: ศึกษาลักษณะโรค (Visual Analysis)**
ให้ผู้เรียนอ่านข้อมูลและตอบคำถาม:
```
1. "ทำไม Leaf_Spot ใบจึงเหลือง?" 
   → เพราะสารประกอบพิษ แบคทีเรีย ทำให้เนื้อเซลล์ตาย

2. "ลักษณะไหนที่บ่งชี้โรค Blast?"
   → ใบห่อตัว (Curled Leaf), เส้นเกรย์/ดำ (Linear Pattern), 
      ความมัน Low (มัวหมอก)

3. "สามารถจำแนกโรคได้อย่างไรจากข้อมูลเพียง 5 ลักษณะนี้?"
```

**วิธีสอน:**
- สร้าง 3 กลุ่ม → ให้แต่ละกลุ่มศึกษาโรค 1 ชนิด
- เขียนลักษณะสำคัญบน Whiteboard
- นำเสนอ 2 นาที/กลุ่ม

#### **Activity 2B: สร้าง "Decision Tree" โดยไม่ใช้โปรแกรม**
**Manual Classification Rule:**
```
IF Leaf_Color = Green AND Spot_Pattern = No
   → Healthy ✓

ELSE IF Leaf_Curl = Yes AND Spot_Pattern = Linear
   → Blast ✓

ELSE IF Leaf_Color = Yellow_Green/Brown AND Spot_Pattern = Circular
   → Leaf_Spot ✓
```

**ให้ผู้เรียนทดลอง:**
- ใช้ Logic นี้เพื่อจำแนก 5 แปลงแรก
- นับว่า "จำแนกถูก" กี่ % 
- สรุป: "นี่คือพื้นฐานของ AI! เพียงแต่ AI ทำมันแบบ Automatic"

---

### **Dataset 3: ข้อมูล Precision Agriculture (30 โซน)**
**ชื่อไฟล์:** `precision_agriculture_fertilizer_dataset.csv`

**ประเด็นหลัก:**
- ข้อมูล 30 โซนไร่ ใน 5 บริเวณ (A-E)
- ตัวแปร: ประเภทดิน, ธาตุอาหารในดิน, ปุ๋ยทั่ว vs ปุ๋ยแม่นยำ, ผลผลิด, ต้นทุน
- **สรุปอย่าง Simple:** Fertilizer ให้ถูกจุด = ลดต้นทุน + เพิ่มผลผลิด + ลดมลพิษ
- ใช้สำหรับ: ตัวอย่าง ROI (Return on Investment), ความยั่งยืน

**กิจกรรม Hands-on (20 นาที):**

#### **Activity 3A: เปรียบเทียบการปันปุ๋ย (Recommended vs Applied)**
**โจทย์:** "พูดได้ไหมว่าไร่ไหนใช้ปุ๋ยเกิน?"
```
ขั้นตอน:
1. เปิด Dataset
2. เพิ่ม Column "N_Excess" = Applied_N - Recommended_N
3. Filter: เลือก N_Excess > 0 (ใช้เกิน)
4. นับจำนวน: กี่โซนใช้เกิน?
   → ตัวอย่าง: โซน C1, C2, C3 ใช้เกิน (ไม่ได้คำแนะนำ)
5. ถาม: "ถ้า 1 kg N ราคา 40 บาท, สิ้นเปลือง = ?"
```

**ผลคำนวณที่คาดหวัง:**
- โซน C1: ใช้เกิน N = 75-68 = 7 kg × 40 บาท = **280 บาท/ไร่ สิ้นเปลือง**
- ไร่ขนาด 2.5 ไร่ = 700 บาทสิ้นเปลือง!

#### **Activity 3B: สร้างกราฟเปรียบเทียบ "ต้นทุน vs ผลผลิด"**
**ใช้ Excel/Google Sheets:**
```
1. เลือก Column: Cost, Yield_Increase_percent
2. Insert → Scatter Chart (Bubble Chart)
3. X-axis: Cost (ต้นทุน), Y-axis: Yield_Increase (เพิ่มผลผลิด %)
4. สังเกต: โซนไหนให้ผลตอบแทนดี?
```

**ผลลัพธ์:**
- โซน A3, B3, C3: Cost ต่ำ แต่ Yield เกือบไม่เพิ่ม (Precision เทพ!)
- โซน A1, A4, B1: Cost สูงขึ้น แต่ Yield เพิ่ม 20-27% (ROI ดี!)

---

### **Dataset 4: ข้อมูลสภาพอากาศ vs ผลผลิด (36 เดือน)**
**ชื่อไฟล์:** `weather_yield_prediction_dataset.csv`

**ประเด็นหลัก:**
- ข้อมูล 6 ปี (2018-2023) × 6 เดือน = 36 ระเบียน
- ตัวแปร: อุณหภูมิ, ฝน, ความชื้น, แดด, ผลผลิดที่แท้จริง
- ใช้สำหรับ: ความสัมพันธ์ระหว่างสภาพอากาศกับผลผลิด, การคาดการณ์
- **Key Insight:** "ปริมาณฝน 250-320 มม. (ก.ย.) ให้ผลผลิดอยู่ 580-585 kg/rai"

**กิจกรรม Hands-on (15 นาที):**

#### **Activity 4A: เก็บข้อมูลเหตุปัจจัยของผลผลิดดี**
**โจทย์:** "เดือนไหนให้ผลผลิดสูงสุด? อากาศเป็นอย่างไร?"
```
ขั้นตอน:
1. เปิด Dataset
2. Filter/Sort: Actual_Yield จากมากไปน้อย
3. ดูเดือนที่ Top 5 (ผลผลิดสูง):
   - ต.ค. 2019: 660 kg/rai
   - ต.ค. 2023: 658 kg/rai
   - ต.ค. 2022: 655 kg/rai
4. สังเกต: "ลักษณ์เหมือนกัน?"
   - ฝน: ~90-95 มม (ลดลง - เตรียมเก็บเกี่ยว)
   - ความชื้น: ~68-70% (พอเพียง)
   - แดด: 215-220 ชั่วโมง (เยอะ - ช่วยสุกพร้อม)
5. สรุป: "ต.ค. ดีสำหรับเก็บเกี่ยว!"
```

#### **Activity 4B: สร้าง Simple Prediction Model (ไม่ต้องใช้โปรแกรม)**
**ด้วยนิยม "ถ้า...แล้ว...":**
```
Rule Base:
- ถ้า Total_Rainfall (May-Sep) > 1,200 มม. และ Sunshine > 900 ชั่วโมง
  → Predicted Yield ≈ 600+ kg/rai ✓ (ปัญหา)

- ถ้า Total_Rainfall (May-Sep) < 1,200 มม.
  → Predicted Yield ≈ 580-590 kg/rai (เสี่ยง)

- ถ้า Total_Rainfall (May-Sep) 1,150-1,250 มม. + Sunshine 830+ ชั่วโมง
  → Predicted Yield ≈ 620-640 kg/rai ✓ (ดีที่สุด)
```

**ให้ผู้เรียนทดลอง:** 
- ดูข้อมูล 2024 (5 เดือนแรก) → คาดการณ์ผลผลิด
- ใช้ Rule นี้ → ทำนาย
- "นี่คือหลักการเบื้องต้นของ Machine Learning!"

---

## 🎯 การเลือกใช้ Dataset สำหรับแต่ละส่วนของการบรรยาย

| เวลา | เนื้อหา | Dataset | Activity | ระดับความลำบาก |
|------|--------|---------|----------|-----------------|
| 45 นาที | Part 1: บริบท | - | - | - |
| 45 นาที | Part 2.1: เทคโนโลยี | 1, 2 | ศึกษากรณี | ต่ำ |
| 45 นาที | Part 2.2: Case Studies | 1, 2, 3 | วิเคราะห์ | ปานกลาง |
| 30 นาที | Part 3.1: Live Demo | 1, 3 | Hands-on | ปานกลาง |
| 15 นาที | Part 3.2: นำเสนอ | - | สร้างกราฟ | ต่ำ |
| 15 นาที | Summary | 4 | Prediction | สูง |

---

## 🛠️ เครื่องมือที่แนะนำสำหรับแต่ละ Activity

### **Activity 1A & 1B: Google Sheets / Excel**
✅ ใช้ได้ดีที่สุด
- ผู้เรียนทำตามไปด้วยได้เลย
- Filter/Pivot ใช้งาน 5 นาที
- ผลลัพธ์ชัดเจน

**วิธี Share:**
```
1. Upload rice_yield_dataset.csv ไป Google Drive
2. สร้าง Google Sheet เปิดสู่สาธารณะ (Share Link)
3. ให้ผู้เรียนเปิด → ไม่ต้อง Login
4. Copy file → สามารถแก้ไขได้
```

### **Activity 2A & 2B: วิศวกร + Whiteboard**
✅ ไม่ต้องเครื่องมือเพิ่ม - ใช้เอกสาร
- นั่งเรียน + คิด + เขียน
- ไม่ต้องหน้าจอ - ตาสบาย
- ตัวเลข อ่านจากไฟล์

### **Activity 3A & 3B: Excel / Google Sheets**
✅ Hands-on
- ผู้เรียนเปิด + สร้าง Column เอง
- Scatter Chart ง่าย
- เห็น ROI เห็นจริง

### **Activity 4A & 4B: Excel / ตารางกระดาษ**
✅ ตารางก่อน → เข้าใจก่อน
- เขียน Rule เอง (ไม่ใช้โปรแกรม)
- ทำนายแล้ว Check กับข้อมูลจริง
- สรุป: "AI ทำแบบนี้ แต่ Automatic"

---

## 📋 Check List เตรียมก่อนบรรยาย

- [ ] Download 4 files CSV
- [ ] Test เปิด Google Sheets / Excel (Check format)
- [ ] สร้าง Google Sheet Share Link (สำหรับ 1A, 1B)
- [ ] Print Handout (Data Dictionary) ให้ผู้เรียน
- [ ] Prepare Whiteboard + Markers
- [ ] Test Live Demo (อันไหนจะทำ)
- [ ] เตรียม "Fallback Video" ถ้า Demo ล้ม
- [ ] QR Code ไป Dataset files

---

## 📊 Data Dictionary (อธิบายตัวแปร)

### **rice_yield_dataset.csv**
| Column | ความหมาย | หน่วย | ช่วง |
|--------|---------|------|------|
| Plot_ID | เลขแปลง | - | 1-30 |
| Province | จังหวัด | - | 9 จังหวัด |
| Area_Rai | พื้นที่ | ไร่ | 1.5-3.5 |
| Rainfall_mm | ปริมาณน้ำฝน | มม. | 1750-2400 |
| Avg_Temp_C | อุณหภูมิเฉลี่ย | °C | 27.5-29.2 |
| Soil_pH | ความเป็นกรด/ด่าง | - | 6.3-7.1 |
| Nitrogen_kg | ปุ๋ยไนโตรเจน | kg/ไร่ | 48-85 |
| Phosphorus_kg | ปุ๋ยฟอสฟอรัส | kg/ไร่ | 23-42 |
| Potassium_kg | ปุ๋ยโปแตสเซียม | kg/ไร่ | 14-30 |
| Irrigation_Days | วันที่รดน้ำ | วัน | 95-155 |
| Fertilizer_Type | ชนิดปุ๋ย | - | NPK / Organic |
| Pesticide_Used | ใช้สารเคมี | - | Yes/No |
| **Yield_kg_per_rai** | **ผลผลิดข้าว** | **kg/ไร่** | **520-720** |

### **rice_disease_classification_dataset.csv**
| Column | ความหมาย | ตัวอย่าง |
|--------|---------|---------|
| Image_ID | เลขรูป | 1-48 |
| Crop_Type | พืช | Rice |
| Leaf_Color | สีใบ | Green, Yellow_Green, Brown... |
| Spot_Pattern | ลักษณะจุด | No, Circular, Linear, Irregular |
| Spot_Color | สีจุด | Brown, Dark_Brown, Black, Gray |
| Spot_Size_mm | ขนาดจุด | 0-13 มม. |
| **Disease_Name** | **โรค** | **Healthy / Leaf_Spot / Blast** |
| Severity | ความรุนแรง | Mild, Moderate, Severe |

### **precision_agriculture_fertilizer_dataset.csv**
| Column | ความหมาย | หน่วย |
|--------|---------|------|
| Plot_No | เลขโซน | 1-30 |
| Zone | บริเวณ | A-E |
| Soil_Nitrogen_ppm | ไนโตรเจนในดิน | ppm |
| Recommended_N_kg | ปุ๋ย N ที่ควรใช้ | kg/ไร่ |
| Applied_N_kg | ปุ๋ย N ที่ใช้จริง | kg/ไร่ |
| Cost_Baht | ต้นทุนปุ๋ย | บาท |
| **Current_Yield_kg_rai** | **ผลผลิดจริง** | **kg/ไร่** |
| **Yield_Increase_percent** | **เพิ่มผลผลิด %** | **%** |
| Environmental_Impact_Score | สถาบันสิ่งแวดล้อม | 0-100 |

### **weather_yield_prediction_dataset.csv**
| Column | ความหมาย | หน่วย |
|--------|---------|------|
| Year | ปี | 2018-2023 |
| Month | เดือน | May-October |
| Avg_Temperature_C | อุณหภูมิเฉลี่ย | °C |
| Total_Rainfall_mm | ปริมาณน้ำฝน | มม. |
| Avg_Humidity_percent | ความชื้นอากาศ | % |
| Sunshine_Hours | ชั่วโมงแดด | ชั่วโมง |
| **Actual_Yield_kg_rai_End_of_Season** | **ผลผลิดสุดท้าย** | **kg/ไร่** |

---


## 🎁 Resources ที่ให้ผู้เรียนดาวน์โหลดไป

ให้สร้าง QR Code / Link:
1. **CSV Files (4 ไฟล์)**
2. **Handout PDF** (Data Dictionary)
3. **Excel Template** (สำหรับ Activity 3B)
4. **Google Sheet Share Link**

