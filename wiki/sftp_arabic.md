# [نظام التشغيل] Debian Almquist Shell (dash) sftp الاستخدام: نقل الملفات بشكل آمن

## Overview
أمر `sftp` (Secure File Transfer Protocol) يُستخدم لنقل الملفات بشكل آمن بين الأنظمة عبر شبكة. يعتمد هذا البروتوكول على SSH (Secure Shell) لتوفير نقل آمن للبيانات، مما يجعله خيارًا شائعًا لنقل الملفات الحساسة.

## Usage
تكون الصيغة الأساسية لأمر `sftp` كالتالي:

```bash
sftp [options] [user@]host
```

## Common Options
- `-P port`: تحديد رقم المنفذ الذي يجب الاتصال به.
- `-o option`: تمرير خيارات إضافية إلى SSH.
- `-b batchfile`: استخدام ملف دفعة لتنفيذ الأوامر بشكل غير تفاعلي.

## Common Examples
- **الاتصال بخادم SFTP:**
  ```bash
  sftp user@hostname
  ```

- **نقل ملف من النظام المحلي إلى الخادم:**
  ```bash
  sftp user@hostname:/path/to/remote/directory <<< $'put /path/to/local/file'
  ```

- **تنزيل ملف من الخادم إلى النظام المحلي:**
  ```bash
  sftp user@hostname:/path/to/remote/file <<< $'get /path/to/local/directory'
  ```

- **عرض الملفات في الدليل البعيد:**
  ```bash
  sftp user@hostname <<< $'ls'
  ```

## Tips
- تأكد من استخدام اسم مستخدم وكلمة مرور قوية عند الاتصال بخادم SFTP.
- استخدم خيار `-P` لتحديد منفذ مختلف إذا كان الخادم لا يستخدم المنفذ الافتراضي 22.
- من الجيد استخدام ملفات المفاتيح العامة والخاصة لتسهيل الاتصال بدون الحاجة إلى إدخال كلمة المرور في كل مرة.