# [דביאן] Debian Almquist Shell (dash) wget שימוש: הורדת קבצים מהאינטרנט

## Overview
הפקודה `wget` היא כלי עוצמתי להורדת קבצים מהאינטרנט. היא תומכת בפרוטוקולים שונים כמו HTTP, HTTPS ו-FTP, ומאפשרת להוריד קבצים בקלות וביעילות.

## Usage
התחביר הבסיסי של הפקודה הוא:
```
wget [options] [arguments]
```

## Common Options
- `-O <file>`: שמור את הקובץ בשם שצוין במקום השם המקורי.
- `-q`: הפעל מצב שקט, ללא פלט למסך.
- `-c`: המשך הורדה של קובץ שנקטע.
- `-r`: הורדה רRecursive, כלומר הורדת כל הקבצים הקשורים.
- `--limit-rate=<rate>`: הגבל את מהירות ההורדה.

## Common Examples
- הורדת קובץ פשוט:
  ```bash
  wget http://example.com/file.txt
  ```

- שמירת הקובץ בשם שונה:
  ```bash
  wget -O newfile.txt http://example.com/file.txt
  ```

- המשך הורדה של קובץ:
  ```bash
  wget -c http://example.com/largefile.zip
  ```

- הורדת אתר שלם:
  ```bash
  wget -r http://example.com
  ```

- הגבלת מהירות ההורדה:
  ```bash
  wget --limit-rate=200k http://example.com/file.zip
  ```

## Tips
- השתמש באופציה `-q` כדי להוריד קבצים בשקט, במיוחד כשאתה לא רוצה להפריע לעבודה שלך.
- אם אתה מוריד קבצים גדולים, שקול להשתמש באופציה `-c` כדי לא לאבד את ההתקדמות במקרה של הפסקת הורדה.
- תמיד בדוק את הקישורים לפני ההורדה כדי לוודא שהם עדיין פעילים.