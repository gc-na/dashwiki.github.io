# [דביאן] Debian Almquist Shell (dash) grep שימוש: חיפוש טקסט בקבצים

## Overview
הפקודה `grep` משמשת לחיפוש טקסט בתוכן של קבצים. היא מאפשרת למצוא שורות המכילות תבניות ספציפיות, מה שהופך אותה לכלי שימושי מאוד בניתוח טקסטים ובסקריפטים.

## Usage
התחביר הבסיסי של הפקודה הוא:
```bash
grep [אפשרויות] [ארגומנטים]
```

## Common Options
- `-i`: מתעלם מהבדלי רישיות בעת החיפוש.
- `-v`: מחזיר שורות שאינן תואמות לתבנית.
- `-r`: מחפש בתיקיות בצורה רקורסיבית.
- `-n`: מציג את מספר השורה שבה נמצאה ההתאמה.
- `-l`: מציג את שמות הקבצים בלבד שבהם נמצאה ההתאמה.

## Common Examples
- חיפוש מילה בקובץ:
```bash
grep "מילה" קובץ.txt
```

- חיפוש מילה בכל הקבצים בתיקייה:
```bash
grep "מילה" *
```

- חיפוש מילה בתיקייה בצורה רקורסיבית:
```bash
grep -r "מילה" תיקייה/
```

- חיפוש מילה תוך התעלמות מהבדלי רישיות:
```bash
grep -i "מילה" קובץ.txt
```

- חיפוש מילה והצגת מספר השורה:
```bash
grep -n "מילה" קובץ.txt
```

## Tips
- השתמש באפשרות `-v` כדי למצוא שורות שאינן מכילות את התבנית, זה יכול להיות שימושי לסינון תוצאות.
- כשאתה מחפש בתיקיות, השתמש באפשרות `-r` כדי לחסוך זמן ולא לחפש בכל קובץ בנפרד.
- אם אתה עובד עם קבצים גדולים, שקול להשתמש באפשרות `--color` כדי להדגיש את ההתאמות, מה שמקל על הקריאה.