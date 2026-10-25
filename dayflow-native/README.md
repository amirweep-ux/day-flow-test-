# Day Flow — ساخت اپ اندروید (APK)

این پوشه نسخه‌ی «اپ واقعی» است: بدون مرورگر باز می‌شود، همه‌چیز آفلاین کار می‌کند و یادآورها حتی با بسته‌بودن برنامه می‌رسند.

## پیش‌نیاز
- Node.js (نسخه‌ی LTS) و Android Studio روی کامپیوتر
- اینترنت فقط برای نصب بسته‌ها

## مراحل
1. در پوشه‌ی پروژه: `npm install`
2. `npm run build`  ← Tailwind، فونت و supabase را داخل `www` جاسازی می‌کند
3. فقط بار اول: `npx cap add android`
4. آیکن: `npx @capacitor/assets generate --android`
5. `npx cap sync` و بعد `npx cap open android`
6. در Android Studio: Build ← Build Bundle(s)/APK(s) ← Build APK(s)

## بعد از نصب روی گوشی
- در تنظیمات برنامه، «یادآورها» را روشن کن و اجازه‌ی اعلان را بده.
- اندروید ۱۲ به بالا: اجازه‌ی «Alarms & reminders» را بده و برای Day Flow «بهینه‌سازی باتری» را خاموش کن (در برخی گوشی‌ها مثل شیائومی و سامسونگ لازم است).

نکته: این پوشه روی کامپیوتر خودت ساخته می‌شود؛ ساخت APK به اینترنت و Android Studio نیاز دارد.

## ساخت APK بدون Android Studio (با GitHub، رایگان)
1. در github.com یک حساب بساز و یک مخزن (Repository) جدید باز کن (می‌تواند خصوصی باشد).
2. محتوای همین پوشه را (از جمله پوشه‌ی `.github`) داخل مخزن آپلود کن: Add file ← Upload files.
3. به تب Actions برو، «Build Day Flow APK» را انتخاب کن و Run workflow را بزن. حدود ۱۰ دقیقه صبر کن.
4. در پایین صفحه‌ی همان اجرا، فایل `dayflow-apk` را دانلود کن؛ داخلش `app-debug.apk` است.
5. APK را روی گوشی نصب کن (اجازه‌ی «نصب از منبع ناشناس» لازم است).
