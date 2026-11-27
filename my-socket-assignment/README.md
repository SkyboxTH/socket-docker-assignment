# รายงานแบบฝึกหัด Socket API & Docker (Assignment 1 & 2)

**ข้อมูลผู้จัดทำ**
* ชื่อ-นามสกุล: อภิสิทธิ์ ก้องเวหน
* รหัสนักศึกษา: 6714952016
* กลุ่ม/เซคชัน: 2

---

## 🛠️ แบบฝึกหัดที่ 1: ระบบ Chat ด้วย Docker (2 Clients & 1 Server)

### คำอธิบายการทำงาน
ระบบแชทนี้ประยุกต์ใช้ Socket API แบบ TCP ในการส่งข้อมูลระหว่าง Client 2 ตัว ผ่าน Server กลาง โดยรันอยู่ในรูปแบบของ Docker Multi-container และใช้ Docker Compose ในการจัดการ

### ขั้นตอนการเริ่มทำงาน (How to run)
* 1. เปิด Terminal และเข้าไปที่โฟลเดอร์แบบฝึกหัดที่ 1:
   ```bash
   cd exercise-1
   
* 2.สั่งรันคอนเทนเนอร์ทั้งหมดผ่าน Docker Compose:
   ```bash
   docker-compose up --build

* 3.การเข้าใช้งาน Client:
เปิด Terminal ใหม่เพื่อเข้าคอนเทนเนอร์ Client 1:
   ```bash
   docker exec -it chat_client1 python client.py

* 4.เปิด Terminal ใหม่เพื่อเข้าคอนเทนเนอร์ Client 2:
   ```bash
   docker exec -it chat_client2 python client.py

## แบบฝึกหัดที่ 2: เว็บแอปพลิเคชัน Flask และ Socket Server

### คำอธิบายการทำงาน
แอปพลิเคชันหน้าเว็บพัฒนาด้วย Flask รับข้อความผ่านการกดส่งฟอร์ม (POST Method) จากนั้น Flask จะทำหน้าที่เป็น Client ส่งข้อความนั้นต่อไปยัง Socket Server เพื่อทำการสะท้อนข้อมูลกลับ (Echo) และแสดงผลบนหน้าเว็บ

### ขั้นตอนการเริ่มทำงาน (How to run)
* 1.เปิด Terminal และเข้าไปที่โฟลเดอร์แบบฝึกหัดที่ 2:
   ```bash
   cd exercise-2
* 2.สั่งรัน Docker Compose:
   ```bash
   docker-compose up --build
* ปิดเว็บเบราว์เซอร์ไปที่ลิงก์: http://localhost:5000 เพื่อทำการทดสอบส่งข้อความ
