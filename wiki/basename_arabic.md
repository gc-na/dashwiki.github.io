# [لينكس] Debian Almquist Shell (dash) basename الاستخدام: [إزالة مسار الملف]

## Overview
يستخدم أمر `basename` لإزالة مسار الملف وإرجاع اسم الملف فقط. هذا الأمر مفيد عندما تحتاج إلى استخراج اسم الملف من مسار كامل.

## Usage
يمكن استخدام الأمر `basename` بالشكل التالي:

```bash
basename [options] [arguments]
```

## Common Options
- `-a`: يعالج جميع المدخلات في قائمة.
- `-s`: يحدد لاحقة معينة لإزالتها من اسم الملف.

## Common Examples
إليك بعض الأمثلة العملية لاستخدام الأمر `basename`:

1. **إزالة مسار من اسم ملف:**
   ```bash
   basename /home/user/file.txt
   ```
   الناتج سيكون:
   ```
   file.txt
   ```

2. **إزالة لاحقة معينة:**
   ```bash
   basename /home/user/file.txt .txt
   ```
   الناتج سيكون:
   ```
   file
   ```

3. **معالجة قائمة من الملفات:**
   ```bash
   basename -a /home/user/file1.txt /home/user/file2.txt
   ```
   الناتج سيكون:
   ```
   file1.txt
   file2.txt
   ```

## Tips
- استخدم `basename` مع `dirname` للحصول على اسم الملف ومساره بشكل منفصل.
- تأكد من استخدام الخيارات المناسبة مثل `-s` لإزالة اللاحقات غير المرغوب فيها.