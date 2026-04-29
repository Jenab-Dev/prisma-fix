# Prisma & better-sqlite3 Fix
# 📦 راهنمای نصب Prisma در شرایط اینترنت ملی

> راهنمای قدم‌به‌قدم برای نصب Prisma با دانلود دستی پیش‌نیازها  

---

## ⚠️ پیش‌نیازهای اولیه (قبل از شروع)

- ✅ Node.js 24.15.0 (فایل نصبی داخل فولدر قرار گرفته)
- ✅ Python (فایل نصبی داخل فولدر قرار گرفته)
- ✅ Visual Studio 2022 (C++ build tools)

> اگر VS 2022 ندارید، از [این لینک](https://soft98.ir/263-Visual-Studio.html) دانلود و نصب کنید.

---

## 📥 مرحله 1: نصب Prisma و وابستگی‌های توسعه

```bash
npm install prisma @types/node @types/better-sqlite3 -D
