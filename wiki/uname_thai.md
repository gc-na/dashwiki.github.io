# [ไทย] Debian Almquist Shell (dash) uname การใช้งาน: แสดงข้อมูลเกี่ยวกับระบบ

## Overview
คำสั่ง `uname` ใช้เพื่อแสดงข้อมูลเกี่ยวกับระบบปฏิบัติการและฮาร์ดแวร์ที่กำลังใช้งานอยู่ เช่น ชื่อของระบบปฏิบัติการ เวอร์ชัน และประเภทของฮาร์ดแวร์

## Usage
รูปแบบพื้นฐานของคำสั่ง `uname` มีดังนี้:
```
uname [options] [arguments]
```

## Common Options
- `-a`: แสดงข้อมูลทั้งหมดเกี่ยวกับระบบ
- `-s`: แสดงชื่อของระบบปฏิบัติการ
- `-n`: แสดงชื่อของโฮสต์
- `-r`: แสดงเวอร์ชันของเคอร์เนล
- `-v`: แสดงข้อมูลเพิ่มเติมเกี่ยวกับเวอร์ชันของเคอร์เนล
- `-m`: แสดงประเภทของฮาร์ดแวร์

## Common Examples
1. แสดงข้อมูลทั้งหมดเกี่ยวกับระบบ:
   ```sh
   uname -a
   ```

2. แสดงชื่อของระบบปฏิบัติการ:
   ```sh
   uname -s
   ```

3. แสดงเวอร์ชันของเคอร์เนล:
   ```sh
   uname -r
   ```

4. แสดงชื่อของโฮสต์:
   ```sh
   uname -n
   ```

5. แสดงประเภทของฮาร์ดแวร์:
   ```sh
   uname -m
   ```

## Tips
- ใช้ `uname -a` เพื่อรับข้อมูลที่ครบถ้วนที่สุดเกี่ยวกับระบบในครั้งเดียว
- คำสั่ง `uname` เป็นเครื่องมือที่มีประโยชน์ในการตรวจสอบความเข้ากันได้ของซอฟต์แวร์กับระบบปฏิบัติการของคุณ
- หากคุณต้องการใช้คำสั่งในสคริปต์ ให้พิจารณาใช้ตัวเลือกที่เฉพาะเจาะจงเพื่อให้ได้ข้อมูลที่ต้องการอย่างแม่นยำ