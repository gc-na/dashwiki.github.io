# [ديبيان] Debian Almquist Shell (dash) scp: نقل الملفات بأمان

## Overview
أمر `scp` (Secure Copy Protocol) يُستخدم لنقل الملفات بين الأنظمة بشكل آمن عبر بروتوكول SSH. يتيح لك هذا الأمر نقل الملفات والمجلدات من جهاز إلى آخر بطريقة مشفرة، مما يحافظ على خصوصية البيانات.

## Usage
التركيب الأساسي للأمر هو كما يلي:
```bash
scp [options] [source] [destination]
```

## Common Options
- `-r`: لنقل المجلدات بشكل متكرر.
- `-P`: لتحديد رقم المنفذ (port) عند الاتصال بالخادم.
- `-i`: لتحديد ملف المفتاح الخاص عند استخدام المصادقة بالمفتاح.
- `-v`: لتفعيل وضع التصحيح (verbose) لعرض تفاصيل إضافية عن عملية النقل.

## Common Examples
- لنقل ملف من جهاز محلي إلى خادم بعيد:
```bash
scp /path/to/local/file username@remote_host:/path/to/remote/directory
```

- لنقل ملف من خادم بعيد إلى جهاز محلي:
```bash
scp username@remote_host:/path/to/remote/file /path/to/local/directory
```

- لنقل مجلد كامل من جهاز محلي إلى خادم بعيد:
```bash
scp -r /path/to/local/directory username@remote_host:/path/to/remote/directory
```

- لنقل ملف باستخدام منفذ مخصص:
```bash
scp -P 2222 /path/to/local/file username@remote_host:/path/to/remote/directory
```

## Tips
- تأكد من أن لديك الأذونات اللازمة على كلا الجهازين لنقل الملفات.
- استخدم خيار `-v` لتشخيص أي مشاكل قد تواجهها أثناء النقل.
- إذا كنت تنقل ملفات كبيرة، يمكنك استخدام `-C` لتمكين الضغط، مما قد يسرع عملية النقل.