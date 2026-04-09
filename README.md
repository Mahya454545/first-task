# 🚀 ForFX — Sales & Support Dashboard
### گزارش کامل مراحل آموزش و پیاده‌سازی

> **برنامه آموزشی داخلی Opofinance** | تهیه‌شده توسط: Sara Ahmadi | تاریخ: ۲۰ فروردین ۱۴۰۵

---

## 📋 فهرست مطالب

1. [مفاهیم پایه](#-مرحله-۱--آشنایی-با-مفاهیم-پایه)
2. [نصب ابزارها](#-مرحله-۲--نصب-ابزارهای-لازم)
3. [اکستنشن‌های VS Code](#-اکستنشن-های-vs-code)
4. [ساخت اکانت‌ها](#-مرحله-۳--ساخت-اکانت-ها)
5. [نصب Claude Code](#-مرحله-۴--نصب-و-راه-اندازی-claude-code)
6. [دیتای فیک](#-ساخت-دیتای-فیک)
7. [ساخت داشبورد](#-ساخت-داشبورد)
8. [انتشار روی GitHub Pages](#-مرحله-۵--انتشار-روی-github-pages)

---

## 🧠 مرحله ۱ — آشنایی با مفاهیم پایه

قبل از شروع کار، با مفاهیم زیر آشنا شدیم:

| مفهوم | توضیح ساده |
|---|---|
| **HTML** | اسکلت صفحه وب — مشخص می‌کنه چه چیزی روی صفحه هست |
| **CSS** | ظاهر و رنگ‌آمیزی — مشخص می‌کنه هر چیز چه شکلی داره |
| **JavaScript** | رفتار و پویایی — مشخص می‌کنه هر چیز چیکار می‌کنه |
| **Terminal** | پنجره‌ای که با تایپ دستور به کامپیوتر فرمان می‌دیم |
| **Git** | ابزار همگام‌سازی کد بین کامپیوتر و GitHub |
| **GitHub** | سایت نگهداری و اشتراک‌گذاری کدها |
| **Node.js** | زیرساخت لازم برای اجرای Claude Code |
| **Claude Code** | هوش مصنوعی که با توضیح ساده، کد می‌نویسه |

---

## 🛠 مرحله ۲ — نصب ابزارهای لازم

### سیستم عامل: macOS

#### نصب Node.js
```bash
# دانلود از سایت رسمی
https://nodejs.org  →  نسخه LTS را دانلود کن

# تأیید نصب
node --version
# خروجی مورد انتظار: v22.x.x
```

#### نصب Git
```bash
# چک کردن نصب بودن
git --version
# خروجی مورد انتظار: git version 2.x.x

# تنظیم اطلاعات کاربری
git config --global user.name "نام شما"
git config --global user.email "ایمیل شما"
```

#### نصب VS Code
```
دانلود از: https://code.visualstudio.com
→ فایل ZIP را باز کنید
→ به Applications بکشید و بندازید
```

#### نصب GitHub Desktop
```
دانلود از: https://desktop.github.com
→ فایل ZIP را باز کنید
→ به Applications بکشید و بندازید
```

---

## 🔌 اکستنشن‌های VS Code

این اکستنشن‌ها برای پروژه نصب شدن:

| اکستنشن | کاربرد |
|---|---|
| **Live Server** | نمایش زنده داشبورد در مرورگر |
| **Prettier** | مرتب‌سازی اتوماتیک کد |
| **HTML CSS Support** | راهنمایی در کدنویسی HTML و CSS |
| **JavaScript ES6 Snippets** | پیشنهاد کدهای JS |
| **GitLens** | مدیریت Git داخل VS Code |
| **Material Icon Theme** | آیکون‌های رنگی برای فایل‌ها |

---

## 👤 مرحله ۳ — ساخت اکانت‌ها

### GitHub (رایگان)
```
سایت: https://github.com
→ Sign up
→ ایمیل + رمز + نام کاربری
→ کد تأیید ایمیل را وارد کن
→ GitHub Desktop را به اکانت وصل کن
```

### Claude.ai (پلن Pro — ماهی ۲۰ دلار)
```
سایت: https://claude.ai
→ Sign up (با Google یا ایمیل)
→ Upgrade to Pro
→ اطلاعات کارت بین‌المللی را وارد کن
```

> ⚠️ **نکته:** کارت بانکی ایرانی کار نمی‌کنه. باید از Visa یا Mastercard بین‌المللی استفاده کرد.

---

## 🤖 مرحله ۴ — نصب و راه‌اندازی Claude Code

```bash
# نصب Claude Code
npm install -g @anthropic-ai/claude-code

# تأیید نصب
claude --version

# اجرا و لاگین
claude
# مرورگر باز می‌شه → Authorize را بزن → برگرد به ترمینال
```

بعد از لاگین موفق:
```
✓ Logged in as sara@gmail.com
Welcome to Claude Code!
>
```

---

## 📊 ساخت دیتای فیک

برای داشبورد، یک فایل داده با **۱۰۰ ردیف** و **۲۵ ستون** ساخته شد.

### ستون‌های اصلی (از ساختار اولیه)
`date` · `Email` · `billing_phone` · `Lname` · `Country` · `Plan-Tags` · `Purchase Plans` · `Amount-USD` · `UTM Campaign` · `UTM Medium` · `UTM Source` · `Status`

### ستون‌های اضافه‌شده برای Sales و Support
`Fname` · `Account Type` · `Platform` · `Leverage` · `Deposit Count` · `Total Deposits (USD)` · `Profit/Loss (USD)` · `Ticket Category` · `Ticket Status` · `Response Time (hrs)` · `Assigned Agent` · `Last Login Date` · `Trades Count`

### فایل‌ها
- `client_data_fake.xlsx` — فایل Excel با فرمت‌بندی رنگی
- `client_data_fake.csv` — همان داده به فرمت CSV

---

## 🎨 ساخت داشبورد

### مشخصات فنی
- **زبان:** HTML + CSS + JavaScript (بدون Backend)
- **طراحی:** Material Design 3
- **چارت‌ها:** Chart.js
- **تم:** بنفش با Dark Mode

### صفحات (Routes)

| صفحه | محتوا |
|---|---|
| 📊 Dashboard | نمای کلی — KPI ها و چارت‌های اصلی |
| 💰 Sales Analytics | روند درآمد، انواع حساب، پلن‌ها |
| 👥 Clients | لیست کلاینت‌ها با سرچ و فیلتر |
| 🌍 Geography | توزیع جغرافیایی کلاینت‌ها |
| 🎫 Tickets | تیکت‌های پشتیبانی و live feed |
| 🧑‍💼 Agents | پرفورمنس و حجم کار هر اجنت |
| 📣 Marketing | منابع UTM و کمپین‌ها |
| 📋 Reports | خلاصه KPI ها و وضعیت targets |

### ویژگی‌های اصلی
- ✅ Dark Mode با toggle
- ✅ Responsive برای موبایل، تبلت و دسکتاپ
- ✅ Hash-based routing (هر صفحه URL جداگانه دارد)
- ✅ جدول کلاینت با قابلیت سرچ و فیلتر
- ✅ Live ticket feed
- ✅ جدول پرفورمنس اجنت‌ها با ستاره‌بندی
- ✅ رنگ‌بندی وضعیت تیکت‌ها

---

## 🚀 مرحله ۵ — انتشار روی GitHub Pages

### ساخت Repository
```
github.com → + → New repository
نام: my-dashboard
نوع: Public
✅ Add a README file
→ Create repository
```

### آپلود فایل
```
Add file → Upload files
→ فایل index.html را آپلود کن
→ Commit message: "Add ForFX dashboard"
→ Commit changes
```

> ⚠️ **نکته مهم:** فایل باید حتماً `index.html` نام داشته باشد، نه `dashboard.html`

### فعال‌سازی GitHub Pages
```
Settings → Pages
Branch: main | / (root)
→ Save
→ ۲ دقیقه صبر کن
```

### لینک نهایی
```
https://mahya454545.github.io/my-dashboard/
```

---

## 📸 خروجی نهایی

داشبورد شامل این داده‌هاست:

- **۱۰۰ کلاینت** از ۲۰ کشور
- **۸ اجنت پشتیبانی**
- **۱۲ ماه** داده تاریخی
- **۹ نمودار** تعاملی
- **۸ صفحه** مجزا با routing

---

## 💬 یک جمله درباره تجربه

> *"با کمک هوش مصنوعی، یک داشبورد حرفه‌ای ساختم بدون اینکه حتی یک خط کد بلد باشم."*

---

## 🔗 لینک‌های مفید

| منبع | لینک |
|---|---|
| GitHub Repository | https://github.com/mahya454545/my-dashboard |
| داشبورد آنلاین | https://mahya454545.github.io/my-dashboard/ |
| Claude.ai | https://claude.ai |
| GitHub Desktop | https://desktop.github.com |
| VS Code | https://code.visualstudio.com |

---

*ساخته‌شده در برنامه آموزش داخلی AI — Opofinance 2026* 🚀
