# [لينكس] Debian Almquist Shell (dash) killall الاستخدام: إنهاء العمليات بناءً على الاسم

## Overview
يستخدم أمر `killall` لإنهاء جميع العمليات التي تحمل اسمًا معينًا. يعد هذا الأمر مفيدًا عندما تحتاج إلى إيقاف تشغيل عدة عمليات في وقت واحد دون الحاجة إلى معرفة معرّفات العمليات (PIDs) الخاصة بها.

## Usage
تكون الصيغة الأساسية للأمر كالتالي:

```
killall [options] [arguments]
```

## Common Options
- `-u` : إنهاء العمليات التي تعود لمستخدم معين.
- `-s` : تحديد إشارة معينة لإرسالها إلى العمليات.
- `-q` : تشغيل الأمر في وضع "صامت"، مما يعني عدم عرض أي رسائل خطأ.

## Common Examples
إليك بعض الأمثلة العملية لاستخدام أمر `killall`:

1. إنهاء جميع العمليات التي تحمل اسم "firefox":
   ```bash
   killall firefox
   ```

2. إنهاء جميع العمليات التي تحمل اسم "python":
   ```bash
   killall python
   ```

3. إنهاء جميع العمليات التي تعود لمستخدم معين (على سبيل المثال، المستخدم "john"):
   ```bash
   killall -u john
   ```

4. إرسال إشارة محددة (مثل SIGTERM) لإنهاء العمليات:
   ```bash
   killall -s SIGTERM firefox
   ```

5. تشغيل الأمر في وضع صامت:
   ```bash
   killall -q firefox
   ```

## Tips
- تأكد من أنك تعرف ما تفعله قبل استخدام `killall`، حيث يمكن أن يؤدي إلى إنهاء عمليات مهمة.
- استخدم الخيار `-q` لتجنب الرسائل غير الضرورية عند إنهاء العمليات.
- يمكنك استخدام `pgrep` مع `killall` للحصول على قائمة بالعمليات قبل إنهائها، مما يساعدك على اتخاذ قرار مستنير.