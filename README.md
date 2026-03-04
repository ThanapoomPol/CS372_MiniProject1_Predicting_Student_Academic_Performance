# CS372_MiniProject1_Predicting_Student_Academic_Performance

**จัดทำโดย**
* ธนภูมิ พลเมืองดี รหัสนักศึกษา 6609611972
* พฤกษ์ ฤกขะวุฒิกุล รหัสนักศึกษา 6609612137
* สุภนัย จิรกาลกุล รหัสนักศึกษา 6609612269

## **ตารางคำอธิบายตัวแปร (Data Dictionary)**

| ลำดับ | ชื่อคอลัมน์ | ประเภทข้อมูล           | บทบาท                | รายละเอียด / ความหมาย                                                                |
| ----- | ----------- | ---------------------- | -------------------- | ------------------------------------------------------------------------------------ |
| 1     | school      | Categorical (Binary)   | Feature              | โรงเรียนของนักเรียน: `GP` (Gabriel Pereira) หรือ `MS` (Mousinho da Silveira)         |
| 2     | sex         | Categorical (Binary)   | Feature              | เพศของนักเรียน: `F` (หญิง), `M` (ชาย)                                                |
| 3     | age         | Numerical (Discrete)   | Feature              | อายุของนักเรียน (15–22 ปี)                                                           |
| 4     | address     | Categorical (Binary)   | Feature              | ที่อยู่อาศัย: `U` (Urban), `R` (Rural)                                               |
| 5     | famsize     | Categorical (Binary)   | Feature              | ขนาดครอบครัว: `LE3` (≤3 คน), `GT3` (>3 คน)                                           |
| 6     | Pstatus     | Categorical (Binary)   | Feature              | สถานะการอยู่ร่วมกันของพ่อแม่: `T` (อยู่ด้วยกัน), `A` (แยกกันอยู่)                    |
| 7     | Medu        | Numerical (Ordinal)    | Feature              | ระดับการศึกษาของแม่ (0–4)                                                            |
| 8     | Fedu        | Numerical (Ordinal)    | Feature              | ระดับการศึกษาของพ่อ (0–4)                                                            |
| 9     | Mjob        | Categorical (Nominal)  | Feature              | อาชีพแม่: teacher, health, services, at_home, other                                  |
| 10    | Fjob        | Categorical (Nominal)  | Feature              | อาชีพพ่อ: teacher, health, services, at_home, other                                  |
| 11    | reason      | Categorical (Nominal)  | Feature              | เหตุผลที่เลือกโรงเรียน: home, reputation, course, other                              |
| 12    | guardian    | Categorical (Nominal)  | Feature              | ผู้ปกครองหลัก: mother, father, other                                                 |
| 13    | traveltime  | Numerical (Ordinal)    | Feature              | เวลาเดินทางไปโรงเรียน (1–4)                                                          |
| 14    | studytime   | Numerical (Ordinal)    | Feature              | เวลาอ่านหนังสือต่อสัปดาห์ (1–4)                                                      |
| 15    | failures    | Numerical (Discrete)   | Feature              | จำนวนครั้งที่เคยสอบตก (0–4)                                                          |
| 16    | schoolsup   | Categorical (Binary)   | Feature              | ได้รับการสนับสนุนพิเศษจากโรงเรียน (yes/no)                                           |
| 17    | famsup      | Categorical (Binary)   | Feature              | ได้รับการสนับสนุนทางการศึกษาจากครอบครัว (yes/no)                                     |
| 18    | paid        | Categorical (Binary)   | Feature              | เรียนพิเศษแบบเสียเงินในรายวิชานั้น (yes/no)                                          |
| 19    | activities  | Categorical (Binary)   | Feature              | เข้าร่วมกิจกรรมนอกหลักสูตร (yes/no)                                                  |
| 20    | nursery     | Categorical (Binary)   | Feature              | เคยเรียนอนุบาลหรือไม่ (yes/no)                                                       |
| 21    | higher      | Categorical (Binary)   | Feature              | ต้องการเรียนต่อระดับอุดมศึกษา (yes/no)                                               |
| 22    | internet    | Categorical (Binary)   | Feature              | มีอินเทอร์เน็ตที่บ้าน (yes/no)                                                       |
| 23    | romantic    | Categorical (Binary)   | Feature              | มีความสัมพันธ์เชิงชู้สาว (yes/no)                                                    |
| 24    | famrel      | Numerical (Ordinal)    | Feature              | คุณภาพความสัมพันธ์ในครอบครัว (1–5)                                                   |
| 25    | freetime    | Numerical (Ordinal)    | Feature              | เวลาว่างหลังเลิกเรียน (1–5)                                                          |
| 26    | goout       | Numerical (Ordinal)    | Feature              | ความถี่ในการออกไปเที่ยวกับเพื่อน (1–5)                                               |
| 27    | Dalc        | Numerical (Ordinal)    | Feature              | การดื่มแอลกอฮอล์วันธรรมดา (1–5)                                                      |
| 28    | Walc        | Numerical (Ordinal)    | Feature              | การดื่มแอลกอฮอล์วันหยุด (1–5)                                                        |
| 29    | health      | Numerical (Ordinal)    | Feature              | สถานะสุขภาพปัจจุบัน (1–5)                                                            |
| 30    | absences    | Numerical (Discrete)   | Feature              | จำนวนครั้งที่ขาดเรียน (0–93)                                                         |
| 31    | G1          | Numerical (Continuous) | Feature              | คะแนนสอบเทอม 1 (0–20)                                                                |
| 32    | G2          | Numerical (Continuous) | Feature              | คะแนนสอบเทอม 2 (0–20)                                                                |
| 33    | G3          | Numerical (Continuous) | *ไม่ใช้เป็น Feature* | คะแนนสอบปลายภาค (0–20) — ใช้สร้าง Target                                             |
