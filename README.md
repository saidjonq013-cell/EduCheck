# Maktab — O‘quvchi va o‘qituvchilar uchun testlar

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

## Telefonda internet orqali ochish

`main` yoki loyiha branch’iga push qilinganda GitHub Actions saytni GitHub Pages’ga chiqaradi. Birinchi marta repository sozlamalaridagi **Settings → Pages → Build and deployment → Source** qiymatini **GitHub Actions** qilib tanlang. Deploy tugagach, sayt quyidagi manzilda ochiladi:

`https://saidjonq013-cell.github.io/EduCheck/`

GitHub Pages tarqatilishi bir necha daqiqa olishi mumkin. Sayt mobil brauzerda ochiladi; ma’lumotlar har bir qurilmada alohida saqlanadi.

## Muhim cheklov

Bu hozircha demo: turli telefon va kompyuterlar orasida ma’lumotlar ulashilmaydi, foydalanuvchi akkauntlari hamda haqiqiy server yo‘q. Internet orqali umumiy foydalanish uchun backend, ma’lumotlar bazasi, autentifikatsiya va hosting kerak bo‘ladi.