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

---

## 📋 **Dataset: Weather & Yield Prediction Data (6 ปี)**

```
จำนวนแถว: 36 (ชั่วโมง × 6 ปี = 6 × 6 = 36 เดือน)
จำนวนคอลัมน์: 11

Year | Month | Avg_Temp_C | Max_Temp_C | Min_Temp_C | Rainfall_mm | Humidity_% | Sunshine_Hours | Rainy_Days | Evaporation_mm | Actual_Yield_kg_rai
-----|-------|-----------|-----------|-----------|-------------|-----------|----------------|-----------|----------------|-------------------
2018 | May   | 28.5      | 32.1      | 24.8      | 145         | 72        | 185            | 8         | 110            | 620
2018 | June  | 27.9      | 31.2      | 24.5      | 185         | 78        | 168            | 15        | 95             | 605
2018 | July  | 27.2      | 30.8      | 23.9      | 250         | 82        | 148            | 18        | 88             | 575
2018 | August| 27.5      | 31.0      | 24.1      | 270         | 80        | 139            | 17        | 85             | 580
2018 | Sept  | 28.1      | 32.5      | 24.6      | 320         | 75        | 125            | 19        | 92             | 585
2018 | October| 28.8     | 34.0      | 25.5      | 102         | 65        | 220            | 4         | 140            | 660
...
2023 | October| 29.0     | 33.8      | 26.2      | 92          | 63        | 225            | 3         | 145            | 720
```

**Key Variables:**
- Year: ปี (2018-2023)
- Month: เดือน (May-October)
- Weather: Rainfall_mm, Sunshine_Hours, Avg_Temp_C, Humidity_%
- Actual_Yield: ผลผลิดจริง (ตัวแปรที่ต้องทำนาย/วิเคราะห์)
```

---

## 🎤 **PROMPT LENGKAP สำหรับ Workshop D8**

```
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
[Paste weather_yield_prediction_dataset.csv]
หรือมี 36 rows × 11 columns (สมบูรณ์)

**Analysis Focus:**
- Focus: Rainfall + Sunshine แต่ไม่ใช่ Temperature
- Pattern: Seasonal Pattern (เดือน) สำคัญกว่า Year-to-Year
- Forecast: Simple Trend-Based (อาจใช้ Moving Average)
```

---

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

---

## 📋 **Dataset: Rice Disease Classification Data (48 ตัวอย่าง)**

```
จำนวนแถว: 48 (ใบไม้/รูป)
จำนวนคอลัมน์: 13

Image_ID | Province | Leaf_Color | Leaf_Shape | Spot_Pattern | Spot_Color | Spot_Size_mm | Leaf_Curl | Texture | Moisture_Level | Disease_Name | Severity
---------|----------|-----------|-----------|------------|-----------|------------|----------|---------|---------------|------------|----------
1        | Khon_Kaen| Green     | Normal    | No        | None      | 0          | No       | Smooth  | Normal        | Healthy    | -
2        | Khon_Kaen| Yellow_Grn| Curled    | Circular  | Brown     | 6          | No       | Rough   | High          | Leaf_Spot  | Moderate
3        | Nakhon_R | Brown     | Heavily   | Linear    | Gray      | 10         | Yes      | Very_R  | Very_Low      | Blast      | Severe
...
48       | Udon_Thani| Green    | Normal    | No        | None      | 0          | No       | Smooth  | Normal        | Healthy    | -

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

```
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

---

## 📌 **Expected Output จาก Workshop D9**

```
Dashboard:
✓ Summary Cards (Healthy %, Disease %, Risk Level)
✓ Disease Distribution (Pie: 60% Healthy, 25% Leaf_Spot, 15% Blast)
✓ Severity by Disease (Stacked Bar)
✓ Leaf Characteristics by Disease (Feature Comparison)
✓ Geographic Distribution (Province - Risk Map)
✓ Classification Rules (Decision Tree)
✓ Risk Alert Panel (Red/Yellow/Green)
✓ Action Recommendation Panel

Key Findings:
✓ 60% Healthy (ปกติดี)
✓ 25% Leaf_Spot (ปานกลาง)
✓ 15% Blast (ต้องระวัง)

Disease Characteristics:
Leaf_Spot:
✓ Spot_Pattern: Circular (90%)
✓ Spot_Color: Brown (80%)
✓ Spot_Size: 5-8 mm (ส่วนใหญ่)
✓ Severity: Mostly Mild-Moderate

Blast:
✓ Spot_Pattern: Linear (95%)
✓ Leaf_Curl: Yes (95%)
✓ Texture: Very Rough (90%)
✓ Severity: Moderate-Severe (ต้องรีบ!)

Prevention Actions:
✓ Leaf_Spot → Fungicide Spray (ปลอดภัย)
✓ Blast → Immediate Action Required! (รีบด้วย)
✓ Healthy → Maintain & Monitor
✓ High Risk Province: [Province] → Alert!
```

---

---

## 🎯 **SUMMARY: Workshop D8 & D9**

| Workshop | Data Source | Topic | Key Output |
|----------|------------|-------|-----------|
| **D8** | weather_yield_prediction | Weather Pattern & Forecast | Trend + Forecast + Timing |
| **D9** | rice_disease_classification | Disease Detection & Prevention | Classification + Alert + Action |

---

## 🚀 **วิธีใช้ D8 & D9**

### **สำหรับผู้สอน:**
```
1. ให้นักศึกษา อ่าน โจทย์ (D8 หรือ D9)
2. แจก Dataset (weather_yield หรือ disease_classification)
3. ให้ Copy Prompt ที่เกี่ยวข้อง
4. Paste ลง ChatGPT/Claude → เสี่ยมข้าว
5. รอ 15-20 นาที → ได้ Dashboard
6. นำไป Present & Discuss
```

### **สำหรับนักศึกษา:**
```
D8: Weather Forecasting
1. อ่านโจทย์ (อยากรู้ผลผลิด ปีหน้า?)
2. Copy Prompt D8
3. Paste lên AI + Dataset
4. ได้: Dashboard + Forecast 2024

D9: Disease Detection
1. อ่านโจทย์ (ใบไม้นี้ป่วยไหม?)
2. Copy Prompt D9
3. Paste lên AI + Dataset
4. ได้: Dashboard + Classification
```

---

## ✅ **ตอนนี้มี Dashboard Workshop ทั้งหมด 9 ตัว**

```
✅ D1: Simple Dashboard
✅ D2: Interactive Power BI
✅ D3: Storytelling Dashboard
✅ D4: Vegetable Farm Profitability
✅ D5: Aquaculture Performance
✅ D6: Student Performance
✅ D7: E-Commerce Sales
✅ D8: Weather & Yield Forecasting ← NEW (ใช้ weather_yield)
✅ D9: Disease Detection ← NEW (ใช้ disease_classification)

= 9 Workshops × Complete Prompts + Datasets
```

---

**2 Workshop ใหม่ (D8 & D9) จาก Dataset เดิม - พร้อมใช้! ✅**
