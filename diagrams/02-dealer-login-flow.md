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

