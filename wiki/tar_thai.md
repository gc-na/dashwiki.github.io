# [ไทย] Debian Almquist Shell (dash) tar <การใช้งาน>: การบีบอัดและแตกไฟล์

## Overview
คำสั่ง `tar` ใช้สำหรับการบีบอัดไฟล์และโฟลเดอร์ในระบบ Unix/Linux โดยสามารถสร้างไฟล์ archive ที่มีนามสกุล `.tar` หรือบีบอัดไฟล์ด้วยการใช้ตัวเลือกเพิ่มเติม เช่น gzip หรือ bzip2

## Usage
รูปแบบพื้นฐานของคำสั่ง tar คือ:

```bash
tar [options] [arguments]
```

## Common Options
- `-c`: สร้างไฟล์ archive ใหม่
- `-x`: แตกไฟล์ archive
- `-f`: ระบุชื่อไฟล์ archive
- `-v`: แสดงรายละเอียดในระหว่างการทำงาน
- `-z`: บีบอัดด้วย gzip
- `-j`: บีบอัดด้วย bzip2

## Common Examples
- สร้างไฟล์ archive จากโฟลเดอร์:
    ```bash
    tar -cvf archive.tar /path/to/directory
    ```

- แตกไฟล์ archive:
    ```bash
    tar -xvf archive.tar
    ```

- สร้างไฟล์ archive ที่บีบอัดด้วย gzip:
    ```bash
    tar -czvf archive.tar.gz /path/to/directory
    ```

- แตกไฟล์ archive ที่บีบอัดด้วย gzip:
    ```bash
    tar -xzvf archive.tar.gz
    ```

- สร้างไฟล์ archive ที่บีบอัดด้วย bzip2:
    ```bash
    tar -cjvf archive.tar.bz2 /path/to/directory
    ```

- แตกไฟล์ archive ที่บีบอัดด้วย bzip2:
    ```bash
    tar -xjvf archive.tar.bz2
    ```

## Tips
- ใช้ตัวเลือก `-v` เพื่อให้เห็นไฟล์ที่ถูกบีบอัดหรือแตกในระหว่างการทำงาน
- ตรวจสอบขนาดของไฟล์ archive โดยใช้คำสั่ง `du -h archive.tar` ก่อนและหลังการบีบอัด
- หากต้องการบีบอัดไฟล์หลายไฟล์ในครั้งเดียว ให้ระบุชื่อไฟล์ทั้งหมดในคำสั่ง tar เช่น `tar -cvf archive.tar file1 file2 file3`