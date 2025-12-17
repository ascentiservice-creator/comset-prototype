## Rule-based Compatibility Engine

### ตัวอย่าง Rule
- Case.maxVga >= Vga.length
- PSU.watt >= GPU.minWatt
- CPU.socket == Mainboard.socket

### Output
- PASS
- WARN (แนะนำ)
- BLOCK (ใส่ไม่ได้)
