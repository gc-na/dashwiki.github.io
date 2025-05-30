# [دبیان] Debian Almquist Shell (dash) expr معادل استفاده: [محاسبات ریاضی و ارزیابی عبارات]

## Overview
دستور `expr` در شل دبیان آلکویست (dash) برای ارزیابی عبارات و انجام محاسبات ریاضی استفاده می‌شود. این دستور می‌تواند برای انجام عملیات‌های ساده مانند جمع، تفریق، ضرب و تقسیم به کار رود.

## Usage
سینتکس پایه دستور `expr` به صورت زیر است:

```sh
expr [options] [arguments]
```

## Common Options
- `+` : جمع دو عدد.
- `-` : تفریق دو عدد.
- `*` : ضرب دو عدد. (برای استفاده از این علامت باید آن را در کوتیشن قرار دهید.)
- `/` : تقسیم دو عدد.
- `%` : باقی‌مانده تقسیم دو عدد.
- `=` : بررسی برابری دو عبارت.

## Common Examples
در اینجا چند مثال عملی از استفاده از دستور `expr` آورده شده است:

### جمع دو عدد
```sh
expr 5 + 3
```
خروجی: `8`

### تفریق دو عدد
```sh
expr 10 - 4
```
خروجی: `6`

### ضرب دو عدد
```sh
expr 7 \* 6
```
خروجی: `42`

### تقسیم دو عدد
```sh
expr 20 / 4
```
خروجی: `5`

### باقی‌مانده تقسیم
```sh
expr 10 % 3
```
خروجی: `1`

### بررسی برابری
```sh
expr 5 = 5
```
خروجی: `1` (به معنای درست بودن)

## Tips
- برای استفاده از علامت ضرب (`*`)، حتماً آن را با یک بک‌اسلش (`\`) فرار دهید.
- می‌توانید از `expr` در اسکریپت‌های شل برای انجام محاسبات دینامیک استفاده کنید.
- برای جلوگیری از خطاهای احتمالی، همیشه از فاصله‌های مناسب بین عبارات استفاده کنید.