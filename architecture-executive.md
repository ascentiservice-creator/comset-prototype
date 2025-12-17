```mermaid
flowchart LR

  U[ผู้ใช้งาน<br/>ลูกค้า / ฝ่ายขาย]

  subgraph WEB[แพลตฟอร์ม Comset]
    FE[เว็บจัดสเปคคอม<br/>เลือกอุปกรณ์<br/>เห็นราคา]
  end

  subgraph ORG[ข้อมูลขององค์กร]
    DATA[ข้อมูลสินค้าและราคา<br/>แก้ไขโดยทีมงาน]
  end

  subgraph SYSTEM[ระบบอัจฉริยะ]
    CORE[ระบบประมวลผลกลาง<br/>ตรวจสอบสเปค<br/>แนะนำชุดที่เหมาะสม]
  end

  DB[(ฐานข้อมูลกลาง)]

  U --> FE
  FE --> CORE
  CORE --> FE

  DATA --> CORE
  CORE --> DB
