# [ระบบปฏิบัติการ Debian] Debian Almquist Shell (dash) scp การใช้งาน: คัดลอกไฟล์ระหว่างโฮสต์

## Overview
คำสั่ง `scp` (Secure Copy Protocol) ใช้สำหรับคัดลอกไฟล์หรือไดเรกทอรีระหว่างโฮสต์ที่เชื่อมต่อกันผ่าน SSH โดยจะมีการเข้ารหัสข้อมูลเพื่อความปลอดภัย

## Usage
รูปแบบพื้นฐานของคำสั่ง `scp` คือ:

```bash
scp [options] [source] [destination]
```

## Common Options
- `-r`: คัดลอกไดเรกทอรีและเนื้อหาทั้งหมดภายใน
- `-P port`: ระบุพอร์ตที่ใช้ในการเชื่อมต่อ (พอร์ต SSH ปกติคือ 22)
- `-i identity_file`: ใช้ไฟล์คีย์ส่วนตัวสำหรับการตรวจสอบตัวตน
- `-v`: แสดงข้อมูลการทำงานเพื่อการดีบัก

## Common Examples
1. คัดลอกไฟล์จากเครื่องท้องถิ่นไปยังเซิร์ฟเวอร์:
   ```bash
   scp /path/to/local/file username@remote_host:/path/to/remote/directory
   ```

2. คัดลอกไฟล์จากเซิร์ฟเวอร์ไปยังเครื่องท้องถิ่น:
   ```bash
   scp username@remote_host:/path/to/remote/file /path/to/local/directory
   ```

3. คัดลอกไดเรกทอรีทั้งหมดจากเครื่องท้องถิ่นไปยังเซิร์ฟเวอร์:
   ```bash
   scp -r /path/to/local/directory username@remote_host:/path/to/remote/directory
   ```

4. คัดลอกไฟล์โดยระบุพอร์ตที่ไม่ใช่ค่าเริ่มต้น:
   ```bash
   scp -P 2222 /path/to/local/file username@remote_host:/path/to/remote/directory
   ```

## Tips
- ตรวจสอบให้แน่ใจว่า SSH ทำงานอยู่บนเซิร์ฟเวอร์ที่คุณต้องการคัดลอกไฟล์ไป
- ใช้ `-v` เพื่อดูรายละเอียดการเชื่อมต่อหากคุณพบปัญหา
- คิดให้รอบคอบเกี่ยวกับการใช้คีย์ส่วนตัวเพื่อความปลอดภัยในการเข้าถึงเซิร์ฟเวอร์