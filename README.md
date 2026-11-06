# Chust Davomat

Chust tumani maktab direktorlari uchun telefon brauzeriga mos davomat prototipi.

## Ishga tushirish

`index.html` faylini HTTPS orqali oching (masalan, GitHub Pages) yoki loyiha papkasidan:

```powershell
python -m http.server 8000
```

`http://localhost:8000` manzilida birinchi admin login va parolini yarating. Admin “Maktablar” bo‘limidan maktablarni qo‘lda qo‘shishi yoki CSV import qilishi mumkin.

## Telefonda internet orqali ochish

GitHub repository’da **Settings → Pages → Build and deployment → Source** ni **GitHub Actions** qilib tanlang. So‘ng `agents/mn-sn-bilan-maktab-uchun-dastur-yaratiwimiz-kera` branch’iga yuborilgan kod Actions orqali tarqatiladi. Deploy muvaffaqiyatli bo‘lgach, telefoningizda <https://saidjonq013-cell.github.io/EduCheck/> manzilini oching. Agar GitHub Pages sozlamasiga kira olmasangiz, repository egasidan yoqib berishini so‘rang.

Admin va direktor parol bilan kirgach, yuqoridagi **Face ID / biometrikani yoqish** tugmasi orqali passkey qo‘shishi mumkin. Keyingi kirishda login nomini yozib, biometrik kirish tugmasini bosing. HTTPS kerak; iPhone Face ID, Android barmoq izi yoki qurilma PIN’i brauzer va qurilma qo‘llashiga qarab ishlaydi.

CSV sarlavhalari:

```text
school_name,director_name,username,address,latitude,longitude
```

CSV import qilingan direktorlar uchun “Parol o‘rnatish” tugmasidan alohida parol belgilang. Xarita nuqtalari uchun latitude/longitude kiriting. Google Maps’da barcha maktablarni ko‘rsatish uchun “Davomat” sahifasidan KML’ni yuklab Google My Maps’ga import qiling; My Maps embed URL’ni “Xarita” bo‘limiga kiriting.

## Muhim cheklovlar

- Bu faqat prototip: akkauntlar va davomat shu brauzer qurilmasining `localStorage`’ida saqlanadi; turli telefonlarda ulashilmaydi. Brauzer ma’lumotlari o‘chirilsa, yozuvlar yo‘qoladi.
- Parollar lokalda xeshlangan bo‘lsa ham, bu server autentifikatsiyasi emas. Haqiqiy, ko‘p qurilmali tizim uchun backend, ma’lumotlar bazasi va himoyalangan hosting kerak.
- Passkey brauzer WebAuthn API bilan qurilma biometrikasi/PIN’ini tasdiqlaydi, ammo ushbu prototipda passkey va ochiq kalit brauzer xotirasida turadi. Bu server tekshiruvining o‘rnini bosmaydi va boshqa qurilmaga avtomatik o‘tmaydi.
- Selfi kamerada olinib tekshiruv tugagach tashlanadi; rasm saqlanmaydi va yuz bo‘yicha shaxsni avtomatik aniqlash amalga oshmaydi.
- GPS faqat maktab koordinatalari mavjud bo‘lsa so‘raladi; 500 metrdan uzoqda davomat yuborilmaydi.
- Maktablar ro‘yxatiga rasmiy ma’lumotlar kiritilishi kerak; hozircha haqiqiy direktorlar/koordinatalar kiritilmagan.
- Eski o‘quvchi/o‘qituvchi demo sahifasi `student-app.html` faylida qolgan.

GitHub Pages manzili: <https://saidjonq013-cell.github.io/EduCheck/>
