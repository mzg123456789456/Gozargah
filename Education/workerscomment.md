<h1 align="center">🚀 نصب از طریق Cloudflare Workers</h1>

### مرحله 1: دانلود کد Worker  
ابتدا کد Worker را از لینک زیر دانلود کنید و به داشبورد **Cloudflare Workers** منتقل کنید. به‌جای Copy-Paste، فایل را آپلود کنید تا کار آسان‌تر باشد.  
[دانلود کد Worker](https://github.com/valid7996/Gozargah/blob/main/worker_vless/%20_worker.js)

در گوشی‌های موبایل، منوی کناری را باز کنید، روی گزینه **Upload** نگه دارید و فایل را آپلود کنید:  
<p align="center">
  <img src="https://github.com/valid7996/Gozargah/blob/main/images/imagwor/IMG_20250104_163617.jpg" alt="آپلود فایل" width="70%">
</p>

### مرحله 2: Save & Deploy  
پس از آپلود کد، می‌توانید از مقادیر پیش‌فرض استفاده کنید یا به بخش **[تنظیمات پیشرفته](#تنظیمات-پیشرفته-اختیاری)** مراجعه کنید.  
در نهایت، روی گزینه `Save and Deploy` کلیک کنید:  
<p align="center">
  <img src="https://github.com/valid7996/Gozargah/blob/main/images/imagwor/IMG_20250104_163647.jpg" alt="ذخیره و انتشار" width="70%">
</p>

---

<h1 align="center">⚙️ تنظیمات پیشرفته (اختیاری)</h1>

اگر نیاز به تغییر **UUID** یا **Proxy IP** دارید، می‌توانید این مرحله را انجام دهید. توصیه می‌شود حداقل **UUID** را تغییر دهید.

---

## تغییر UUID  
1. UUID به‌عنوان یک شناسه یکتا در لینک‌های اشتراک و کانفیگ‌ها استفاده می‌شود.  
2. تغییر آن باعث قطع دسترسی کاربران فعلی می‌شود، بنابراین باید کانفیگ‌ها را دوباره به اشتراک بگذارید.  

### مراحل تغییر UUID:
- از منوی سمت چپ، به بخش **Workers & Pages** بروید.  
- روی Worker ساخته‌شده کلیک کنید، به **Settings** بروید و گزینه **Variables and Secrets** را پیدا کنید:  
<p align="center">
  <img src="https://github.com/valid7996/Gozargah/blob/main/images/imagwor/IMG_20250104_163547.jpg" alt="تنظیمات" width="70%">
</p>

- گزینه **Add Variable** را انتخاب کنید:  
  - در فیلد اول `UUID` را وارد کنید.  
  - از [اینجا](https://www.uuidgenerator.net/) یک UUID جدید بگیرید و در فیلد دوم قرار دهید.  
<p align="center">
  <img src="https://github.com/valid7996/Gozargah/blob/main/images/imagwor/InShot_20250104_155744172.jpg" alt="افزودن UUID" width="70%">
</p>

---

## ثابت کردن Proxy IP  
اگر نیاز دارید IP ثابت برای پروکسی تعریف کنید:  
1. دوباره **Add Variable** را بزنید.  
2. در فیلد اول `PROXYIP` را بنویسید.  
3. از [Proxy IP](https://www.nslookup.io/domains/bpb.yousef.isegaro.com/dns-records/) یک IP انتخاب کنید و در فیلد دوم وارد کنید.  
<p align="center">
  <img src="https://github.com/valid7996/Gozargah/blob/main/images/imagwor/InShot_20250104_155719489.jpg" alt="افزودن Proxy IP" width="70%">
</p>

---

<h1 align="center">🌐 اتصال دامنه به Worker</h1>

برای اتصال دامنه به Worker:  
1. به داشبورد Cloudflare بروید و از بخش **Workers and Pages**، Worker خود را انتخاب کنید.  
2. به قسمت **Settings** رفته و **Domains & Routes** را باز کنید.  
3. گزینه **Add +** را بزنید و **Custom Domain** را انتخاب کنید.  
4. دامنه یا زیردامنه موردنظر (مثلاً `xyz.bv.com`) را وارد کنید.  
5. روی **Add Domain** کلیک کنید.  
6. سپس **Route** را اضافه کنید و دامنه را به شکل زیر وارد کنید:
7. حالا می‌توانید از آدرس `https://domin.com/uuid` وارد پنل شوید و تنظیمات را مشاهده کنید.

---

<h1 align="center">🔧 مقادیر پیش‌فرض</h1>

| شرح          | مقدار پیش‌فرض                      | مقدار سفارشی      |
|:-------------|:----------------------------------|:------------------|
| **UUID**     | 86c50e3a-5687-49dd-bd20-03c7f2735 | سفارشی‌شده توسط شما |
| **Proxy IP** | ts.hpc.tw                         | تنظیم‌شده توسط شما |

> **توجه:** اگر دامنه را به Worker وصل کنید، ترافیک به‌صورت **نامحدود** خواهد شد.

---

<h1 align="center">📋 نکات پایانی</h1>

- در صورت بروز هرگونه مشکل، به راهنمای کامل مراجعه کنید.  
- اتصال به برنامه‌های مختلف (مانند V2Ray، NikaNg) نیز توضیح داده‌شده است.
