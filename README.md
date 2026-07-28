<div align="center">

# 📖 TriLex

**واژه‌نامهٔ سه‌زبانهٔ آلمانی – انگلیسی – فارسی، بر پایهٔ کتاب Starten wir A1**

[![Live Demo](https://img.shields.io/badge/demo-online-3F6B4F?style=flat-square)](https://hajmehrad.github.io/TriLex/)
[![Release](https://img.shields.io/badge/release-v1.1-B4802E?style=flat-square)](https://github.com/Hajmehrad/TriLex/releases)
[![License](https://img.shields.io/badge/license-MIT-1F2A3C?style=flat-square)](LICENSE)
[![Made with](https://img.shields.io/badge/made%20with-HTML%20%7C%20CSS%20%7C%20JS-7A3030?style=flat-square)]()

</div>

---

## دربارهٔ پروژه

**TriLex** یک واژه‌نامهٔ تعاملی برای زبان‌آموزان فارسی‌زبانِ آلمانی است که واژگان کتاب *Starten wir A1* را به‌صورت درس‌به‌درس (۱۲ درس)، همراه با ترجمهٔ انگلیسی و فارسی، توضیح، مثال کاربردی و صرف کامل فعل در اختیار کاربر قرار می‌دهد. نام برنامه از ترکیب **Tri** (سه‌زبانه: آلمانی، انگلیسی، فارسی) و **Lex** (Lexicon) گرفته شده است.

این پروژه به‌صورت یک وب‌اپلیکیشن تک‌فایلی (Single-file HTML App) ساخته شده و روی **GitHub Pages** میزبانی می‌شود، به همین دلیل بدون نیاز به نصب یا سرور، مستقیماً در مرورگر قابل استفاده است.

🔗 **دسترسی آنلاین:** [hajmehrad.github.io/TriLex](https://hajmehrad.github.io/TriLex/)

---

## ✨ امکانات

- 📚 **۱۲ درس کامل** مطابق فصل‌بندی کتاب Starten wir A1 (از «Super!» تا «Beruf und Leben»)
- 🔍 **جست‌وجوی زنده** بین واژهٔ آلمانی، معادل انگلیسی، معادل فارسی، توضیح و نقش دستوری، با نادیده‌گرفتن نویسه‌های ویژهٔ آلمانی (ä/ö/ü/ß) در جست‌وجو
- 🏷️ **فیلتر بر اساس نقش دستوری (Part of Speech)** — اسم، فعل، فعل کمکی، صفت، قید، ضمیر، حرف‌اضافه، حرف‌ربط، عدد، اصطلاح و…، به‌همراه شمارش تعداد واژگان هر دسته
- 🗂️ **تب‌های درس‌به‌درس** با نمایش تعداد واژگان هر درس و نشانگر (●) برای درس‌هایی که ترجمه‌شان کامل شده است
- 🪟 **پنجرهٔ جزئیات واژه (Modal)** شامل:
  - توضیح کامل کلمه (تعریف)
  - مثال‌های کاربردی سه‌زبانه (آلمانی + انگلیسی + فارسی)
  - جدول کامل صرف فعل برای همهٔ ضمایر (ich, du, er/sie/es, wir, ihr, sie/Sie) به‌همراه مثال جداگانه برای هر صیغه
  - فرم Perfekt فعل
- 🕘 **تاریخچهٔ جست‌وجوی شخصی** که به‌صورت محلی برای هر کاربر ذخیره می‌شود، با امکان کلیک مجدد روی عبارت‌های قبلی و پاک‌کردن کامل تاریخچه
- 🎨 **طراحی اختصاصی با تم کاغذی/آنتیک** با فونت‌های Vazirmatn (فارسی)، Fraunces (سرلوحه‌ها) و Inter (متن لاتین)
- ↔️ **پشتیبانی کامل از RTL** برای بخش فارسی، در کنار نمایش صحیح LTR برای بخش‌های آلمانی و انگلیسی در همان کارت‌ها
- 📱 **طراحی واکنش‌گرا (Responsive)** مناسب موبایل، تبلت و دسکتاپ

---

## 🖼️ ساختار پروژه

```
TriLex/
├── index.html      # کل اپلیکیشن (HTML + CSS + JavaScript) در یک فایل
├── README.md        # این فایل
└── LICENSE           # لایسنس پروژه
```

فعلاً کل منطق برنامه — رابط کاربری، استایل و داده‌های واژگان — در یک فایل واحد `index.html` قرار دارد که هم توسعه و هم استقرار (Deploy) روی GitHub Pages را بسیار ساده می‌کند.

---

## 🚀 شروع سریع

### استفادهٔ آنلاین (پیشنهادی)

کافیست آدرس زیر را باز کنید:

👉 **[hajmehrad.github.io/TriLex](https://hajmehrad.github.io/TriLex/)**

### اجرای محلی

```bash
git clone https://github.com/Hajmehrad/TriLex.git
cd TriLex
```

سپس فایل `index.html` را مستقیماً در هر مرورگری باز کنید — نیازی به نصب هیچ وابستگی، پکیج یا سرور نیست.

---

## 🧱 ساختار داده‌های واژگان

هر واژه در قالب یک شیء JavaScript با فیلدهای زیر تعریف می‌شود:

```json
{
  "de": "Haus",
  "artikel": "das",
  "plural": "Häuser",
  "pos": "Nomen",
  "en": "house",
  "fa": "خانه",
  "def": "توضیح کوتاه دربارهٔ کلمه",
  "example": {
    "de": "Ich wohne in einem Haus.",
    "en": "I live in a house.",
    "fa": "من در یک خانه زندگی می‌کنم."
  },
  "conj": {
    "ich":  { "form": "wohne",  "de": "...", "en": "...", "fa": "..." },
    "du":   { "form": "wohnst", "de": "...", "en": "...", "fa": "..." },
    "er":   { "form": "wohnt",  "de": "...", "en": "...", "fa": "..." },
    "wir":  { "form": "wohnen", "de": "...", "en": "...", "fa": "..." },
    "ihr":  { "form": "wohnt",  "de": "...", "en": "...", "fa": "..." },
    "sie":  { "form": "wohnen", "de": "...", "en": "...", "fa": "..." },
    "perfekt": "hat gewohnt"
  }
}
```

واژگان بر اساس شمارهٔ درس (`"1"` تا `"12"`) در یک شیء اصلی به نام `DATA` دسته‌بندی می‌شوند و در آرایه‌ای به نام `TRANSLATED_LEKTIONS` مشخص می‌شود کدام درس‌ها ترجمهٔ کاملشان انجام شده است.

### فهرست درس‌ها (Lektionen)

| # | عنوان درس |
|---|---|
| 1 | Super! |
| 2 | Menschen |
| 3 | Essen und Trinken |
| 4 | Mein Leben |
| 5 | Freizeit |
| 6 | Meine Stadt, meine Wohnung |
| 7 | Wie, wo und wann? |
| 8 | Unterwegs |
| 9 | Unter Freunden |
| 10 | Ich war noch nie ... |
| 11 | Bist du fit? |
| 12 | Beruf und Leben |

---

## 🛠️ فناوری‌های استفاده‌شده

| فناوری | کاربرد |
|---|---|
| **HTML5 / CSS3** | چیدمان، طراحی و تم بصری |
| **Vanilla JavaScript** | منطق جست‌وجو، فیلتر، رندر کارت‌ها و مدیریت پنجرهٔ جزئیات |
| **Google Fonts** | Vazirmatn (فارسی)، Fraunces (سرلوحه‌ها)، Inter (متن‌های لاتین) |
| **Storage API** | ذخیرهٔ محلی و شخصی تاریخچهٔ جست‌وجوی هر کاربر |
| **GitHub Pages** | میزبانی و استقرار نسخهٔ آنلاین |

---

## 🗺️ نقشهٔ راه (Roadmap)

- [ ] تکمیل ترجمهٔ فارسی/انگلیسی درس‌های باقی‌مانده
- [ ] افزودن تلفظ صوتی کلمات (Text-to-Speech)
- [ ] افزودن حالت تمرین/کوییز و فلش‌کارت
- [ ] پشتیبانی از سطوح A2، B1 و بالاتر
- [ ] حالت آفلاین کامل (PWA)
- [ ] امکان بوکمارک‌کردن واژگان دلخواه

پیشنهاد یا درخواست ویژگی جدید دارید؟ از بخش [Issues](https://github.com/Hajmehrad/TriLex/issues) مطرح کنید.

---

## 🤝 مشارکت (Contributing)

از هرگونه مشارکت استقبال می‌شود!

1. ریپازیتوری را Fork کنید
2. یک برنچ جدید بسازید:
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. تغییرات خود را Commit کنید:
   ```bash
   git commit -m "افزودن ویژگی جدید"
   ```
4. برنچ را Push کنید:
   ```bash
   git push origin feature/amazing-feature
   ```
5. یک Pull Request باز کنید

---

## 📦 نسخه‌ها (Releases)

آخرین نسخهٔ منتشرشده: **TriLex v1.1**
برای مشاهدهٔ تاریخچهٔ کامل نسخه‌ها به بخش [Releases](https://github.com/Hajmehrad/TriLex/releases) مراجعه کنید.

---

## 📄 لایسنس

این پروژه تحت لایسنس [MIT](LICENSE) منتشر می‌شود.

---

## 👤 نویسنده

**Hajmehrad**
GitHub: [@Hajmehrad](https://github.com/Hajmehrad)

ساخته‌شده با ❤️ برای زبان‌آموزان فارسی‌زبانِ آلمانی — اگر این پروژه برایتان مفید بود، فراموش نکنید یک ⭐ به ریپازیتوری بدهید!
