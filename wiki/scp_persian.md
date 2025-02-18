# [لینوکس] Debian Almquist Shell (dash) scp استفاده: انتقال فایل‌ها به صورت امن

## Overview
دستور `scp` (Secure Copy Protocol) برای انتقال فایل‌ها و دایرکتوری‌ها به صورت امن بین سیستم‌های مختلف استفاده می‌شود. این دستور با استفاده از پروتکل SSH، امکان انتقال داده‌ها را به صورت رمزنگاری شده فراهم می‌کند.

## Usage
سینتکس پایه دستور `scp` به صورت زیر است:

```bash
scp [options] [source] [destination]
```

## Common Options
- `-r`: انتقال دایرکتوری‌ها به صورت بازگشتی.
- `-P`: مشخص کردن پورت SSH (به حروف بزرگ).
- `-i`: استفاده از کلید خصوصی برای احراز هویت.
- `-v`: فعال کردن حالت verbose برای نمایش جزئیات بیشتر.

## Common Examples
- انتقال یک فایل از سیستم محلی به سرور:
```bash
scp /path/to/local/file username@remote_host:/path/to/remote/directory
```

- انتقال یک دایرکتوری به صورت بازگشتی:
```bash
scp -r /path/to/local/directory username@remote_host:/path/to/remote/directory
```

- انتقال یک فایل از سرور به سیستم محلی:
```bash
scp username@remote_host:/path/to/remote/file /path/to/local/directory
```

- استفاده از پورت خاص برای اتصال:
```bash
scp -P 2222 /path/to/local/file username@remote_host:/path/to/remote/directory
```

## Tips
- همیشه از گزینه `-v` استفاده کنید تا در صورت بروز مشکل، جزئیات بیشتری دریافت کنید.
- برای انتقال فایل‌های بزرگ، از گزینه `-C` برای فشرده‌سازی داده‌ها استفاده کنید.
- مطمئن شوید که کلید SSH شما به درستی تنظیم شده باشد تا از ورود به سیستم بدون نیاز به رمز عبور اطمینان حاصل کنید.