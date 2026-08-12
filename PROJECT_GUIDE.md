# دليل مشروع Engaz Website

آخر مراجعة: 2026-08-12

## 1. الهدف

الموقع التعريفي العام لشركة ENGAZ. هذا المستودع يحتوي الموقع الرئيسي فقط؛ كل Demo موجود في مستودع ونطاق مستقل.

## 2. النسخة الرسمية

- المستودع: `SheedoZ/Engaz_Website`
- الفرع الرسمي: `main`
- المسار المحلي المنظم: `D:\Projects\Engaz-Website`
- مجلدات `engaz-sites` و`website` القديمة داخل أرشيف الشركة ليست مصدر الإنتاج الحالي.

## 3. تركيب الملفات

- `index.html`: الموقع الكامل.
- `social-preview.png`: صورة المشاركة على الشبكات.
- `CNAME`: النطاق `engaz.premiumpower-eg.com`.
- `.nojekyll`: نشر الملفات كما هي على GitHub Pages.
- `.github/workflows/validate.yml`: فحص الملفات والروابط والأمان ونهايات الأسطر.
- `README.md`: قواعد النشر والفصل عن الـdemos.
- `PROJECT_GUIDE.md`: هذا الدليل.

## 4. التشغيل والإنتاج

الموقع Static على GitHub Pages من جذر `main`، والنطاق هو `https://engaz.premiumpower-eg.com/`. لا توجد قاعدة بيانات أو أسرار تشغيل داخل المشروع.

## 5. طريقة التعديل الآمنة

1. حدّث `main` وأنشئ فرعًا جديدًا.
2. عدّل `index.html` أو `social-preview.png` فقط حسب الحاجة.
3. لا تعِد مجلد `demos/` أو `.openai/` إلى هذا المستودع.
4. نفّذ الفحص المحلي وراجع الصفحة في المتصفح.
5. افتح Pull Request وانتظر نجاح `Validate website` قبل الدمج.

## 6. اختبار صغير

```powershell
git diff --check
```

ثم افتح `index.html` محليًا وتأكد من الهيدر، الأقسام، نموذج التواصل وروابط الـClinic/Lab/Automation.

## 7. النشر والرجوع

الدمج في `main` ينشر عبر GitHub Pages تلقائيًا. بعده راجع HTTPS والنطاق. للرجوع استخدم `git revert` للـcommit الأخير ثم ادمج التراجع وانتظر Pages.

## 8. حدود البيانات والأمان

- لا تضف credentials أو ملفات بيئة أو exports أو uploads أو بيانات عملاء.
- بيانات الـdemos يجب أن تظل صناعية، وفي مستودعاتها المنفصلة.
- لا تغيّر `CNAME` إلا بالتنسيق مع DNS وإعدادات Pages.
