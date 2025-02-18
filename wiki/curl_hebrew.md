# [דביאן] Debian Almquist Shell (dash) curl שימוש: שליחת בקשות HTTP

## Overview
הפקודה `curl` משמשת לשליחת בקשות HTTP לשרתים שונים. היא מאפשרת להוריד ולשלוח נתונים באינטרנט, ולבצע פעולות שונות כמו קבלת תוכן מדף אינטרנט או שליחת נתונים לשרת.

## Usage
התחביר הבסיסי של הפקודה הוא:

```bash
curl [options] [arguments]
```

## Common Options
- `-X`: לקבוע את סוג הבקשה (GET, POST, וכו').
- `-d`: לשלוח נתונים בגוף הבקשה (למשל, בעת שליחת טופס).
- `-H`: להוסיף כותרות לבקשה.
- `-o`: לשמור את התגובה לקובץ.
- `-I`: לקבל רק את הכותרות של התגובה.

## Common Examples
- **שליחת בקשת GET לדף אינטרנט:**
  ```bash
  curl https://www.example.com
  ```

- **שליחת בקשת POST עם נתונים:**
  ```bash
  curl -X POST -d "name=John&age=30" https://www.example.com/api
  ```

- **הוספת כותרת לבקשה:**
  ```bash
  curl -H "Authorization: Bearer token" https://www.example.com/protected
  ```

- **שמור את התגובה לקובץ:**
  ```bash
  curl -o response.txt https://www.example.com
  ```

- **קבלת רק כותרות התגובה:**
  ```bash
  curl -I https://www.example.com
  ```

## Tips
- השתמש באופציה `-v` כדי לקבל פלט מפורט על הבקשה והתגובה, מה שיכול לעזור בפתרון בעיות.
- אם אתה עובד עם APIs, ודא שאתה מבין את סוגי הבקשות הנדרשות (GET, POST, וכו').
- ניתן לשלב מספר אפשרויות יחד כדי להתאים את הבקשה לצרכים שלך.