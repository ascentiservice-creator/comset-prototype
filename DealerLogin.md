```mermaid

flowchart LR
  U[Dealer เข้าเว็บ Comset] --> C{Login แล้วหรือยัง?}

  C -- ยัง --> G[Guest Mode]
  G --> G1[ดู Demo Comset]
  G --> G2[เห็นราคา SRP เท่านั้น]
  G --> G3[ปุ่ม Login สำหรับ Dealer]

  C -- ใช่ --> D[Dealer Dashboard]
  D --> D1[โหลด Profile Dealer]
  D --> D2[แสดงราคา SDP + SRP]
  D --> D3[เริ่มจัด Comset]

  D3 --> S1[Save Comset]
  D3 --> S2[Send to Sales]
  D3 --> S3[Export / Share Spec]

  S2 --> SALES[ฝ่ายขายรับ Lead]
