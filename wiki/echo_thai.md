# [ภาษาไทย] Debian Almquist Shell (dash) echo การใช้งาน: แสดงข้อความในเทอร์มินัล

## Overview
คำสั่ง `echo` ใน Dash ใช้สำหรับแสดงข้อความหรือค่าต่าง ๆ ลงในเทอร์มินัล มักใช้ในการแสดงผลข้อมูลหรือการตรวจสอบค่าตัวแปรในสคริปต์

## Usage
รูปแบบพื้นฐานของคำสั่ง `echo` คือ:

```sh
echo [options] [arguments]
```

## Common Options
- `-n`: ไม่แสดง newline หลังจากข้อความ
- `-e`: เปิดใช้งานการแปล escape sequences เช่น `\n` สำหรับการขึ้นบรรทัดใหม่
- `-E`: ปิดการแปล escape sequences (เป็นค่าเริ่มต้น)

## Common Examples
แสดงข้อความธรรมดา:
```sh
echo "สวัสดี, โลก!"
```

แสดงข้อความโดยไม่ขึ้นบรรทัดใหม่:
```sh
echo -n "ข้อความนี้จะอยู่ในบรรทัดเดียวกัน"
```

ใช้ escape sequences:
```sh
echo -e "บรรทัดแรก\nบรรทัดที่สอง"
```

แสดงค่าตัวแปร:
```sh
name="ผู้ใช้"
echo "สวัสดี, $name!"
```

## Tips
- ใช้ `-n` เมื่อคุณต้องการให้ข้อความอยู่ในบรรทัดเดียวกัน
- ใช้ `-e` เพื่อใช้ escape sequences ในการจัดรูปแบบข้อความ
- ตรวจสอบให้แน่ใจว่าคุณใช้เครื่องหมายคำพูดรอบข้อความที่มีช่องว่างเพื่อหลีกเลี่ยงข้อผิดพลาดในการประมวลผล