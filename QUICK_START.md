# 🚀 البدء السريع - GW

## الخطوات (5 دقائق)

### 1️⃣ ثبّت Node.js
حمّل من: https://nodejs.org/ (اختر LTS)

### 2️⃣ افتح Terminal/CMD في مجلد التطبيق

**ماك:**
```bash
cd ~/Desktop/gw-app   # أو المسار اللي حطيت فيه المجلد
```

**ويندوز:**
```cmd
cd C:\Users\YOUR_NAME\Desktop\gw-app
```

### 3️⃣ ثبّت الاعتماديات (مرة واحدة فقط)
```bash
npm install
```
سيستغرق دقيقتين تقريباً وينزل ملفات Electron.

### 4️⃣ شغّل التطبيق
```bash
npm start
```

🎉 التطبيق راح يفتح بنافذة سطح مكتب حقيقية!

---

## بناء نسخة قابلة للتثبيت

بعد ما تجرب التطبيق وتتأكد إنه شغّال:

### للماك:
```bash
npm run build:mac
```
بعد الانتهاء، تجد ملف `.dmg` في مجلد `dist/`. افتحه واسحب التطبيق لمجلد Applications.

### للويندوز:
```bash
npm run build:win
```
بعد الانتهاء، تجد ملف `.exe` في مجلد `dist/`. شغّله ليثبّت التطبيق.

---

## استكشاف الأخطاء

**خطأ: `npm: command not found`**
- لم تثبّت Node.js. حمّله من nodejs.org.

**خطأ في `npm install`:**
- جرّب: `npm install --force`
- أو احذف `node_modules/` و `package-lock.json` وأعد المحاولة.

**التطبيق ما يفتح:**
- جرّب: `npm run dev` لتشاهد الأخطاء في console.

**خطأ في البناء على ماك:**
- قد تحتاج Xcode Command Line Tools: `xcode-select --install`

**خطأ في البناء على ويندوز:**
- شغّل CMD أو PowerShell **كمسؤول (Run as Administrator)**.

---

## أيقونة التطبيق

ملف `build/icon.svg` فيه أيقونة بسيطة. لاستخدامها:

1. افتح: https://cloudconvert.com
2. حوّل `icon.svg` إلى:
   - `icon.icns` (للماك) - حجم 1024x1024
   - `icon.ico` (للويندوز) - حجم 256x256
   - `icon.png` (للينكس) - حجم 512x512
3. ضع الملفات في مجلد `build/`

أو استخدم أداة مثل: https://www.electron.build/icons

---

## نصائح

- 🔥 التطبيق يحفظ بيانات Xtream تلقائياً، فلا تحتاج تدخلها كل مرة
- 🔥 المفضلة محفوظة محلياً ولن تضيع
- 🔥 يدعم الشاشة الكاملة (View > Toggle Fullscreen أو F11)
- 🔥 يفتح روابط HTTP بدون مشاكل (بعكس المتصفح)
