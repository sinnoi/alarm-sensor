# เซนเซอร์เตือนภัย

โมเดลนี้ใช้เซนเซอร์วัดระยะ Ultrasonic เพื่อวัดระยะทางไปยังวัตถุและแสดงระยะทางบนชุด LED

## ฮาร์ดแวร์

- Arduino board
- Ultrasonic distance sensor (HC-SR04)
- LED 7 ชิ้น

## การ Setup

1. เชื่อมต่อ Ultrasonic เข้ากับบอร์ด Arduino โดยใช้การเชื่อมต่อพินต่อไปนี้
- VCC (บนเซนเซอร์วัดระยะทาง) to 5V (บน Arduino)
- GND (บนเซนเซอร์วัดระยะทาง) to GND (บน Arduino)
- TRIG (บนเซนเซอร์วัดระยะทาง) to pin 12 (บน Arduino)
- ECHO (บนเซนเซอร์วัดระยะทาง) to pin 13 (บน Arduino)

2. เชื่อม LED ไปยัง Arduino board โดยการเชื่อมพินต่อไปนี้ :

- Anode ของ LED 1 ไปยัง พิน 8 (บน Arduino)
- Cathode ของ LED 1 ไปยัง GND (บน Arduino)
- Anode ของ LED 2 ไปยัง พิน 7 (บน Arduino)
- Cathode ของ LED 2 ไปยัง GND (บน Arduino)
- Anode ของ LED 3 ไปยัง พิน 6 (บน Arduino)
- Cathode ของ LED 3 ไปยัง GND (บน Arduino)
- Anode ของ LED 4 ไปยัง พิน 5 (บน Arduino)
- Cathode ของ LED 4 ไปยัง GND (บน Arduino)
- Anode ของ LED 5 ไปยัง พิน 4 (บน Arduino)
- Cathode ของ LED 5 ไปยัง GND (บน Arduino)
- Anode ของ LED 6 ไปยัง พิน 3 (บน Arduino)
- Cathode ของ LED 6 ไปยัง GND (บน Arduino) 
- Anode ของ LED 7 ไปยัง พิน 2 (บน Arduino)
- Cathode ของ LED 7 ไปยัง GND (บน Arduino)

3. อัปโหลดไปยังบอร์ด Arduino

## หลักการทำงาน

เมื่อโค้ดถูกอัปโหลดไปยังบอร์ด Arduino แล้ว ระยะทางไปยังวัตถุจะถูกวัดและแสดงบนไฟ LED ไฟ LED ที่ใกล้ที่สุดกับเซ็นเซอร์วัดระยะจะสว่างขึ้นสำหรับระยะทางสูงสุด 7 ซม. ไฟ LED ถัดไปจะสว่างขึ้นสำหรับระยะทางสูงสุด 14 ซม. ไปเรื่อยๆ หากระยะห่างมากกว่า 49 ซม. ไฟ LED ทั้งหมดจะดับลง การวัดระยะทางและจอแสดงผล LED จะได้รับการอัปเดตอย่างต่อเนื่อง
