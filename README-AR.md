# برج الإنارة — V6 Industrial Future

مشروع React + Vite + Tailwind CSS + Framer Motion + React Three Fiber + Three.js + Lenis. تجربة عربية RTL مع شاشة تشغيل كهربائية ومصباح WebGL تفاعلي، وبحث وتصنيفات وسلة محلية.

## التشغيل المحلي

1. ثبّت Node.js إصدار 20 أو أحدث.
2. افتح مجلد المشروع في الطرفية.
3. نفّذ `npm install` ثم `npm run dev`.
4. للبناء: `npm run build`، والناتج داخل `dist/`.

## النشر على GitHub Pages

**هذا الإصدار مختلف عن V5:** لا ترفع ملفات `src` وحدها وتتوقع أن تعمل مباشرة على Pages. يجب بناؤها بواسطة GitHub Actions.

1. احفظ نسخة من مستودع V5 أو أنشئ فرعاً احتياطياً.
2. ارفع **كل محتويات هذا المجلد** إلى جذر المستودع `yaslamaliksa/burj-alenara-store` مع الحفاظ على المجلدات `src` و`public` و`.github/workflows`.
3. من Settings → Pages → Build and deployment اختر **GitHub Actions** بدلاً من Deploy from a branch.
4. من Actions راقب `Deploy V6 to GitHub Pages` حتى يظهر النجاح.
5. افتح https://yaslamaliksa.github.io/burj-alenara-store/ ثم حدث الصفحة بقوة.
6. احذف ملفات V5 القديمة من الجذر (`script.js` و`style.css` و`sw.js` و`mobile.js` و`manifest.webmanifest`) بعد التأكد من نجاح النشر، حتى لا تسبب التباساً. لا تحذف الملفات قبل الاحتفاظ بنسخة احتياطية.

### تنبيه
- `base` مضبوط على `/burj-alenara-store/`. إذا تغير اسم المستودع، حدّث `vite.config.js`.
- لا يوجد خادم دفع أو طلبات حقيقية. السلة محلية فقط، والأسعار والمنتجات تجريبية.
- صور المنتجات الحالية موروثة من V5 وتحتاج لاحقاً إلى استبدالها بصور فوتوغرافية أصلية مرخصة.
- لا توجد حركة X-ray/Shader حقيقية لبطاقات المنتجات؛ يوجد تأثير لمعان وتكبير خفيف. المصباح ثلاثي الأبعاد حقيقي باستخدام WebGL ولكنه نموذج هندسي stylized وليس تصويراً فوتوغرافياً.
- أداء 60fps هدف تصميمي وليس ضماناً لكل جهاز.
- لم يتوفر اتصال npm في بيئة إنشاء الحزمة، لذلك لم أتمكن من تنفيذ `npm install` أو اختبار build. ستنفذ GitHub Actions التثبيت والبناء عند النشر.
