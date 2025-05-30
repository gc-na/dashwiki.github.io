# [דביאן] Debian Almquist Shell (dash) iotop שימוש: ניטור שימוש ב-I/O של תהליכים

## Overview
הפקודה `iotop` משמשת לניהול ולניטור השימוש ב-I/O (קלט/פלט) של תהליכים במערכת. היא מציגה את התהליכים הפועלים ואת כמות המשאבים שהם צורכים, מה שמאפשר למשתמשים להבין אילו תהליכים משפיעים על ביצועי הדיסק.

## Usage
התחביר הבסיסי של הפקודה הוא:
```bash
iotop [options] [arguments]
```

## Common Options
- `-o`, `--only`: הצג רק תהליכים שמשתמשים ב-I/O.
- `-b`, `--batch`: הפעל במצב באצ' (batch mode) להפקת פלט קבוע.
- `-d`, `--delay`: הגדר את זמן ההשהיה בין עדכונים (במילישניות).
- `-p`, `--pid`: צפה רק בתהליך עם מזהה תהליך ספציפי.

## Common Examples
- להציג את כל התהליכים המשתמשים ב-I/O:
```bash
iotop
```

- להציג רק תהליכים שמשתמשים ב-I/O:
```bash
iotop -o
```

- להפעיל במצב באצ' עם עדכון כל 2 שניות:
```bash
iotop -b -d 2
```

- לצפות בתהליך ספציפי עם מזהה 1234:
```bash
iotop -p 1234
```

## Tips
- השתמש באופציה `-o` כדי למקד את תשומת הלב שלך בתהליכים שצורכים את רוב המשאבים.
- במצב באצ', תוכל להפוך את הפלט לקובץ על ידי הפניית הפלט:
```bash
iotop -b -d 2 > iotop_output.txt
```
- זכור להריץ את `iotop` עם הרשאות מנהל (root) כדי לקבל מידע מלא על כל התהליכים.