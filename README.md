# CS372_MiniProject1_Predicting_Student_Academic_Performance

## **ตารางคำอธิบายตัวแปร (Data Dictionary)**

| ลำดับ | ชื่อคอลัมน์ | ประเภทข้อมูล           | บทบาท                | รายละเอียด / ความหมาย                                                                |
| ----- | ----------- | ---------------------- | -------------------- | ------------------------------------------------------------------------------------ |
| 1     | school      | Categorical (Binary)   | Feature              | โรงเรียนของนักเรียน: `GP` (Gabriel Pereira) หรือ `MS` (Mousinho da Silveira)         |
| 2     | subject     | Categorical (Nominal)  | Feature              | รายวิชา: `math` (คณิตศาสตร์) หรือ `portuguese` (ภาษาโปรตุเกส) เพิ่มเข้ามาหลังรวมไฟล์ |
| 3     | sex         | Categorical (Binary)   | Feature              | เพศของนักเรียน: `F` (หญิง), `M` (ชาย)                                                |
| 4     | age         | Numerical (Discrete)   | Feature              | อายุของนักเรียน (15–22 ปี)                                                           |
| 5     | address     | Categorical (Binary)   | Feature              | ที่อยู่อาศัย: `U` (Urban), `R` (Rural)                                               |
| 6     | famsize     | Categorical (Binary)   | Feature              | ขนาดครอบครัว: `LE3` (≤3 คน), `GT3` (>3 คน)                                           |
| 7     | Pstatus     | Categorical (Binary)   | Feature              | สถานะการอยู่ร่วมกันของพ่อแม่: `T` (อยู่ด้วยกัน), `A` (แยกกันอยู่)                    |
| 8     | Medu        | Numerical (Ordinal)    | Feature              | ระดับการศึกษาของแม่ (0–4)                                                            |
| 9     | Fedu        | Numerical (Ordinal)    | Feature              | ระดับการศึกษาของพ่อ (0–4)                                                            |
| 10    | Mjob        | Categorical (Nominal)  | Feature              | อาชีพแม่: teacher, health, services, at_home, other                                  |
| 11    | Fjob        | Categorical (Nominal)  | Feature              | อาชีพพ่อ: teacher, health, services, at_home, other                                  |
| 12    | reason      | Categorical (Nominal)  | Feature              | เหตุผลที่เลือกโรงเรียน: home, reputation, course, other                              |
| 13    | guardian    | Categorical (Nominal)  | Feature              | ผู้ปกครองหลัก: mother, father, other                                                 |
| 14    | traveltime  | Numerical (Ordinal)    | Feature              | เวลาเดินทางไปโรงเรียน (1–4)                                                          |
| 15    | studytime   | Numerical (Ordinal)    | Feature              | เวลาอ่านหนังสือต่อสัปดาห์ (1–4)                                                      |
| 16    | failures    | Numerical (Discrete)   | Feature              | จำนวนครั้งที่เคยสอบตก (0–4)                                                          |
| 17    | schoolsup   | Categorical (Binary)   | Feature              | ได้รับการสนับสนุนพิเศษจากโรงเรียน (yes/no)                                           |
| 18    | famsup      | Categorical (Binary)   | Feature              | ได้รับการสนับสนุนทางการศึกษาจากครอบครัว (yes/no)                                     |
| 19    | paid        | Categorical (Binary)   | Feature              | เรียนพิเศษแบบเสียเงินในรายวิชานั้น (yes/no)                                          |
| 20    | activities  | Categorical (Binary)   | Feature              | เข้าร่วมกิจกรรมนอกหลักสูตร (yes/no)                                                  |
| 21    | nursery     | Categorical (Binary)   | Feature              | เคยเรียนอนุบาลหรือไม่ (yes/no)                                                       |
| 22    | higher      | Categorical (Binary)   | Feature              | ต้องการเรียนต่อระดับอุดมศึกษา (yes/no)                                               |
| 23    | internet    | Categorical (Binary)   | Feature              | มีอินเทอร์เน็ตที่บ้าน (yes/no)                                                       |
| 24    | romantic    | Categorical (Binary)   | Feature              | มีความสัมพันธ์เชิงชู้สาว (yes/no)                                                    |
| 25    | famrel      | Numerical (Ordinal)    | Feature              | คุณภาพความสัมพันธ์ในครอบครัว (1–5)                                                   |
| 26    | freetime    | Numerical (Ordinal)    | Feature              | เวลาว่างหลังเลิกเรียน (1–5)                                                          |
| 27    | goout       | Numerical (Ordinal)    | Feature              | ความถี่ในการออกไปเที่ยวกับเพื่อน (1–5)                                               |
| 28    | Dalc        | Numerical (Ordinal)    | Feature              | การดื่มแอลกอฮอล์วันธรรมดา (1–5)                                                      |
| 29    | Walc        | Numerical (Ordinal)    | Feature              | การดื่มแอลกอฮอล์วันหยุด (1–5)                                                        |
| 30    | health      | Numerical (Ordinal)    | Feature              | สถานะสุขภาพปัจจุบัน (1–5)                                                            |
| 31    | absences    | Numerical (Discrete)   | Feature              | จำนวนครั้งที่ขาดเรียน (0–93)                                                         |
| 32    | G1          | Numerical (Continuous) | Feature              | คะแนนสอบเทอม 1 (0–20)                                                                |
| 33    | G2          | Numerical (Continuous) | Feature              | คะแนนสอบเทอม 2 (0–20)                                                                |
| 34    | G3          | Numerical (Continuous) | *ไม่ใช้เป็น Feature* | คะแนนสอบปลายภาค (0–20) — ใช้สร้าง Target                                             |
| 35    | target      | Categorical (Binary)   | Target               | ตัวแปรเป้าหมาย: 1 = ผ่าน (G3 ≥ 10), 0 = ไม่ผ่าน (G3 < 10)                            |

---

### **บทบาทของตัวแปรในโมเดล**
* Feature ทั้งหมด = ทุกตัวแปรยกเว้น G3
* Target = target (ผ่าน/ไม่ผ่าน)
* ป้องกัน Data Leakage = ไม่นำ G3 เข้าโมเดล
