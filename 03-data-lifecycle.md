```mermaid
flowchart LR

  A[ทีมงานแก้ข้อมูล<br/>Google Sheets]
  B[n8n ดึงข้อมูล<br/>ตรวจสอบ / แปลง]
  C[บันทึกข้อมูล<br/>Database]
  D[API เรียกใช้ข้อมูล]
  E[Frontend แสดงผล<br/>ให้ลูกค้า]
  F[Feedback / Log]

  A --> B
  B --> C
  C --> D
  D --> E
  E --> F
  F --> C
