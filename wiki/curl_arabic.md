# [نظام التشغيل] Debian Almquist Shell (dash) curl الاستخدام: نقل البيانات عبر الشبكة

## Overview
أداة `curl` هي أداة قوية تستخدم لنقل البيانات عبر الشبكات باستخدام بروتوكولات مختلفة مثل HTTP وHTTPS وFTP. يمكن استخدامها لتحميل الملفات أو إرسال البيانات إلى الخوادم.

## Usage
التركيب الأساسي للأمر هو:

```bash
curl [options] [arguments]
```

## Common Options
- `-O`: تحميل الملف بنفس اسم الملف الموجود على الخادم.
- `-o [filename]`: تحميل الملف وإعادة تسميته إلى الاسم المحدد.
- `-I`: عرض رؤوس الاستجابة فقط.
- `-d [data]`: إرسال بيانات عبر POST.
- `-H [header]`: إضافة رأس مخصص إلى الطلب.

## Common Examples
- تحميل ملف من الإنترنت:
```bash
curl -O https://example.com/file.txt
```

- تحميل ملف وإعادة تسميته:
```bash
curl -o myfile.txt https://example.com/file.txt
```

- عرض رؤوس استجابة HTTP:
```bash
curl -I https://example.com
```

- إرسال بيانات عبر POST:
```bash
curl -d "param1=value1&param2=value2" https://example.com/submit
```

- إضافة رأس مخصص إلى الطلب:
```bash
curl -H "Authorization: Bearer token" https://example.com/protected
```

## Tips
- تأكد من استخدام الخيار `-O` لتحميل الملفات بنفس الاسم لتجنب الارتباك.
- استخدم الخيار `-I` للتحقق من حالة الخادم قبل تحميل الملفات.
- يمكنك استخدام `-v` للحصول على معلومات تفصيلية حول الطلب والاستجابة، مما يساعد في استكشاف الأخطاء.