# ورد الاستغفار - مشروع أندرويد

## الطريقة 1: GitHub (بدون تثبيت أي برنامج)
1. أنشئ مستودعًا جديدًا على github.com وارفع كل محتويات هذا المجلد إليه (بما فيها المجلد المخفي .github).
2. افتح تبويب Actions ثم Build APK وانتظر نحو 5 دقائق حتى يكتمل البناء.
3. من صفحة التشغيل نزّل الملف istighfar-apk في الأسفل، وفك ضغطه لتحصل على app-debug.apk.
4. انقله إلى هاتفك وثبّته (فعّل «التثبيت من مصادر غير معروفة» إن طُلب).

## الطريقة 2: Android Studio
1. ثبّت Node.js 20 و Android Studio.
2. في هذا المجلد نفّذ:
   npm install
   npx cap add android
3. أضف داخل android/app/src/main/AndroidManifest.xml قبل </manifest>:
   <uses-permission android:name="android.permission.POST_NOTIFICATIONS"/>
   <uses-permission android:name="android.permission.SCHEDULE_EXACT_ALARM"/>
   <uses-permission android:name="android.permission.RECEIVE_BOOT_COMPLETED"/>
4. نفّذ npx cap sync android ثم npx cap open android، ومن Android Studio: Build ثم Build APK(s).

بعد التثبيت افتح التطبيق، واضبط الأوقات في قسم «التذكيرات اليومية»، واضغط «حفظ التذكيرات» ووافق على إذن الإشعارات.
