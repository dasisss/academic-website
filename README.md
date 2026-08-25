# موقع أكاديمي + Decap CMS

هذا المشروع يجمع Quarto مع Decap CMS. الموقع العام يُبنى من ملفات QMD، ولوحة الإدارة موجودة في `/admin/`.

## مهم قبل أول تشغيل

ملف `admin/config.yml` مضبوط على Netlify Identity + Git Gateway. لذلك أسهل بنية هي ربط هذا المستودع بـ Netlify وتشغيل Identity وGit Gateway، ثم دعوة بريدك كمدير. هذا الأسلوب يسمح لك بالتعديل والرفع من لوحة CMS دون منح المستخدمين صلاحية GitHub مباشرة.

## نشر الموقع

### خيار 1: Netlify (الموصى به مع CMS)

1. ارفع المشروع إلى GitHub.
2. في Netlify اختر Add new project → Import an existing project → GitHub.
3. Build command: `quarto render`
4. Publish directory: `_site`
5. بعد النشر فعّل Identity ثم Git Gateway.
6. اجعل التسجيل Invite only، ثم ادعُ بريدك.
7. افتح `https://YOUR-SITE.netlify.app/admin/`.

### خيار 2: GitHub Pages

الموقع العام يمكن نشره عبر GitHub Actions، لكن إعداد المصادقة الخاص بـ CMS يظل أسهل مع Netlify. لا تضع رموز GitHub السرية داخل `config.yml`.

## ما يمكنك تعديله من CMS

- الصفحة الرئيسية والسيرة والبحث والتدريس والموارد والاتصال.
- إضافة/تعديل/حذف المنشورات.
- رفع PDF.
- رفع عروض PowerPoint أو ملفات أخرى.
- إضافة محاضرات ومواد تعليمية.
- إضافة موارد وروابط.

## بعد الحفظ

Decap ينشئ commit في مستودع Git، ثم يعيد Netlify بناء الموقع تلقائيًا.

## تخصيص الهوية

قبل النشر استبدل الاسم والرتبة والبريد والروابط الأكاديمية والبيانات غير المؤكدة.
