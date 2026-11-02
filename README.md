# EduCheck

O‘zbekiston maktablari uchun o‘zbek tilidagi, mobil ekranga mos o‘quv platformasi prototipi.

## Hozirgi imkoniyatlar

- O‘quvchi panelida fanlar, topshiriqlar, baholar va matematika testi.
- O‘qituvchi panelida 11-A sinfga topshiriq qo‘shish va test natijalarini ko‘rish.
- Topshiriqlar va test natijalari shu brauzerning `localStorage` xotirasida saqlanadi.

## Ishga tushirish

`index.html` faylini brauzerda oching yoki loyiha papkasidan lokal server ishga tushiring:

```powershell
python -m http.server 8000
```

So‘ng `http://localhost:8000` manziliga kiring.

## Muhim cheklov

Bu hozircha demo: turli telefon va kompyuterlar orasida ma’lumotlar ulashilmaydi, foydalanuvchi akkauntlari hamda haqiqiy server yo‘q. Internet orqali umumiy foydalanish uchun backend, ma’lumotlar bazasi, autentifikatsiya va hosting kerak bo‘ladi.