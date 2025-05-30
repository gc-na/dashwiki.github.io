# [דביאן] Debian Almquist Shell (dash) cp שימוש: העתקת קבצים ותיקיות

## סקירה
הפקודה `cp` משמשת להעתקת קבצים ותיקיות במערכת הקבצים של לינוקס. היא מאפשרת למשתמש להעתיק קבצים ממקום אחד לאחר, תוך שמירה על תוכן הקבצים.

## שימוש
התחביר הבסיסי של הפקודה הוא:

```bash
cp [אפשרויות] [ארגומנטים]
```

## אפשרויות נפוצות
- `-r`: העתקת תיקיות באופן רקורסיבי.
- `-i`: בקשה לאישור לפני החלפת קובץ קיים.
- `-u`: העתקת קבצים רק אם הקובץ המקורי חדש יותר או אם הוא לא קיים ביעד.
- `-v`: הצגת פרטי ההעתקה במהלך התהליך.

## דוגמאות נפוצות
הנה כמה דוגמאות שימושיות להעתקת קבצים:

1. העתקת קובץ:
   ```bash
   cp file1.txt file2.txt
   ```

2. העתקת תיקיה באופן רקורסיבי:
   ```bash
   cp -r folder1/ folder2/
   ```

3. העתקת קובץ עם אישור לפני החלפה:
   ```bash
   cp -i file1.txt file2.txt
   ```

4. העתקת קובץ רק אם הוא חדש יותר:
   ```bash
   cp -u file1.txt file2.txt
   ```

5. הצגת פרטי ההעתקה:
   ```bash
   cp -v file1.txt file2.txt
   ```

## טיפים
- תמיד השתמש באופציה `-i` כאשר אתה מעתיק קבצים, כדי למנוע החלפת קבצים בטעות.
- אם אתה מעתיק תיקיות, אל תשכח להשתמש באופציה `-r`.
- בדוק את הקבצים לאחר ההעתקה כדי לוודא שהכל הועתק כראוי.