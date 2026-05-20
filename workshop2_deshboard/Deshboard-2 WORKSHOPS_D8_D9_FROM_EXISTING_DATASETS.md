# 📊 2 DASHBOARD WORKSHOPS (D8 & D9)
## จาก Dataset ที่มี: weather_yield_prediction & rice_disease_classification

---

---

# **WORKSHOP D8: WEATHER PATTERN & YIELD FORECASTING DASHBOARD**
## "ทำนายผลผลิดจากสภาพอากาศ (6 ปีข้อมูล)"

---

## 🎯 **โจทย์ (Problem Statement)**

```
สถานการณ์:
คุณเป็นเจ้าหน้าที่วิทยาศาสตร์ปลูกข้าว กรมการเกษตร
มี Dataset 6 ปี (2018-2023) 
รวบรวมข้อมูล: สภาพอากาศ (ฝน, แดด, อุณหภูมิ) ของแต่ละเดือน
และ ผลผลิดข้าวจริง (เก็บเกี่ยวสิ้นฤดู)

ปัญหา:
✗ ไม่รู้ เดือนไหนต้องปลูก ได้ผลผลิดดีสุด
✗ ไม่รู้ สภาพอากาศ (ฝน, แดด) ส่งผลต่อผลผลิด
✗ ไม่รู้ ปีไหนจะมีผลผลิดสูง-ต่ำ ได้ลึกลับ
✗ ต้อง "ทำนาย" ผลผลิด ปีหน้า เพื่อวางแผน

ต้องการ:
✓ Dashboard แสดง Trend 6 ปี
✓ ค้นหา Pattern: "เดือนไหน ผลสูง"
✓ วิเคราะห์ Correlation: สภาพอากาศ ↔ ผลผลิด
✓ ให้ Forecast: ปีหน้า อาจได้ผลเท่าไหร่
✓ ให้ Recommendation: ปลูกตรงเวลา ได้ผล
```


**Key Variables:**
- Year: ปี (2018-2023)
- Month: เดือน (May-October)
- Weather: Rainfall_mm, Sunshine_Hours, Avg_Temp_C, Humidity_%
- Actual_Yield: ผลผลิดจริง (ตัวแปรที่ต้องทำนาย/วิเคราะห์)
```

---

## 🎤 **PROMPT LENGKAP สำหรับ Workshop D8**

คุณเป็นนักวิเคราะห์ข้อมูล Agricultural Meteorology

ฉันมี Dataset ชื่อ "weather_yield_prediction_dataset" ที่มี:
• 36 เดือน (6 ปี: 2018-2023)
• 6 เดือนต่อปี (May-October = ฤดูปลูกข้าว)
• ข้อมูลสภาพอากาศ: Rainfall, Sunshine, Temperature, Humidity, Evaporation
• ข้อมูลผลผลิด: Actual Yield (kg/ไร่) ที่เก็บเกี่ยวปลายฤดู

ขอให้คุณทำ 4 สิ่ง:

1️⃣ วิเคราะห์ WEATHER PATTERNS & YIELD RELATIONSHIP
   • Trend ผลผลิด 6 ปี (มีความเสถียรหรือไม่)
   • เดือนไหนให้ผลผลิดสูงสุด? (ในทุกปี)
   • เดือนไหนให้ผลต่ำสุด?
   • Rainfall ส่งผลต่อ Yield ไหม? (Correlation)
   • Sunshine Hours ส่งผลต่อ Yield ไหม?
   • Temperature Optimal ช่วง?
   • Pattern: ฝนมากแล้ว Yield ต่ำ (จริงไหม?)
   • ปี 2018 vs 2023 ผลต่างเท่าไหร่? สาเหตุ?
   • ทำนาย: ปี 2024 อาจได้ผล ≈ ?

2️⃣ ออกแบบ DASHBOARD
   • Summary: Avg Yield (6 ปี), Best Year, Worst Year
   • Line Chart: Monthly Yield Trend (6 ปี รวม)
   • Heatmap: Year × Month (แสดง Yield แต่ละปี)
   • Bar Chart: Rainfall by Month (Average 6 ปี)
   • Bar Chart: Sunshine Hours by Month (Average)
   • Scatter: Rainfall vs Yield (เห็น Correlation)
   • Scatter: Sunshine vs Yield
   • Box Plot: Yield Distribution by Month (แสดง Variability)
   • Forecast Chart: 2024 Prediction (ตามสมการ/Pattern)
   • Top 3 Best Months (ผลสูงสุด)

3️⃣ สรุป INSIGHTS & FORECAST
   • Best Performing Month:
     ✓ October ให้ผลสูงสุด (660+ kg/ไร่)
     ✓ เพราะ Rainfall ต่ำ (92mm) + Sunshine สูง (220h)
   • Risky Month:
     ✓ July-August ต่ำสุด (575-590 kg/ไร่)
     ✓ เพราะ Rainfall สูง (250-270mm) + Sunshine ต่ำ (145h)
   • Weather-Yield Relationship:
     ✓ Rainfall HIGH → Yield LOW (Inverse)
     ✓ Sunshine HIGH → Yield HIGH (Positive)
     ✓ Temperature Optimal: 28-29°C
   • Year Comparison:
     ✓ Best Year: ? (Avg Yield)
     ✓ Worst Year: ? (Avg Yield)
     ✓ Difference: ? kg/ไร่ (ต่างกันเท่าไหร่)
   • 2024 Forecast:
     ✓ ถ้า May 145mm/185h → Predict ≈ 620 kg/ไร่
     ✓ ถ้า Oct 92mm/225h → Predict ≈ 720 kg/ไร่
   • Recommendations:
     ✓ ควรปลูก May ตรงเวลา (เพื่อเก็บ Oct)
     ✓ ติดตาม Forecast: ถ้า Oct ฝนเยอะ → ปรับแผน
     ✓ เตรียม Irrigation ถ้า Jul-Aug ฝนน้อย

4️⃣ ตอบแบบ "Forecaster" - ให้ Prediction ชัดเจน
   • ชี้ Pattern ที่เจอ
   • ให้ตัวเลข Forecast
   • ให้ Timeline (ต้องทำเมื่อไหร่)
   • ให้ Risk Assessment

**Dataset Information:**
[Paste rice_disease_classification_dataset.csv]
หรือมี 48 rows × 13 columns (สมบูรณ์)

**Classification Focus:**
- 3 Classes: Healthy, Leaf_Spot, Blast
- Feature Importance: Spot_Pattern > Leaf_Curl > Spot_Color
- Severity: Important for Treatment Decision
```


## 📌 **Expected Output จาก Workshop D8**

```
Dashboard:
✓ Summary Cards (Avg Yield, Best/Worst Year)
✓ Line Chart: Monthly Yield Trend (6 ปี)
✓ Heatmap: Year × Month Yield Matrix
✓ Rainfall by Month (Bar)
✓ Sunshine Hours by Month (Bar)
✓ Rainfall vs Yield (Scatter - เห็นความสัมพันธ์ลบ)
✓ Sunshine vs Yield (Scatter - เห็นความสัมพันธ์บวก)
✓ Yield Distribution by Month (Box Plot)
✓ 2024 Forecast (Line Projection)

Key Findings:
✓ October = Best Month (660-720 kg/ไร่)
✓ July-August = Worst (570-590 kg/ไร่)
✓ Rainfall ↑ → Yield ↓ (Inverse Relationship)
✓ Sunshine ↑ → Yield ↑ (Positive)
✓ Best Year: 2023 (Avg 625 kg)
✓ Worst Year: 2020 (Avg 590 kg)
✓ Variation: 35 kg/ไร่ ระหว่างปี (5.9%)

Forecast 2024:
✓ ถ้า Follow 2023 Pattern → 620 kg/ไร่
✓ ถ้า Rainfall <150mm ต่ำ → 650+ kg/ไร่
✓ ถ้า Sunshine >200 hours → 680+ kg/ไร่
```

---

---

# **WORKSHOP D9: RICE DISEASE DETECTION & PREVENTION DASHBOARD**
## "จำแนกโรค ใบไม้ข้าว และการป้องกัน"

---

## 🎯 **โจทย์ (Problem Statement)**

```
สถานการณ์:
คุณเป็นเจ้าหน้าที่พยาธิวิทยาพืช (Plant Pathologist)
มี Dataset 48 ตัวอย่างใบไม้ข้าว
จำแนกโรค 3 ชนิด: Healthy, Leaf Spot, Blast
มีข้อมูลลักษณะใบ: สี, รูปร่าง, จุดโรค, พื้นผิว, ความชื้น

ปัญหา:
✗ เกษตรกร ไม่รู้ใบไม้ข้าว ป่วยโรคไหน
✗ ไม่รู้ ต้องไม่ใจด้วย วิธี (ยา, การปลูก)
✗ ไม่รู้ ลักษณะไหนแสดง "เสี่ยง" โรค
✗ ไม่รู้ ความรุนแรง (Mild/Moderate/Severe)
✗ ต้อง "ติดตาม" สนามไข่ เมื่อไหร่ต้องแทรกแซง

ต้องการ:
✓ Dashboard จำแนกโรค (Healthy/Spot/Blast)
✓ แสดง ความรุนแรง ของแต่ละโรค
✓ วิเคราะห์ ลักษณะ → โรค (Feature Analysis)
✓ ให้ การป้องกัน/การรักษา เฉพาะ
✓ ให้ Risk Alert ในสัปดาห์นี้
✓ ติดตาม พื้นที่เสี่ยง
```


Key Variables:
- Image_ID: เลขที่ตัวอย่าง
- Province: จังหวัด (เพื่อแสดง Geographic Pattern)
- Leaf_Color: สีใบ (Green, Yellow_Green, Brown, ฯลฯ)
- Spot_Pattern: ลักษณะจุด (No, Circular, Linear, Irregular)
- Spot_Size_mm: ขนาดจุด (0-13 mm)
- Disease_Name: โรค (3 ชนิด): Healthy, Leaf_Spot, Blast
- Severity: ความรุนแรง (Mild, Moderate, Severe)
```

---

## 🎤 **PROMPT LENGKAP สำหรับ Workshop D9**

คุณเป็นนักวิเคราะห์ข้อมูล Plant Disease Detection

ฉันมี Dataset ชื่อ "rice_disease_classification_dataset" ที่มี:
• 48 ตัวอย่างใบไม้ข้าว
• 3 โรค: Healthy (ปกติ), Leaf_Spot (โรคจุด), Blast (โรคแห้งดำ)
• ข้อมูล: Leaf Color, Shape, Spot Pattern, Size, Texture, Moisture
• ข้อมูล Severity: Mild, Moderate, Severe

ขอให้คุณทำ 4 สิ่ง:

1️⃣ วิเคราะห์ DISEASE PATTERN & CHARACTERISTICS
   • โรคแต่ละชนิด มีลักษณะ (Feature) อะไร?
   • โรคจุด (Leaf Spot):
     ✓ Spot Pattern: Circular หรือไม่?
     ✓ Spot Color: Brown?
     ✓ Spot Size: 5-8 mm?
   • โรคแห้งดำ (Blast):
     ✓ Spot Pattern: Linear?
     ✓ Leaf_Curl: Yes?
     ✓ Texture: Very Rough?
   • Healthy:
     ✓ ไม่มี Spots?
     ✓ Leaf Color: Green?
     ✓ Texture: Smooth?
   • Severity Pattern:
     ✓ Mild → ไหน?
     ✓ Moderate → ไหน?
     ✓ Severe → ไหน?
   • Geographic Pattern: โรคที่ไหนเยอะ?
   • Moisture Level ส่งผล? (ปลูกควร ตากฟ้าไหม)

2️⃣ ออกแบบ DISEASE MONITORING DASHBOARD
   • Summary: Healthy %, Leaf_Spot %, Blast %
   • Alert Gauge: Overall Risk Level (Green/Yellow/Red)
   • Disease Distribution (Pie Chart):
     ✓ Healthy (%)
     ✓ Leaf_Spot (%)
     ✓ Blast (%)
   • Severity by Disease (Stacked Bar):
     ✓ Mild/Moderate/Severe สำหรับแต่ละโรค
   • Feature Importance (Bar Chart):
     ✓ What features indicate each disease?
     ✓ Spot_Pattern most important?
     ✓ Leaf_Curl most important?
   • Geographic Heat Map (Province):
     ✓ โรคที่ไหนมีเยอะสุด
   • Decision Tree / Classification Rules:
     ✓ IF Spot_Pattern = Circular THEN Leaf_Spot
     ✓ IF Leaf_Curl = Yes THEN Blast
   • Risk Alert Panel:
     ✓ Sample ไหนอยู่ในความเสี่ยง
     ✓ Action Required

3️⃣ สรุป DISEASE INSIGHTS & PREVENTION STRATEGY
   • Disease Prevalence:
     ✓ Healthy: ? samples (ร้อยละ)
     ✓ Leaf_Spot: ? samples
     ✓ Blast: ? samples
   • Key Characteristics:
     ✓ Leaf_Spot = Circular Spots + Brown Color
     ✓ Blast = Linear Spots + Leaf Curl + Very Rough
     ✓ Healthy = No Spots + Green + Smooth
   • Severity Assessment:
     ✓ Mild cases: ? (แค่บ้าง)
     ✓ Moderate: ? (ระบาด)
     ✓ Severe: ? (รุนแรง)
   • Geographic Risk:
     ✓ Province ไหน High Risk?
   • Prevention & Control:
     ✓ Leaf_Spot:
        - Spray Fungicide (ดูแลตากฟ้า)
        - Remove Infected Leaves
        - Improve Air Circulation
     ✓ Blast:
        - Early Intervention! (ต้องรีบ)
        - Use Blast-Resistant Varieties
        - Control Moisture
        - Spray Systemic Fungicide
     ✓ General:
        - Sanitation (ทำความสะอาด)
        - Avoid Overcrowding
        - Proper Irrigation

4️⃣ ตอบแบบ "Action-Oriented Disease Manager"
   • ระบุโรค ชัดเจน
   • ให้ Action เฉพาะแต่ละโรค
   • ให้ Timeline (ต้องทำตอนไหน)
   • ให้ Success Rate (จะหายไหม)

**Dataset Information:**
[Paste rice_disease_classification_dataset.csv]
หรือมี 48 rows × 13 columns (สมบูรณ์)

**Classification Focus:**
- 3 Classes: Healthy, Leaf_Spot, Blast
- Feature Importance: Spot_Pattern > Leaf_Curl > Spot_Color
- Severity: Important for Treatment Decision
```

