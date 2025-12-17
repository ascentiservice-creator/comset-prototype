# Comset Prototype

This repository contains a **prototype web application** for the Comset system.

The purpose of this project is to demonstrate the **user experience (UX)** and **interaction flow** for selecting computer components, viewing configurations, and understanding overall pricing logic.

---

## 🔍 Project Purpose

- Demonstrate Comset concept for internal review
- Present UI/UX flow to management and partners
- Serve as a foundation for future development

---

## ✨ Key Features (Prototype)

- Component selection by category
- Brand-based filtering
- Budget-oriented selection flow
- Real-time total price preview
- Visual representation of selected components

> ⚠️ This is a **prototype version**.  
> Data, pricing logic, and validation rules are for demonstration purposes only.

---

## 🌐 Live Demo

GitHub Pages URL will be available after deployment.

---

## 🛠 Tech Stack

- HTML
- CSS
- JavaScript (Vanilla)

No backend or database is connected in this stage.

---

## 📌 Notes

- This repository is intended for **demo and evaluation purposes**
- Not a production system
- Features and structure may change during development

---


---

## ตัวอย่าง: ผังของคุณ (ใช้ได้ทันทีบน GitHub)

คัดลอกอันนี้ไปวางใน `README.md` หรือไฟล์ `.md` ใดก็ได้ 👇

```mermaid
flowchart LR

  %% ======================
  %% ผู้ใช้งาน
  %% ======================
  U[ผู้ใช้งาน<br/>ลูกค้าและฝ่ายขาย<br/>ใช้งานผ่านเว็บ]

  %% ======================
  %% หน้าเว็บ
  %% ======================
  subgraph FRONTEND[หน้าเว็บจัด Comset]
    FE[เว็บจัดสเปคคอม<br/>แสดงสินค้าและราคา<br/>ให้เลือกอุปกรณ์เป็นชุด]
  end

  %% ======================
  %% แหล่งข้อมูลขององค์กร
  %% ======================
  subgraph DATASOURCE[ข้อมูลขององค์กร]
    GS[ตารางข้อมูลสินค้า<br/>Google Sheets<br/>ทีมงานแก้ไขได้]
    IMG[ที่เก็บรูปสินค้า<br/>ใช้แสดงบนหน้าเว็บ]
  end

  %% ======================
  %% ระบบอัตโนมัติ
  %% ======================
  subgraph AUTOMATION[ระบบอัตโนมัติ]
    N8N[ระบบ n8n<br/>ดึงข้อมูลจาก Sheets<br/>อัปเดตข้อมูลเข้าระบบกลาง]
  end

  %% ======================
  %% ระบบประมวลผลกลาง
  %% ======================
  subgraph BACKEND[ระบบประมวลผลกลาง]
    API[ระบบ API กลาง<br/>รับคำขอจากหน้าเว็บ<br/>ประมวลผลข้อมูล]
    RULE[ระบบตรวจสอบสเปค<br/>เช็คว่าอุปกรณ์<br/>ใส่ร่วมกันได้หรือไม่]
    AI[ระบบช่วยแนะนำสเปค<br/>วิเคราะห์ความคุ้มค่า<br/>และงบประมาณ]
  end

  %% ======================
  %% ฐานข้อมูล
  %% ======================
  subgraph DATABASE[ฐานข้อมูล]
    DB[ฐานข้อมูลกลาง<br/>เก็บข้อมูลสินค้า<br/>และสเปคทั้งหมด]
  end

  %% ======================
  %% การไหลของข้อมูล
  %% ======================
  U --> FE
  FE --> API
  FE --> IMG

  API --> RULE
  API --> AI
  RULE --> API
  AI --> API

  API --> DB
  DB --> API

  GS --> N8N
  N8N --> DB
  N8N --> IMG


© Ascenti Resources — Internal Prototype
