# AJ Store Updates

هذا المستودع العام هو متجر تحديثات تطبيق AJ Store. التطبيق يقرأ `latest.json` مباشرة من GitHub عند فتحه، ويمكن للمستخدم طلب الفحص يدوياً من صفحة «حسابي».

## ملف التحديث latest.json

- `enabled`: تشغيل أو إيقاف التحديثات.
- `versionName`: رقم الإصدار الظاهر للمستخدم.
- `versionCode`: رقم بناء Android ويجب أن يكون أكبر من الإصدار المثبت.
- `apkUrl`: رابط تنزيل APK من GitHub Release في هذا المستودع.
- `releaseNotes`: وصف التغييرات.

## نشر تحديث جديد

1. ارفع APK إلى GitHub Release في هذا المستودع باسم `aj-store.apk`.
2. ضع رابط التنزيل المباشر في `apkUrl`، بالشكل:
   `https://github.com/ahmadjalladjo1984-code/aj-store-updates/releases/download/TAG/aj-store.apk`
3. حدّث `versionName` و`versionCode` و`releaseNotes` في `latest.json` بعد التأكد من أن رابط APK يعمل.
4. ارفع `versionCode` دائماً ولا تعِد استخدام رقم بناء سابق.

## أمان وتوافق Android

- كل APK جديد يجب أن يستخدم **مفتاح التوقيع نفسه** المستخدم في النسخة المثبتة؛ وإلا سيرفض Android التحديث فوق التطبيق الحالي.
- لا ترفع ملف keystore أو كلمات المرور إلى هذا المستودع العام.
- التثبيت ليس صامتاً؛ Android يعرض شاشة التثبيت ويطلب موافقة المستخدم، وقد يطلب السماح بالتثبيت من هذا المصدر.
- لا تضع رابط APK قبل التأكد من أن الملف منشور ومتاح للتنزيل.
