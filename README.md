# Prisma & better-sqlite3 Fix
# 📦 راهنمای نصب Prisma در شرایط اینترنت ملی

> راهنمای قدم‌به‌قدم برای نصب Prisma با دانلود دستی پیش‌نیازها  


## ⚠️ پیش‌نیازهای اولیه

- ✅ Node.js 24.15.0 (فایل نصبی داخل فولدر قرار گرفته)
- ✅ Python ([دانلود پایتون](https://soft98.ir/software/programming/16260-python.html))
- ✅ Visual Studio 2022 (C++ build tools)

> اگر VS 2022 ندارید، از [این لینک](https://soft98.ir/263-Visual-Studio.html) دانلود و نصب کنید.


## 📥 مرحله 1: نصب Prisma و وابستگی‌ها

```bash
npm install prisma @types/node @types/better-sqlite3 -D
```
- این مرحله به سادگی انجام میشه و نیاز به انجام هیچ کاری نیست ✅





## 🧩 مرحله 2: نصب کلاینت و آداپتور و better-sqlite3

> ⚠️ **این سخت‌ترین بخش نصب است** - لطفاً دقیقاً طبق مراحل پیش بروید.

### 📋 قبل از اجرای دستور `npm`، این کارها را انجام دهید:



### 1️⃣ آماده کردن فایل ها
- فایل `node-v24.15.0-header.rar` را در مسیر `C:\tmp` کپی کنید
- فایل را در همان مسیر استخراج (Extract) کنید
- پس اس استخراج فایل های هدر در مسیر خود قرار گرفتند ✅

### 2️⃣ قرار دادن npmrc
 - فایل `npmrc.` کپی کنید
 - در کنار دیگر فایل های پروژه خودتون قرارش بدید

### 3️⃣ مطمئن شوید Python و Visual Studio نصب هستند



**🐍 Python**

- اگر پایتون نصب ندارید [دانلود کنید](https://soft98.ir/software/programming/16260-python.html)
 
> ⚠️ **حتماً** گزینه **"Add Python to PATH"** را هنگام نصب انتخاب کنید



**🛠️ Visual Studio 2022**

- مطمئن شوید حتما **visual studio** نصب دارید
- **++Desktop development with C** ✅

> 📥 **دانلود Visual Studio 2022**  
> اگر ندارید، از [این لینک](https://soft98.ir/263-Visual-Studio.html) دانلود کنید



** 📌 پیشنهاد میشه یکبار سیتم خود را ریاستارت کنید بعد از اتمام این مرحله **

### 4️⃣ حالا دستور نصب را اجرا کنید
```bash
npm install @prisma/client @prisma/adapter-better-sqlite3 dotenv
```

## 🔧 مرحله 3: یک کامند ساده
```bash
npx prisma
```
- این مرحله بدون هیچ مشکلی باید انجام شود ✅


## ⚙️ مرحله 4:نصب انجین پریسما **(schema-engine)**
### 1️⃣ فایل `schema-engine.exe.gz` داخل فولدر پیدا کنید
- و در مسیر زیر استخراج (extract) کنید
```text
%USERPROFILE%\.prisma
```
> ⚠️ اگر فولدر `prisma.` وجود نداشت، خودتان بسازید

### 2️⃣ تنظیم متغیر های **PowerShell**
- یک ترمینال **PowerShell** در **VS Code** باز کنید
- دستور زیر را اجرا کنید
```powershell
$env:PRISMA_SCHEMA_ENGINE_BINARY = "$env:USERPROFILE\.prisma\schema-engine.exe"
```
> ⚠️ نکته مهم: هر بار که PowerShell را می‌بندید و دوباره باز می‌کنید، باید این دستور را دوباره اجرا کنید.
> **مگر اینکه مراحل زیر انجام دهید**
- در ویندوز `Win + R` زده و `sysdm.cpl` وارد کنید
- به قسمت `advanced` بروید و `Environment Variables` کلیک کنید
- هم در بخش **User Variables** هم **System Variables** مراحل زیر را انجام دهید
- بر روی `...New` کلیک کرده
- Variable name : `PRISMA_SCHEMA_ENGINE_BINARY`
- Variable value : `C:\Users\{YOUR_USERNAME}\.prisma\schema-engine.exe`
> ⚠️ اسم user ویندوز خودتون بجای {YOUR_USERNAME} قرار دهید

- حالا با خیال راحت کامند زیر را اجرا کنید
```bash
npx prisma init --datasource-provider sqlite --output ../generated/prisma
```
## ✅ کار شما تمام شد! Prisma نصب و آماده استفاده است.
- برای برسی نهایی
```bash
npx prisma generate
npx prisma -v
```
