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
