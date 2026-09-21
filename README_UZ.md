# GameGarant — Netlify Database + Functions

Bu paket GameGarant'ning markaziy server bazasi uchun tayyorlangan.

## 1. Netlify Database
Netlify panelida loyiha uchun **Data & Storage → Database → Create a database** qiling.

## 2. Environment Variables
Netlify → Site configuration → Environment variables:

- `ADMIN_SECRET` — uzun, maxfiy admin kalit
- `ADMIN_USERNAME` — admin username, masalan `FenixVertex`
- `ADMIN_PASSWORD` — kuchli admin paroli
- `ADMIN_NAME` — `Fenix Vertex`

Admin parolini `admin` qilib qo‘ymang.

## 3. Deploy
Paketning barcha fayllarini GitHub repository root'iga qo‘ying yoki Netlify'ga deploy qiling. `@netlify/database` mavjudligi sababli Netlify Database migratsiyalarni deploy jarayonida qo‘llaydi.

## 4. Natija
- Bir foydalanuvchi ro‘yxatdan o‘tsa, server database'ga yoziladi.
- Boshqa telefon/kompyuterdagi foydalanuvchi ham shu userni serverdan ko‘radi.
- Bir odam account e’lon qilsa, `/api/trades` orqali umumiy database'ga yoziladi.
- Boshqa foydalanuvchilar Brawl Stars kategoriyasida shu e’lonni ko‘radi.
- E’lonlar 15 soniyada avtomatik yangilanadi va sahifa ochilganda ham serverdan olinadi.
- Admin foydalanuvchilar ro‘yxatini serverdan olishi mumkin.

## Muhim
Bu loyiha Netlify Database (PostgreSQL) ishlatadi; MySQL emas. Netlify Functions backend rolini bajaradi.
