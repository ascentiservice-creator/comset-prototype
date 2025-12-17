```mermaid
flowchart TD

  START[เริ่มจัดสเปค]
  INPUT[ผู้ใช้เลือกอุปกรณ์]

  RULE{ผ่านกฎพื้นฐานหรือไม่}
  FAIL[แจ้งเตือน<br/>เลือกไม่ได้]
  WARN[เตือนแต่เลือกได้]

  AI[AI วิเคราะห์<br/>ความคุ้มค่า / งบ]
  RESULT[ได้สเปคแนะนำ]

  START --> INPUT
  INPUT --> RULE

  RULE -->|ไม่ผ่าน| FAIL
  RULE -->|ผ่านแต่เสี่ยง| WARN
  RULE -->|ผ่าน| AI

  WARN --> AI
  AI --> RESULT
