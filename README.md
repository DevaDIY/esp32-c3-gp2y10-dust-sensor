# esp32-c3-gp2y10-dust-sensor
ESP32-C3 อ่านค่าฝุ่นจาก GP2Y10 พร้อมการเฉลี่ย 20 จุด, EMA Filter, แสดงผล OLED และต่อยอดควบคุมพัดลมอัตโนมัติ

# ESP32-C3 GP2Y10 Dust Sensor

โปรเจกต์อ่านค่าฝุ่นด้วย **ESP32-C3 Super Mini** และเซนเซอร์ **Sharp GP2Y10**  
พร้อมแนวทางทำให้ค่านิ่งขึ้นด้วย

- การเฉลี่ยค่า **20 จุด**
- การกรองสัญญาณแบบ **EMA Filter**
- การแสดงผลบน **OLED**
- การต่อยอดไปควบคุม **พัดลมอัตโนมัติ**

เหมาะสำหรับคนที่กำลังเรียน ESP32, งาน Sensor, งาน ADC และสาย Maker DIY ที่อยากเข้าใจหลักการอ่านค่าฝุ่นแบบใช้งานจริง

---

## จุดเด่นของโปรเจกต์

- ใช้บอร์ด **ESP32-C3 Super Mini**
- อ่านค่าจาก **GP2Y10 Dust Sensor**
- ลด noise ด้วย **20-point averaging**
- ทำค่าลื่นขึ้นด้วย **EMA Filter**
- คำนวณจาก `ADC -> Vadc -> Vout -> Dust`
- รองรับการแสดงผลผ่านจอ OLED
- สามารถต่อยอดเป็นระบบเปิดพัดลมอัตโนมัติได้

---

## บทความอธิบายฉบับเต็ม

อ่านบทความแบบละเอียดได้ที่:  
**https://devadiy.com/esp32-c3-gp2y10-dust-sensor/**

บทความที่เกี่ยวข้องจาก DevaDIY:
- Tutorials: https://devadiy.com/tutorials/
- ESP32-C3 Guide: https://devadiy.com/esp32-c3-guide/
- ESP32-C3 Pinout Super Mini: https://devadiy.com/esp32-c3-pinout-super-mini/
- ESP32 คืออะไร: https://devadiy.com/esp32-%E0%B8%84%E0%B8%B7%E0%B8%AD%E0%B8%AD%E0%B8%B0%E0%B9%84%E0%B8%A3/
- ESP32 Analog Read: https://devadiy.com/esp32-analog-read/

---

## อุปกรณ์ที่ใช้

- ESP32-C3 Super Mini
- GP2Y10 Dust Sensor
- OLED 0.96 inch I2C
- Relay / Fan Module
- Resistor divider สำหรับลดแรงดันเข้าขา ADC
- สาย Jumper และแหล่งจ่ายไฟที่นิ่ง

---

## โครงสร้างไฟล์

```bash
.
├── gp2y10.ino
├── config.h
├── sharpAp2y10.h
├── sharpAp2y10.cpp
├── ControlFan.h
├── ControlFan.cpp
├── display.h
└── display.cpp
