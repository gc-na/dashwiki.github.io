# [دبیان] Debian Almquist Shell (dash) cp استفاده: کپی فایل‌ها و دایرکتوری‌ها

## Overview
دستور `cp` در شل دبیان آلکویست (dash) برای کپی کردن فایل‌ها و دایرکتوری‌ها استفاده می‌شود. این دستور به شما امکان می‌دهد تا فایل‌ها را از یک مکان به مکان دیگر منتقل کنید یا از آن‌ها نسخه پشتیبان تهیه کنید.

## Usage
سینتکس پایه دستور `cp` به صورت زیر است:

```bash
cp [options] [arguments]
```

## Common Options
- `-r`: کپی کردن دایرکتوری‌ها به صورت بازگشتی.
- `-i`: قبل از کپی کردن، از کاربر تأیید می‌خواهد.
- `-u`: فقط فایل‌هایی که جدیدتر از نسخه موجود هستند را کپی می‌کند.
- `-v`: نمایش جزئیات کپی کردن فایل‌ها.

## Common Examples
### کپی یک فایل
برای کپی کردن یک فایل به مکان جدید:

```bash
cp file.txt /path/to/destination/
```

### کپی یک دایرکتوری به صورت بازگشتی
برای کپی کردن یک دایرکتوری و محتوای آن:

```bash
cp -r /path/to/source_directory /path/to/destination_directory/
```

### کپی با تأیید
برای کپی کردن فایل‌ها با درخواست تأیید:

```bash
cp -i file.txt /path/to/destination/
```

### کپی فقط فایل‌های جدیدتر
برای کپی کردن فقط فایل‌هایی که جدیدتر از نسخه موجود هستند:

```bash
cp -u file.txt /path/to/destination/
```

## Tips
- همیشه از گزینه `-i` استفاده کنید تا از کپی کردن ناخواسته فایل‌ها جلوگیری شود.
- برای کپی کردن دایرکتوری‌ها، حتماً از گزینه `-r` استفاده کنید.
- می‌توانید از گزینه `-v` برای مشاهده جزئیات کپی کردن استفاده کنید تا مطمئن شوید که همه چیز به درستی انجام می‌شود.