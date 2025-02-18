# [דביאן] Debian Almquist Shell (dash) scp שימוש: העברת קבצים בין מחשבים

## Overview
הפקודה `scp` (Secure Copy Protocol) משמשת להעברת קבצים בין מחשבים בצורה מאובטחת באמצעות SSH. היא מאפשרת למשתמשים להעביר קבצים ממחשב אחד לאחר, בין אם מדובר במחשב מקומי או מרוחק.

## Usage
התחביר הבסיסי של הפקודה הוא:
```
scp [options] [arguments]
```

## Common Options
- `-r`: מעביר תיקיות באופן ריקורסיבי.
- `-P`: מציין את מספר הפורט לשימוש (שימו לב שהאות היא גדולה).
- `-i`: מציין את קובץ המפתח הפרטי לשימוש באימות.
- `-v`: מצב מפורט, מציג מידע נוסף על תהליך ההעברה.

## Common Examples
הנה כמה דוגמאות שימושיות להעברת קבצים עם `scp`:

1. העברת קובץ מקומי לשרת מרוחק:
   ```bash
   scp /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

2. העברת קובץ משרת מרוחק למחשב מקומי:
   ```bash
   scp user@remote_host:/path/to/remote/file.txt /path/to/local/directory/
   ```

3. העברת תיקייה שלמה לשרת מרוחק:
   ```bash
   scp -r /path/to/local/directory/ user@remote_host:/path/to/remote/directory/
   ```

4. העברת קובץ עם פורט מותאם אישית:
   ```bash
   scp -P 2222 /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

## Tips
- תמיד השתמשו ב-`-v` כשאתם נתקל בבעיות כדי לקבל מידע נוסף על מה קורה.
- אם אתם מעבירים קבצים גדולים, שקלו להשתמש ב-`-C` לדחיסת הקבצים במהלך ההעברה.
- ודאו שהחיבור שלכם מאובטח על ידי שימוש במפתחות SSH ולא בסיסמאות כאשר זה אפשרי.