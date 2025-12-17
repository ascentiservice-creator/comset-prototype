# Dealer Login Flow

```mermaid
flowchart LR
  U[User เข้าเว็บ Comset] --> C{Login แล้วหรือยัง}

  C -- ยัง --> G[Guest Mode]
  G --> G1[จัด Comset Demo]
  G --> G2[เห็นราคา SRP]
  G --> G3[ปุ่ม Login Dealer]

  C -- ใช่ --> D[Dealer Mode]
  D --> D1[เห็นราคา SDP<br/>และ SRP]
  D --> D2[Save Comset History]
  D --> D3[Send Comset to Sales]



---

# 03️⃣ Comset Build Flow (User Journey)

📄 `diagrams/03-comset-build-flow.md`

```md
# Comset Build Flow

```mermaid
flowchart TB
  START[เริ่มจัด Comset] --> SEL[เลือกอุปกรณ์<br/>ตาม Category]

  SEL --> CHECK[ตรวจสอบ Compatibility]
  CHECK -->|ผ่าน| ADD[เพิ่มเข้า Comset]
  CHECK -->|ไม่ผ่าน| WARN[แจ้งเตือน<br/>หรือ Block]

  ADD --> TOTAL[คำนวณราคารวม]
  TOTAL --> BUDGET{เกินงบหรือไม่}

  BUDGET -- ไม่ --> OK[แสดงว่าเหมาะสม]
  BUDGET -- ใช่ --> SUGGEST[แนะนำปรับสเปค]

  OK --> END[พร้อม Save<br/>หรือ Send]
