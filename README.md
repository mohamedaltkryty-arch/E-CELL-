# SPIDER E-CELL

دمج واجهة Spider الأصلية مع نواة E-CELL Python داخل تطبيق Android عبر Chaquopy. لا يحتاج التطبيق إلى Termux.

## الحالة الحالية

تم تجهيز مستودع البناء وملف GitHub Actions. لا يبدأ البناء التلقائي إلا بعد إضافة ملف الحزمة المصدرية إلى جذر المستودع بالاسم الدقيق:

`SPIDER_E-CELL_GITHUB_UPLOAD_READY.zip`

الحزمة الجاهزة تحتوي على مشروع Android وملفات Python والواجهة والاختبارات وملفات البناء. بعد رفعها إلى `main`، يستخرج Workflow المصدر، يشغّل اختبارات Python، ثم يبني APK ويتحقق من اسم الحزمة.

## تنزيل APK بعد نجاح البناء

افتح **Actions**، ثم تشغيل **Build SPIDER E-CELL APK**، ثم نزّل Artifact باسم `SPIDER-E-CELL-debug-apk`.

## مواصفات التطبيق

- Application ID: `com.spider.ecell`
- Version: `1.2.1` (versionCode 121)
- minSdk 24، compileSdk/targetSdk 35
- JDK 17، Gradle 8.13، Android Gradle Plugin 8.13.2
- Chaquopy 17.2.0 وPython 3.11
- ABIs: `arm64-v8a`, `armeabi-v7a`, `x86_64`

الناتج Debug موقّع بمفتاح GitHub Actions، مناسب للاختبار والتثبيت. النشر الدائم يحتاج مفتاح توقيع خاصاً.
