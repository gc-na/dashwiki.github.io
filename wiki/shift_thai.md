# [ระบบปฏิบัติการ Debian] Debian Almquist Shell (dash) shift การใช้งาน: เปลี่ยนตำแหน่งของพารามิเตอร์

## Overview
คำสั่ง `shift` ใน Dash ใช้เพื่อเปลี่ยนตำแหน่งของพารามิเตอร์ในสคริปต์ โดยการเลื่อนพารามิเตอร์ไปทางซ้าย ทำให้พารามิเตอร์ที่อยู่ในตำแหน่งแรกถูกลบออกและพารามิเตอร์ที่ตามมาจะถูกเลื่อนขึ้นมาแทนที่

## Usage
รูปแบบพื้นฐานของคำสั่ง `shift` คือ:

```sh
shift [n]
```

โดยที่ `n` เป็นจำนวนพารามิเตอร์ที่ต้องการเลื่อน หากไม่ระบุ `n` จะถือว่ามีค่าเป็น 1

## Common Options
- `n`: จำนวนพารามิเตอร์ที่ต้องการเลื่อน ถ้าระบุค่า `n` จะเลื่อนพารามิเตอร์ออกไป `n` ตำแหน่ง

## Common Examples

### ตัวอย่างที่ 1: เลื่อนพารามิเตอร์ 1 ตำแหน่ง
```sh
#!/bin/dash
set -- one two three
echo "Before shift: $1"  # แสดงผล: Before shift: one
shift
echo "After shift: $1"   # แสดงผล: After shift: two
```

### ตัวอย่างที่ 2: เลื่อนพารามิเตอร์ 2 ตำแหน่ง
```sh
#!/bin/dash
set -- one two three four
echo "Before shift: $1"  # แสดงผล: Before shift: one
shift 2
echo "After shift: $1"   # แสดงผล: After shift: three
```

### ตัวอย่างที่ 3: ใช้ในลูป
```sh
#!/bin/dash
set -- apple banana cherry
while [ "$#" -gt 0 ]; do
    echo "Current fruit: $1"
    shift
done
# แสดงผล:
# Current fruit: apple
# Current fruit: banana
# Current fruit: cherry
```

## Tips
- ใช้ `shift` เมื่อคุณต้องการจัดการกับพารามิเตอร์ในสคริปต์อย่างมีประสิทธิภาพ
- ตรวจสอบจำนวนพารามิเตอร์ที่เหลืออยู่ด้วย `$#` ก่อนที่จะใช้ `shift` เพื่อหลีกเลี่ยงข้อผิดพลาด
- คำนึงถึงการใช้ `shift` ในลูปเพื่อประมวลผลพารามิเตอร์ทั้งหมดในลำดับที่ต้องการ