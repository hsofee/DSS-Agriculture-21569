# 📊 18 QUESTIONS: RICE YIELD DATA ANALYSIS
## 4 Levels: Descriptive → Diagnostic → Predictive → Prescriptive

---

## 🎯 **OVERVIEW**

```
18 คำถามวิเคราะห์ข้อมูลผลผลิตข้าว แบ่ง 4 ระดับความเชิงลึก:

🔹 Level 1: Descriptive (ข้อ 1-5)
   "ข้อมูลเป็นยังไง?" → สรุปภาพรวม, ค่าเฉลี่ย, Trend
   
🔹 Level 2: Diagnostic (ข้อ 6-10)
   "ทำไมถึงเป็นแบบนี้?" → สาเหตุ, ความสัมพันธ์, Pattern
   
🔹 Level 3: Predictive (ข้อ 11-14)
   "จะเป็นยังไงข้างหน้า?" → ทำนาย, Forecast, What-If
   
🔹 Level 4: Prescriptive (ข้อ 15-18)
   "ควรทำอย่างไร?" → แนวทาง, Strategy, Decision
```

---

---

# 🔹 **LEVEL 1: DESCRIPTIVE (ข้อ 1–5)**
## "What is the data like?" - สรุปภาพรวมข้อมูล

---

## **QUESTION 1: ผลผลิตข้าว - ภาพรวม**

### **โจทย์:**
```
คุณเป็นนักวิเคราะห์ข้อมูลด้านการเกษตร 
ช่วยวิเคราะห์ข้อมูลผลผลิตข้าว และสรุปค่าเฉลี่ย (mean) 
แนวโน้ม และภาพรวมของผลผลิตในแต่ละปี 
โดยอธิบายให้เข้าใจง่ายในเชิงวิชาการ
```

### **PROMPT สำหรับนักศึกษา:**
```
คุณเป็นนักวิเคราะห์ข้อมูล Agricultural Analyst

ฉันมี Dataset "rice_yield_dataset" ที่มี 30 แปลงข้าว

ขอให้คุณ:
1. สรุป ค่าเฉลี่ย (Mean) ของผลผลิด (Yield_kg_per_rai)
2. แนวโน้ม: ผลผลิดในแต่ละปี มีแนวโน้ยังไง?
3. ภาพรวม: 
   - ค่าสูงสุด (Max)
   - ค่าต่ำสุด (Min)
   - ช่วงการกระจายตัว (Range)
4. อธิบายความหมายของตัวเลข (เช่น 630 kg/ไร่ เปรียบเทียบกับปกติ)

ตอบแบบ "สรุปสั้น" แต่ชัดเจน
ไม่ต้องใช้สูตรยุ่งยาก

[Paste rice_yield_dataset.csv]
```

---

## **QUESTION 2: จังหวัดที่ดี-แย่สุด**

### **โจทย์:**
```
ช่วยระบุจังหวัดที่มีผลผลิตข้าวสูงที่สุดและต่ำที่สุดจากข้อมูล 
พร้อมอธิบายความแตกต่องของพื้นที่เหล่านั้น
```

### **PROMPT สำหรับนักศึกษา:**
```
คุณเป็น Data Analyst สำหรับกระทรวงเกษตร

จากข้อมูล rice_yield_dataset ขอให้คุณ:

1. ระบุจังหวัด TOP 3 ที่ให้ผลผลิดสูงสุด
   - ชื่อจังหวัด + ผลผลิดเฉลี่ย
   - จำนวนแปลง
   
2. ระบุจังหวัด BOTTOM 2 ที่ให้ผลผลิดต่ำสุด
   - ชื่อจังหวัด + ผลผลิดเฉลี่ย
   - จำนวนแปลง

3. เปรียบเทียบ:
   - ผลต่างระหว่าง TOP vs BOTTOM (kg/ไร่)
   - ร้อยละความแตกต่าง

4. อธิบาย: พื้นที่ที่ดี อาจมีความแตกต่างเชิงใด? 
   (เช่น ดิน สภาพอากาศ การจัดการ)
   [อย่ายืนยัน แต่ให้สมมติการณ์]

[Paste rice_yield_dataset.csv]
```

---

## **QUESTION 3: แนวโน้มผลผลิด (5-10 ปี)**

### **โจทย์:**
```
ช่วยวิเคราะห์แนวโน้มของผลผลิตข้าวในช่วง 5–10 ปีที่ผ่านมา 
ว่ามีแนวโน้มเพิ่มขึ้น ลดลง หรือคงที่ พร้อมอธิบายเหตุผลที่เป็นไปได้
```

### **PROMPT สำหรับนักศึกษา:**
```
คุณเป็น Agricultural Trend Analyst

จากข้อมูล weather_yield_prediction_dataset (6 ปี: 2018-2023)
ขอให้คุณ:

1. วิเคราะห์ Trend ผลผลิด 6 ปี:
   - ปี 2018 avg yield = ?
   - ปี 2023 avg yield = ?
   - เพิ่มขึ้นหรือลดลง?
   - เพิ่ม/ลด กี่เปอร์เซ็นต์?

2. Pattern:
   - Trend ชัดเจนหรือไม่?
   - มี "ลูกคลื่น" (ขึ้นลงหรือไม่)?
   
3. เหตุผลที่เป็นไปได้:
   - สภาพอากาศเปลี่ยน?
   - เทคโนโลยีการปลูก?
   - เนื้อที่ปลูก?
   [สมมติฐาน ไม่ต้องแน่นอน]

4. Visual: ให้สร้าง Line Chart แสดง Trend

[Paste weather_yield_prediction_dataset.csv]
```

---

## **QUESTION 4: ค่าสถิติพื้นฐาน**

### **โจทย์:**
```
ช่วยคำนวณและอธิบายค่าเฉลี่ย ค่าสูงสุด และค่าต่ำสุดของผลผลิตข้าว 
พร้อมตีความความหมายของตัวเลขเหล่านี้ในบริบททางการเกษตร
```

### **PROMPT สำหรับนักศึกษา:**
```
คุณเป็นผู้เชี่ยวชาญ Agricultural Statistics

จากข้อมูล rice_yield_dataset ขอให้คุณ:

1. คำนวณ Basic Statistics:
   - Mean (ค่าเฉลี่ย)
   - Median (ค่ากลาง)
   - Mode (ค่าที่ปรากฏบ่อยสุด - ถ้ามี)
   - Standard Deviation (การกระจัด)
   - Min (ต่ำสุด)
   - Max (สูงสุด)
   - Range (ช่วง Max-Min)

2. ตีความ:
   - Mean 630 kg/ไร่ นี่ "ดี" หรือ "ต่ำ"? 
     (เปรียบเทียบกับ Global Average หรือ National Target)
   
   - Range 200 kg (720-520) นี่ "สูง" หรือ "ต่ำ"?
     (คือผลต่างมาก ต้องจัดการหรือปกติ?)
   
   - Std Dev คืออะไร? (ความแปรผวน)

3. Implication:
   - ข้อมูลแสดงว่าอะไร?
   - ต้องแก้ไขจุดไหน?

[Paste rice_yield_dataset.csv]
```

---

## **QUESTION 5: Outlier Detection**

### **โจทย์:**
```
ช่วยตรวจสอบว่ามีค่าผิดปกติ (outlier) ในข้อมูลผลผลิตข้าวหรือไม่ 
และอธิบายว่าค่าที่ผิดปกติเหล่านี้อาจเกิดจากสาเหตุใด
```

### **PROMPT สำหรับนักศึกษา:**
```
คุณเป็น Data Quality Analyst

จากข้อมูล rice_yield_dataset ขอให้คุณ:

1. ระบุ Outliers:
   - ค่าไหนผิดปกติ? (สูงหรือต่ำเกิน?)
   - วิธี: ใช้ Mean ± 2×StdDev 
            หรือ IQR Method (Q1-1.5×IQR, Q3+1.5×IQR)
   
2. ลักษณะ:
   - Outlier มีกี่ค่า? (เท่าไหร่ % ของทั้งหมด?)
   - High Outlier (สูงเกิน) เท่าไหร่?
   - Low Outlier (ต่ำเกิน) เท่าไหร่?

3. เหตุผลที่เป็นไปได้:
   - Outlier สูง (720+ kg) อาจเพราะ:
     ✓ สภาพอากาศเหมาะสม
     ✓ การจัดการดีเยี่ยม
     ✓ ทดลองเทคโนโลยีใหม่
   
   - Outlier ต่ำ (<520 kg) อาจเพราะ:
     ✓ ภัยแล้ง
     ✓ เชื้อโรค
     ✓ ความผิดพลาดในการบันทึก

4. ความหมาย:
   - ควรลบ outliers หรือเก็บไว้?
   - บอกอะไรเกี่ยวกับ Data Quality?

[Paste rice_yield_dataset.csv]
```

---

---

# 🔹 **LEVEL 2: DIAGNOSTIC (ข้อ 6–10)**
## "Why is the data this way?" - ค้นหาสาเหตุ

---

## **QUESTION 6: ปัจจัยสำคัญ (Correlation)**

### **โจทย์:**
```
ช่วยวิเคราะห์ว่าปัจจัยใดมีความสัมพันธ์กับผลผลิตข้าวมากที่สุด 
พร้อมอธิบายเชิงเหตุผล
```

### **PROMPT สำหรับนักศึกษา:**
```
คุณเป็น Agricultural Data Scientist

จากข้อมูล rice_yield_dataset ขอให้คุณ:

1. หาความสัมพันธ์ (Correlation):
   ตัวแปรไหน มีสัมพันธ์กับ Yield มากที่สุด?
   
   เช่น:
   - Rainfall_mm ↔ Yield: correlation = ?
   - Irrigation_Days ↔ Yield: correlation = ?
   - Nitrogen_kg ↔ Yield: correlation = ?
   - Soil_pH ↔ Yield: correlation = ?
   - Pesticide_Used ↔ Yield: correlation = ?
   
2. ตีความ:
   - Correlation > 0.7 = STRONG
   - Correlation 0.3-0.7 = MODERATE
   - Correlation < 0.3 = WEAK
   
3. อธิบาย "ทำไม":
   - ปัจจัย [Name] มีผล เพราะ [เหตุผลทางวิทยาศาสตร์]
   
4. Ranking:
   - ปัจจัย TOP 3 ที่มีผลต่อ Yield มากสุด

[Paste rice_yield_dataset.csv]
```

---

## **QUESTION 7: สภาพอากาศ vs ผลผลิด**

### **โจทย์:**
```
ช่วยวิเคราะห์ความสัมพันธ์ระหว่างปริมาณฝนและอุณหภูมิกับผลผลิตข้าว 
และอธิบายว่าปัจจัยด้านสภาพอากาศมีผลอย่างไร
```

### **PROMPT สำหรับนักศึกษา:**
```
คุณเป็นผู้เชี่ยวชาญ Agricultural Meteorology

จากข้อมูล weather_yield_prediction_dataset ขอให้คุณ:

1. วิเคราะห์ Rainfall ↔ Yield:
   - Correlation = ?
   - ความสัมพันธ์บวก หรือ ลบ?
   - ความหมาย: ฝนมากแล้วผลผลิด [เพิ่ม/ลด]?
   
2. วิเคราะห์ Temperature ↔ Yield:
   - Correlation = ?
   - Temperature ที่เหมาะสม = ? °C
   - ถ้า Temp เกิน/ต่ำกว่า → ผลผลิดลด?
   
3. วิเคราะห์ Sunshine Hours ↔ Yield:
   - Correlation = ?
   - ชั่วโมงแดด ที่เหมาะสม = ? ชั่วโมง
   - ไม่มีแดดเพียงพอ → ผลผลิดลด?
   
4. Overall:
   - สภาพอากาศที่ "ดีสำหรับปลูกข้าว" เป็นยังไง?
   - เดือนไหนเหมาะสมที่สุด?

5. Visualization:
   - Scatter plot: Rainfall vs Yield
   - Scatter plot: Sunshine vs Yield

[Paste weather_yield_prediction_dataset.csv]
```

---

## **QUESTION 8: พื้นที่ปลูกแย่ - สาเหตุ**

### **โจทย์:**
```
ช่วยวิเคราะห์พื้นที่ที่มีผลผลิตข้าวต่ำผิดปกติ 
และอธิบายสาเหตุที่เป็นไปได้ เช่น ดิน สภาพอากาศ หรือการจัดการ
```

### **PROMPT สำหรับนักศึกษา:**
```
คุณเป็น Agricultural Diagnostician

จากข้อมูล rice_yield_dataset ขอให้คุณ:

1. ระบุแปลง/จังหวัด ที่ผลต่ำเกิน:
   - เลขแปลง: ?
   - จังหวัด: ?
   - Yield = ? kg/ไร่ (ต่ำกว่า Mean เท่าไหร่?)

2. ตรวจสอบปัจจัยแต่ละตัว:
   - Rainfall = ? mm (เพียงพอหรือไม่?)
   - Soil_pH = ? (เหมาะสม 6.5-7.5 หรือไม่?)
   - Nitrogen = ? kg (เพียงพอหรือไม่?)
   - Irrigation = ? days (เพียงพอหรือไม่?)
   - Fertilizer_Type = ? (NPK หรือ Organic?)
   - Pesticide_Used = ? (มีหรือไม่?)

3. วิเคราะห์สาเหตุ:
   - Soil: ดิน pH ต่ำ? → ปลูกข้าวไม่ดี
   - Water: ฝนน้อย + irrigation น้อย? → ขาดน้ำ
   - Nutrients: ปุ๋ย/ไนโตรเจน น้อย? → ขาดสารอาหาร
   - Disease/Pest: ไม่ใช้ยา? → มีโรค/แมลง
   - Management: อื่น ๆ?

4. Recommendation (เบื้องต้น):
   - ควรแก้ไขอะไรเป็นลำดับแรก?

[Paste rice_yield_dataset.csv]
```

---

## **QUESTION 9: เปรียบเทียบภูมิภาค**

### **โจทย์:**
```
ช่วยเปรียบเทียบผลผลิตข้าวระหว่างภูมิภาคต่าง ๆ 
และอธิบายความแตกต่างในเชิงปัจจัยด้านสิ่งแวดล้อมและเศรษฐกิจ
```

### **PROMPT สำหรับนักศึกษา:**
```
คุณเป็น Regional Agricultural Analyst

จากข้อมูล rice_yield_dataset (9 จังหวัด ตะวันออกเฉียงเหนือ) 
ขอให้คุณ:

1. จัดกลุ่มจังหวัด (ถ้าเป็นไปได้):
   - ตามภูมิศาสตร์ (เหนือ กลาง ใต้ ตะวันออก)
   - หรือ ตามผลผลิด (สูง ปานกลาง ต่ำ)

2. เปรียบเทียบ:
   - Avg Yield ของแต่ละภูมิภาค
   - Rainfall ของแต่ละภูมิภาค
   - Soil pH
   - Fertilizer ที่ใช้ (NPK vs Organic)
   - Pesticide Usage %
   - Irrigation Pattern

3. วิเคราะห์ความแตกต่าง:
   - ภูมิภาค [A] ผลดี เพราะ:
     ✓ ฝนเหมาะสม
     ✓ ดิน pH ดี
     ✓ ใช้ NPK + Pesticide
   
   - ภูมิภาค [B] ผลต่ำ เพราะ:
     ✓ ฝนหลาย/น้อยเกิน
     ✓ ดิน pH ไม่ดี
     ✓ ใช้ Organic + ไม่มี Pesticide

4. Socio-Economic Implication:
   - ภูมิภาคดีมี "ข้อมูล" อะไร?
     (เช่น: เชื่อ Technology, Budget มี, ความรู้เพียงพอ)
   - ภูมิภาคต่ำมี "ปัญหา" อะไร?

[Paste rice_yield_dataset.csv]
```

---

## **QUESTION 10: Pattern & Seasonality**

### **โจทย์:**
```
ช่วยวิเคราะห์ว่าข้อมูลผลผลิตข้าวมีรูปแบบ (pattern) หรือฤดูกาล (seasonality) หรือไม่ 
และอธิบายความหมายของ pattern นั้น
```

### **PROMPT สำหรับนักศึกษา:**
```
คุณเป็น Time Series Analyst

จากข้อมูล weather_yield_prediction_dataset ขอให้คุณ:

1. ค้นหา Seasonality (ฤดูกาล):
   - เดือนไหนให้ผลผลิดสูงเสมอ?
   - เดือนไหนให้ผลต่ำเสมอ?
   - Pattern ซ้ำหรือไม่ทุกปี?
   
2. Cyclical Pattern:
   - มี "ลูกคลื่น" (Up-Down-Up) หรือไม่?
   - ช่วงเวลา (Period) เป็นเท่าไหร่? (เช่น 6 เดือน, 1 ปี)
   
3. Trend:
   - Long-term trend: เพิ่ม/ลด/คงที่?
   - Seasonality independent จาก Trend?
   
4. ความหมาย:
   - Pattern นี้เกิดจากอะไร?
     ✓ Seasonal rainfall?
     ✓ Sunshine hours?
     ✓ Planting schedule?
     ✓ Market demand?
   
5. Implication:
   - หากรู้ Pattern นี้ → ทำอะไรได้?
     (เช่น: วางแผนรดน้ำ, เตรียมความพร้อม)

6. Visualization:
   - Line chart: Month vs Yield (ทั้ง 6 ปี)
   - Highlight: ฤดูกาล pattern

[Paste weather_yield_prediction_dataset.csv]
```

---

---

# 🔹 **LEVEL 3: PREDICTIVE (ข้อ 11–14)**
## "What will happen in the future?" - ทำนายความหมาย

---

## **QUESTION 11: What-If Scenario (Rainfall)**

### **โจทย์:**
```
ช่วยวิเคราะห์ว่า หากปริมาณฝนลดลง 10% จะส่งผลต่อผลผลิตข้าวอย่างไร 
พร้อมอธิบายเชิงเหตุผล
```

### **PROMPT สำหรับนักศึกษา:**
```
คุณเป็น Agricultural Scenario Planner

จากข้อมูล rice_yield_dataset และ weather_yield_prediction_dataset
ขอให้คุณ:

1. หา Correlation: Rainfall ↔ Yield
   - r = ? (ความสัมพันธ์สูง/ต่ำ?)
   - Regression Equation: Yield = a + b×Rainfall
   
2. Scenario: ฝนลดลง 10%
   - Current Avg Rainfall = ? mm
   - New Rainfall (10% down) = ? mm
   
3. Forecast ผลลัพธ์:
   - Current Avg Yield = ? kg/ไร่
   - Expected Yield (after -10% rain) = ? kg/ไร่
   - Loss = ? kg/ไร่ (และ %)
   
4. Explain:
   - ฝนลด → Yield ลดเพราะ:
     ✓ ข้าวต้องน้ำ
     ✓ ต้องรดน้ำตั้งแต่ปลูก
     ✓ ดิน Dry Stress
   
5. Mitigation (ทำอย่างไรแก้):
   - เพิ่ม Irrigation?
   - เปลี่ยนพันธุ์ ที่ทนแห้ง?
   - Adjust Planting Date?

6. Risk Assessment:
   - โอกาส ฝนลด 10% ในปีหน้า = ?%
   - ต้องเตรียม?

[Paste rice_yield_dataset.csv + weather_yield_prediction_dataset.csv]
```

---

## **QUESTION 12: Forecast ปีถัดไป**

### **โจทย์:**
```
ช่วยคาดการณ์แนวโน้มผลผลิตข้าวในปีถัดไป 
โดยอ้างอิงจากข้อมูลที่ผ่านมา และอธิบายเหตุผล
```

### **PROMPT สำหรับนักศึกษา:**
```
คุณเป็น Agricultural Forecaster

จากข้อมูล weather_yield_prediction_dataset (2018-2023)
ขอให้คุณ:

1. วิเคราะห์ Trend:
   - Avg Yield: 2018 = ?, 2023 = ?
   - Trend: +/- เท่าไหร่ต่อปี?
   - Growth Rate = ?% per year
   
2. Simple Forecast (ปี 2024):
   - Method 1: Linear Trend
     Yield 2024 = Yield 2023 + (growth rate × 1)
     
   - Method 2: Moving Average (3-year)
     Yield 2024 = Avg(2021, 2022, 2023)
   
   - Method 3: Pattern-Based
     ถ้า 2024 มีสภาพอากาศ "เหมือน 2023"
     → Yield 2024 ≈ Yield 2023
   
3. Predicted Yield 2024 = ? kg/ไร่
   (และระบุ Method ที่ใช้ + Confidence Level)

4. Explanation:
   - Forecast นี้อ้างอิงจากอะไร?
   - Assumption ที่ทำ?
   - Risk/Uncertainty?

5. Recommendation:
   - ปีนี้ควรปลูกหรือไม่?
   - ปลูกเท่าไร?

[Paste weather_yield_prediction_dataset.csv]
```

---

## **QUESTION 13: Best Predictor**

### **โจทย์:**
```
ช่วยวิเคราะห์ว่าปัจจัยใดเหมาะสมที่สุดสำหรับใช้ในการทำนายผลผลิตข้าว 
พร้อมอธิบายเหตุผลเชิงข้อมูล
```

### **PROMPT สำหรับนักศึกษา:**
```
คุณเป็น Predictive Analytics Specialist

จากข้อมูลทั้ง rice_yield_dataset และ weather_yield_prediction_dataset
ขอให้คุณ:

1. หา Correlation ของทุกปัจจัย:
   ตัวแปร | Correlation with Yield | Strength
   -------|------------------------|----------
   Rainfall_mm | ? | Strong/Moderate/Weak
   Sunshine_Hours | ? | ?
   Nitrogen_kg | ? | ?
   Irrigation_Days | ? | ?
   Soil_pH | ? | ?
   Fertilizer_Type | ? | ?
   Pesticide_Used | ? | ?
   [อื่น ๆ]

2. Ranking:
   - TOP 3 Best Predictors:
     1. [Name] - r = ?, Reason: ?
     2. [Name] - r = ?, Reason: ?
     3. [Name] - r = ?, Reason: ?

3. Explain "ทำไม":
   - Rainfall เป็น Best Predictor เพราะ:
     ✓ ข้าวต้องน้ำ → Direct Impact
     ✓ Rainfall + Irrigation = Total Water
     ✓ Water Stress → Yield ลดชัดเจน
   
   - เพราะไม่ใช่ [Other Factor]:
     ✓ Fertilizer เสมอ เพราะ [เหตุผล]
     ✓ Temperature คงที่ เพราะ [เหตุผล]

4. Model Suggestion:
   - ถ้าต้องสร้าง Prediction Model
   - ควรใช้ตัวแปร: ?
   - Skip ตัวแปร: ? (เพราะเบาบาง)

[Paste rice_yield_dataset.csv + weather_yield_prediction_dataset.csv]
```

---

## **QUESTION 14: Predictive Model Concept**

### **โจทย์:**
```
ช่วยสร้างแนวคิดหรือโมเดลเบื้องต้นสำหรับการพยากรณ์ผลผลิตข้าว 
และอธิบายว่าตัวแปรใดมีความสำคัญมากที่สุด
```

### **PROMPT สำหรับนักศึกษา:**
```
คุณเป็น Predictive Model Designer

จากข้อมูล รวม ขอให้คุณ:

1. เลือก Model Type:
   - Option A: Linear Regression
     Yield = a + b1×Rainfall + b2×Irrigation + b3×Nitrogen + ε
   
   - Option B: Multiple Regression
     Yield = a + b1×Rainfall + b2×Sunshine + b3×Nitrogen + b4×Pesticide + ε
   
   - Option C: Classification Tree
     IF Rainfall < 1,900 mm THEN Risk
     IF Nitrogen < 55 kg THEN Risk
     ...
   
   - ข้อเสนอ: ใช้ [Model Type] เพราะ [เหตุผล]

2. Input Variables (ที่ใช้ทำนาย):
   - Top 3-4 variables ที่ correlate สูง
   - อื่น ๆ?
   
3. Output Variable:
   - Yield_kg_per_rai

4. Model Equation (Simple Example):
   Yield ≈ 400 + 0.12×Rainfall + 1.5×Nitrogen + ...
   
5. Feature Importance (Relative Contribution):
   - Rainfall: ? % ของ Prediction
   - Nitrogen: ? %
   - Irrigation: ? %
   - อื่น ๆ: ? %

6. Accuracy & Uncertainty:
   - Model นี้ predict ได้แม่นเท่าไหร่?
   - Confidence Level = ±? kg/ไร่
   - Worst Case / Best Case?

7. Limitations:
   - Assumptions?
   - ข้อจำกัด?
   - ต้องปรับปรุง?

[Paste rice_yield_dataset.csv + weather_yield_prediction_dataset.csv]
```

---

---

# 🔹 **LEVEL 4: PRESCRIPTIVE (ข้อ 15–18)**
## "What should we do?" - ให้คำแนะนำ/นโยบาย

---

## **QUESTION 15: วิธีเพิ่มผลผลิด**

### **โจทย์:**
```
จากข้อมูลที่วิเคราะห์ ช่วยเสนอแนวทางในการเพิ่มผลผลิตข้าว 
โดยอ้างอิงจากข้อมูลและปัจจัยที่เกี่ยวข้อง
```

### **PROMPT สำหรับนักศึกษา:**
```
คุณเป็น Agricultural Strategy Consultant

จากข้อมูลวิเคราะห์ทั้งหมด ขอให้คุณ:

1. ระบุปัจจัย "ที่แต่จำหน่ายได้" (Controllable):
   ✓ Nitrogen_kg (ปัจจุบัน avg = ?, สามารถเพิ่มได้?)
   ✓ Irrigation_Days (ปัจจุบัน avg = ?, สามารถเพิ่มได้?)
   ✓ Fertilizer_Type (Organic → NPK?)
   ✓ Pesticide_Used (ทั่วไป?)
   ✓ Soil_pH (สามารถปรับได้?)
   
   ❌ ปัจจัย "ไม่ควบคุมได้" (Uncontrollable):
   - Rainfall (ธรรมชาติ)
   - Temperature (ธรรมชาติ)

2. เสนอแนวทาง (Top 5 Actions):
   
   Action 1: เพิ่มไนโตรเจน
   - Current: 63 kg/ไร่
   - Proposed: 75 kg/ไร่
   - Expected Gain: ? kg/ไร่ (? %)
   - Cost: ? บาท/ไร่
   - ROI: ? %
   
   Action 2: เพิ่มการรดน้ำ
   - Current: 120 days
   - Proposed: 135 days
   - Expected Gain: ? kg/ไร่ (? %)
   - Cost: ? บาท/ไร่
   - ROI: ? %
   
   Action 3: เปลี่ยน Fertilizer เป็น NPK
   - Current: ส่วนใหญ่ Organic
   - Proposed: 100% NPK
   - Expected Gain: ? kg/ไร่ (? %)
   - Cost: ?
   - ROI: ? %
   
   Action 4: ใช้ Pesticide ทั้งหมด
   - Current: 80% ใช้, 20% ไม่ใช้
   - Proposed: 100% ใช้
   - Expected Gain: ? kg/ไร่ (? %)
   - Cost: ?
   - ROI: ? %
   
   Action 5: [Other - เสนอเอง]
   - ?

3. Combined Strategy:
   - ถ้าใช้ทุก Action พร้อมกัน
   - Expected Total Gain: ? kg/ไร่
   - Combined Cost: ? บาท
   - Combined ROI: ? %
   - Payback Period: ? ปี?

4. Priority:
   - ควรทำ Action ไหนเป็นลำดับแรก?
   - เหตุผล? (High ROI? Easy to implement? Low risk?)

[Paste rice_yield_dataset.csv + weather_yield_prediction_dataset.csv]
```

---

## **QUESTION 16: เลือกพื้นที่ลงทุน**

### **โจทย์:**
```
ช่วยวิเคราะห์ว่าควรเลือกพื้นที่ใดในการลงทุนเพิ่มผลผลิตข้าว 
พร้อมอธิบายเหตุผลเชิงข้อมูล
```

### **PROMPT สำหรับนักศึกษา:**
```
คุณเป็น Investment Decision Maker

จากข้อมูล rice_yield_dataset (9 จังหวัด)
ขอให้คุณ:

1. Evaluate แต่ละจังหวัด:
   
   Province | Current Yield | Potential | Gap | Risk | Score
   ---------|---------------|-----------|-----|------|-------
   Udon | 686 | 710 | 24 | Low | 85
   Nakhon_R| 680 | 710 | 30 | Low | 90
   Kalasin | 667 | 700 | 33 | Medium | 80
   ... | ... | ... | ... | ... | ...

2. Selection Criteria:
   
   ✓ Criteria 1: Current Yield (ดีแล้ว vs ต่ำ)
     → Focus ที่ "ต่ำ" (มีพื้นที่ยก)
     → หรือ "ดี" (ปรับปรุงเล็กน้อยเพื่อ Peak)
   
   ✓ Criteria 2: Potential Uplift
     → ไหน "Gap" สูงสุด?
   
   ✓ Criteria 3: Risk
     → ไหน "เสี่ยง" น้อยสุด?
   
   ✓ Criteria 4: Infrastructure
     → ไหน มี "สิ่งอำนวยความสะดวก" (น้ำ, ถนน)?
   
   ✓ Criteria 5: Farmer Cooperation
     → ไหน เกษตรกร "เต็มใจ" ทำการปรับปรุง?

3. Top 3 Recommendations:
   
   🥇 #1 Province: [Name]
   - Current Yield: ? kg/ไร่
   - Potential: ? kg/ไร่
   - Gap: ? kg (Opportunity!)
   - Risk: [Low/Medium/High]
   - Why: 
     ✓ Gap สูง → ได้กำไรมาก
     ✓ Risk ต่ำ → ลดการขาดทุน
   - Expected ROI: ? %
   
   🥈 #2 Province: [Name]
   - ...
   
   🥉 #3 Province: [Name]
   - ...

4. Strategy:
   - Invest in #1 first (High Return, Low Risk)
   - Expand to #2, #3 ตามความสามารถ

5. Budget Allocation:
   - If Total Budget = 1,000,000 บาท
   - #1: ? % (? บาท)
   - #2: ? % (? บาท)
   - #3: ? % (? บาท)

[Paste rice_yield_dataset.csv]
```

---

## **QUESTION 17: นโยบายเพิ่มผลผลิด**

### **โจทย์:**
```
ช่วยเสนอแนวทางเชิงนโยบายที่สามารถช่วยเพิ่มผลผลิตข้าว 
โดยใช้ข้อมูลสนับสนุน
```

### **PROMPT สำหรับนักศึกษา:**
```
คุณเป็น Government Policy Advisor

จากข้อมูลวิเคราะห์ ขอให้คุณ:

1. ระบุ Current Issues:
   - ผลผลิดเฉลี่ย: 630 kg/ไร่ (vs Target: 700?)
   - ความแตกต่าง: 70 kg/ไร่ (??? %)
   - Root Causes:
     ✓ ความรู้เกษตรกร (Education)
     ✓ วิธีปลูก (Method)
     ✓ ปุ๋ยและการดูแล (Input)
     ✓ การเข้าถึงเทคโนโลยี (Technology)
     ✓ ราคา Input (Economics)

2. Policy Options (ศูนย์รัฐบาล/ส่วนท้องถิ่น):
   
   Policy 1: Subsidy Fertilizer & Pesticide
   - วิธี: ลดราคา NPK + Pesticide 30%
   - Expected Adoption: 90% ของเกษตรกร
   - Expected Yield Gain: +43 kg/ไร่ (NPK benefit)
   - Total Cost: [Budget]
   - Total Benefit: [ยอดขายเพิ่ม × 8 บาท/kg]
   - ROI: ? %
   
   Policy 2: Irrigation Subsidy
   - วิธี: Support Irrigation Infrastructure
   - Expected Adoption: 80%
   - Expected Yield Gain: +30 kg/ไร่
   - Cost: [Infrastructure + Maintenance]
   - Benefit: [ยอดขายเพิ่ม]
   - ROI: ? %
   
   Policy 3: Agricultural Knowledge Program
   - วิธี: Training + Extension Services
   - Expected Adoption: 70%
   - Expected Yield Gain: +25 kg/ไร่ (Best Practices)
   - Cost: [Training + Staff]
   - Benefit: [Long-term + Sustainable]
   - ROI: ? % + Sustainability
   
   Policy 4: Input Support Group
   - วิธี: เชื่อมโยงเกษตรกร (Cooperative)
   - Expected Adoption: 60%
   - Expected Cost Reduction: 15%
   - Expected Yield Gain: +20 kg/ไร่
   - Cost: [Organizing]
   - Benefit: [Long-term Network]

3. Recommended Policy Mix:
   - Combine Policy 1 + 3 (Subsidy + Knowledge)
   - Expected Combined Gain: ? kg/ไร่
   - Total Cost: ?
   - Timeline: ?

4. Success Metrics:
   - KPI 1: % เกษตรกรใช้ NPK + Pesticide
   - KPI 2: % เกษตรกรปฏิบัติ Best Practices
   - KPI 3: Avg Yield ≥ 700 kg/ไร่
   - KPI 4: Sustainability Score?

5. Risk & Mitigation:
   - Risk 1: เกษตรกร ไม่เชื่อหรือ ต้านทาน
     → Mitigation: Demo plots, Incentives
   - Risk 2: ราคา Input ขึ้น
     → Mitigation: Price Control, Subsidy
   - Risk 3: ผลไม่คาดหวัง
     → Mitigation: Pilot Program first

[Paste rice_yield_dataset.csv + weather_yield_prediction_dataset.csv]
```

---

## **QUESTION 18: จัดการความเสี่ยงภูมิอากาศ**

### **โจทย์:**
```
ช่วยเสนอแนวทางในการจัดการความเสี่ยงจากการเปลี่ยนแปลงสภาพภูมิอากาศ 
ที่ส่งผลต่อผลผลิตข้าว โดยอ้างอิงจากข้อมูล
```

### **PROMPT สำหรับนักศึกษา:**
```
คุณเป็น Climate Risk Manager

จากข้อมูล weather_yield_prediction_dataset และ rice_disease_classification_dataset
ขอให้คุณ:

1. ระบุ Climate Risks:
   
   Risk 1: Drought (ภัยแล้ง)
   - Symptom: Rainfall < 1,500 mm/season
   - Frequency: ? ครั้ง ใน 6 ปี
   - Impact: Yield ↓ ? kg/ไร่
   - Affected Area: Province ไหน?
   
   Risk 2: Excessive Rainfall (ฝนหลาก)
   - Symptom: Rainfall > 300 mm/month
   - Frequency: ? ครั้ง
   - Impact: Yield ↓ ?, Disease ↑?
   - Affected Area: ?
   
   Risk 3: Temperature Extremes
   - Too Hot: Temp > 30°C → Crop Stress
   - Too Cold: Temp < 25°C → Slow Growth
   - Frequency: ?
   - Impact: ?
   
   Risk 4: Disease Outbreak
   - Disease Prevalence: 40% (Leaf Spot + Blast)
   - Trigger: High Moisture + Temp 25-28°C
   - Yield Loss: -50 kg/ไร่ ถ้า Severe
   - Management: ?

2. Mitigation Strategies:

   Strategy 1: Water Management (ตัวสำคัญสุด!)
   - Drought Mitigation:
     ✓ Build Irrigation Infrastructure
     ✓ Water Storage (Pond/Dam)
     ✓ Drip Irrigation (สำหรับแห้ง)
     ✓ Rainwater Harvesting
   - Expected Outcome: ลด Drought Impact ไป 70%
   - Cost: ?
   - Benefit: ? kg/ไร่ Gain
   
   - Excessive Rain Mitigation:
     ✓ Drainage System
     ✓ Elevated Beds (ถ้าเป็นไปได้)
     ✓ Proper Field Preparation
   - Expected Outcome: ลด Flood Damage ไป 80%
   
   Strategy 2: Crop Variety Selection
   - เลือกพันธุ์ที่:
     ✓ ทนแห้ง (Drought-Resistant)
     ✓ ทนน้ำท่วม (Flood-Tolerant)
     ✓ ทนโรค (Disease-Resistant)
   - Expected Outcome: Stability ↑, Loss ↓
   - Cost: ข่องพันธุ์อาจแพงกว่า
   - Benefit: Reduced Risk + Insurance
   
   Strategy 3: Crop Calendar Adjustment
   - เปลี่ยนเวลาปลูก:
     ✓ Avoid Peak Rainfall Months
     ✓ Avoid Peak Disease Months
     ✓ Optimize Sunshine Availability
   - Current: Plant May → Harvest Oct
   - Alternative: Plant April → Harvest September?
   - Expected Outcome: Avoid High-Risk Period
   
   Strategy 4: Disease Management
   - Prevention:
     ✓ Use Disease-Resistant Varieties
     ✓ Proper Sanitation (Clean Equipment)
     ✓ Avoid Overcrowding
     ✓ Monitor Early Symptoms
   - Treatment:
     ✓ Spray Fungicide (Leaf Spot: Preventive)
     ✓ Systemic Treatment (Blast: Immediate)
   - Expected Outcome: Reduce Disease Impact 60-80%
   
   Strategy 5: Insurance & Risk Transfer
   - Crop Insurance:
     ✓ Weather Index Insurance
     ✓ Yield Insurance
   - Expected Outcome: Financial Protection
   - Cost: Premium ?% of Gross Income
   
   Strategy 6: Information & Early Warning
   - ติดตาม:
     ✓ Weather Forecast (พยากรณ์อากาศ)
     ✓ Disease Monitoring (ติดตามโรค)
     ✓ Pest Alert (เตือนแมลง)
   - Action: Adjust Management based on Warnings
   - Expected Outcome: Proactive not Reactive

3. Implementation Timeline:

   Phase 1 (ปีนี้): Quick Wins
   - Buy Insurance?
   - Prepare Irrigation Equipment?
   - Train on Disease Monitoring?
   
   Phase 2 (ปีนี้-ปีหน้า): Medium-term
   - Build Drainage/Water System?
   - Switch Crop Variety?
   
   Phase 3 (2-3 ปี): Long-term
   - Complete Infrastructure
   - Sustainability Achieved?

4. Monitoring & Evaluation:
   
   KPI 1: Rainfall Variability (ความแปรผวนของฝน)
   - Current: +/- 300 mm
   - Target: Managed with Irrigation
   
   KPI 2: Disease Incidence
   - Current: 40% plots affected
   - Target: < 20% with Management
   
   KPI 3: Yield Stability
   - Current: 520-720 kg/ไร่ (coefficient of variation = ?)
   - Target: 680-720 kg/ไร่ (Stable & High)
   
   KPI 4: Farmer Resilience
   - Can survive 1 drought + 1 disease outbreak/year?

[Paste weather_yield_prediction_dataset.csv + rice_disease_classification_dataset.csv]
```

---

---

## 📊 **SUMMARY: 18 QUESTIONS**

```
Level 1: Descriptive (ข้อ 1-5)
✓ ข้อ 1: Overall Summary
✓ ข้อ 2: Top/Bottom Performers
✓ ข้อ 3: Trend over Time
✓ ข้อ 4: Basic Statistics
✓ ข้อ 5: Outlier Detection

Level 2: Diagnostic (ข้อ 6-10)
✓ ข้อ 6: Correlation Analysis
✓ ข้อ 7: Weather Impact
✓ ข้อ 8: Problem Area Analysis
✓ ข้อ 9: Regional Comparison
✓ ข้อ 10: Pattern & Seasonality

Level 3: Predictive (ข้อ 11-14)
✓ ข้อ 11: What-If Scenario
✓ ข้อ 12: Forecast Next Year
✓ ข้อ 13: Best Predictor
✓ ข้อ 14: Model Concept

Level 4: Prescriptive (ข้อ 15-18)
✓ ข้อ 15: Increase Yield Strategy
✓ ข้อ 16: Investment Decision
✓ ข้อ 17: Policy Recommendation
✓ ข้อ 18: Climate Risk Management
```

---

## 🎯 **วิธีใช้ 18 Questions นี้:**

### **สำหรับผู้สอน:**
```
1. เลือก Question ที่เหมาะกับ Level ของผู้เรียน
   - Level 1: ผู้เริ่มต้น (Beginner)
   - Level 2: ปานกลาง (Intermediate)
   - Level 3: ค่อนข้างสูง (Advanced)
   - Level 4: สูง (Expert)

2. ให้นักศึกษา Copy Prompt จากเอกสารนี้

3. ให้ Paste Prompt + Dataset ลง AI

4. รอ 15-30 นาที → ได้ Analysis

5. Discuss ผลลัพธ์กับนักศึกษา
```

### **สำหรับนักศึกษา:**
```
1. อ่านโจทย์ (Question)

2. Copy Prompt ที่สอดคล้อง

3. Paste ลง ChatGPT/Claude/Gemini

4. Paste Dataset

5. ส่ง → รอผลลัพธ์

6. ทำความเข้าใจผลลัพธ์

7. นำเสนอให้เพื่อน
```

---

**18 Questions for Agricultural Data Analysis - Complete & Ready! ✅**
