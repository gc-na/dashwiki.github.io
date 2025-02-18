# [דביאן] Debian Almquist Shell (dash) shift שימוש: שינוי מיקום ארגומנטים

## Overview
הפקודה `shift` ב-dash משמשת להזיז את הארגומנטים המועברים לסקריפט או לפונקציה. כאשר אתה מפעיל את הפקודה, הארגומנט הראשון (הראשי) נמחק, וכל הארגומנטים הנותרים זזים למקום הראשון.

## Usage
התחביר הבסיסי של הפקודה הוא:

```
shift [n]
```

כאשר `n` הוא מספר הארגומנטים שברצונך להזיז. אם לא מצוין מספר, הפקודה תזיז את הארגומנט הראשון בלבד.

## Common Options
- `n`: מספר הארגומנטים שברצונך להזיז. אם לא מצוין, ברירת המחדל היא 1.

## Common Examples

### דוגמה 1: הזזת ארגומנט אחד
```sh
#!/bin/dash
set -- arg1 arg2 arg3
echo "Before shift: $1"  # פלט: Before shift: arg1
shift
echo "After shift: $1"   # פלט: After shift: arg2
```

### דוגמה 2: הזזת שני ארגומנטים
```sh
#!/bin/dash
set -- arg1 arg2 arg3 arg4
echo "Before shift: $1"  # פלט: Before shift: arg1
shift 2
echo "After shift: $1"   # פלט: After shift: arg3
```

### דוגמה 3: שימוש עם לולאה
```sh
#!/bin/dash
set -- one two three four
while [ "$#" -gt 0 ]; do
    echo "Current argument: $1"
    shift
done
# פלט:
# Current argument: one
# Current argument: two
# Current argument: three
# Current argument: four
```

## Tips
- השתמש ב-`shift` כאשר אתה צריך לעבור על רשימת ארגומנטים בלולאה.
- זכור לבדוק את מספר הארגומנטים שנותרו (`$#`) לפני השימוש ב-`shift` כדי למנוע שגיאות.
- ניתן לשלב את `shift` עם פקודות אחרות כמו `case` כדי לנהל בצורה טובה יותר את הארגומנטים.