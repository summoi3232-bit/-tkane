# مسار الإتقان

تطبيق ويب تقدمي (PWA) لتصنيف السور وتوزيع الورد اليومي وتثبيت الحفظ عبر التكرار المتباعد.

## الملفات
- `index.html` — التطبيق الكامل (واجهة + منطق)
- `manifest.json` — بيانات التطبيق كـ PWA
- `service-worker.js` — تشغيل بدون اتصال بالإنترنت (offline-first)
- `icons/` — أيقونات التطبيق (192px, 512px)

## النشر على GitHub Pages
```bash
git init
git add .
git commit -m "مسار الإتقان: نسخة أولى"
git branch -M main
git remote add origin <رابط-المستودع>
git push -u origin main
```
ثم فعّل GitHub Pages من إعدادات المستودع (Settings → Pages → Deploy from branch → main).

## النشر على Netlify
اسحب مجلد المشروع بالكامل إلى [app.netlify.com/drop](https://app.netlify.com/drop)، أو اربط مستودع GitHub مباشرة من لوحة Netlify.

## توليد APK لأندرويد
استخدم [PWABuilder](https://www.pwabuilder.com):
1. انشر التطبيق أولاً (GitHub Pages أو Netlify) للحصول على رابط عام.
2. أدخل الرابط في PWABuilder.
3. اختر Android package → قم بتنزيل الـ APK الموقّع.

## النسخ الاحتياطي للبيانات
البيانات محفوظة محليًا في المتصفح (`localStorage`). يوفر التطبيق زرّي تصدير/استيراد (⭳ / ⭱) أعلى الشاشة لحفظ نسخة JSON واستعادتها عند تغيير الجهاز أو المتصفح.
