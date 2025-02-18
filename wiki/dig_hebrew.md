# [דביאן] Debian Almquist Shell (dash) dig שימוש: קבלת מידע על DNS

## Overview
הפקודה `dig` (Domain Information Groper) משמשת לביצוע שאילתות DNS (Domain Name System). היא מאפשרת למשתמשים לקבל מידע על כתובות IP, רשומות DNS שונות ועוד, בצורה פשוטה וברורה.

## Usage
התחביר הבסיסי של הפקודה הוא:

```bash
dig [אפשרויות] [ארגומנטים]
```

## Common Options
- `@server` - מציין את שרת ה-DNS שבו תתבצע השאילתה.
- `-t type` - קובע את סוג הרשומה שיש לחפש (למשל, A, AAAA, MX).
- `+short` - מציג תוצאה מקוצרת, רק את המידע החשוב.
- `+trace` - עוקב אחרי השאילתה בכל שלביה, מהשרתים העליונים ועד לשרתים המקומיים.

## Common Examples
להלן מספר דוגמאות שימושיות לפקודת `dig`:

1. קבלת כתובת IP של דומיין:
   ```bash
   dig example.com
   ```

2. קבלת רשומת MX עבור דומיין:
   ```bash
   dig -t MX example.com
   ```

3. שימוש בשרת DNS ספציפי:
   ```bash
   dig @8.8.8.8 example.com
   ```

4. קבלת תוצאה מקוצרת:
   ```bash
   dig +short example.com
   ```

5. מעקב אחרי השאילתה:
   ```bash
   dig +trace example.com
   ```

## Tips
- השתמש באפשרות `+short` כדי לקבל תוצאות מהירות וברורות.
- אם אתה מתמודד עם בעיות DNS, השתמש באפשרות `+trace` כדי להבין היכן הבעיה.
- כדאי לבדוק את הרשומות השונות (A, AAAA, CNAME, MX) כדי לקבל תמונה מלאה על הדומיין.