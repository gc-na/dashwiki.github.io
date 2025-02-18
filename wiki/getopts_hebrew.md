# [דביאן] Debian Almquist Shell (dash) getopts שימוש: ניתוח אפשרויות של סקריפטים

## Overview
הפקודה `getopts` משמשת לניתוח אפשרויות (options) שנשלחות לסקריפטים ב-Dash. היא מאפשרת לסקריפט לקבל אפשרויות מהשורה הראשונה של הפקודה, מה שמקל על ניהול פרמטרים שונים.

## Usage
הסינטקס הבסיסי של הפקודה הוא:
```sh
getopts optstring variable
```

## Common Options
- `optstring`: מחרוזת המגדירה את האפשרויות שיכולות להתקבל. כל תו במחרוזת מייצג אפשרות, ותו המופיע פעמיים מציין שאפשרות זו יכולה לקבל ערך.
- `variable`: משתנה שבו יישמרו הערכים של האפשרויות שנקלטו.

## Common Examples

### דוגמה בסיסית
```sh
#!/bin/dash

while getopts "ab:c" opt; do
  case $opt in
    a)
      echo "Option A selected"
      ;;
    b)
      echo "Option B selected with value: $OPTARG"
      ;;
    c)
      echo "Option C selected"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```

### דוגמה עם ערך
```sh
#!/bin/dash

while getopts "f:" opt; do
  case $opt in
    f)
      echo "File name provided: $OPTARG"
      ;;
    *)
      echo "Usage: script.sh -f filename"
      ;;
  esac
done
```

### דוגמה עם מספר אפשרויות
```sh
#!/bin/dash

while getopts "abc" opt; do
  case $opt in
    a)
      echo "Option A"
      ;;
    b)
      echo "Option B"
      ;;
    c)
      echo "Option C"
      ;;
    *)
      echo "Usage: script.sh [-a] [-b] [-c]"
      ;;
  esac
done
```

## Tips
- תמיד השתמשו ב-`case` כדי לנהל את האפשרויות, זה מקל על הקריאות והתחזוקה של הקוד.
- השתמשו ב-`OPTARG` כדי לגשת לערכים של אפשרויות שדורשות ערך.
- ודאו שהסקריפט שלכם כולל טיפול בשגיאות עבור אפשרויות לא חוקיות כדי לשפר את חוויית המשתמש.