# Vazifa 1. Mijoz-server arxitekturasi

## 3 qatlamli va ko'p qatlamli Mijoz-server arxitekturasi

### Ko'p qatlamli Mijoz-server arxitekturasining asosiy komponentlari:

1. **Presentation Tier (Taqdimot qatlami)**
   - Foydalanuvchi interfeysi (UI)
   - Veb-brauzer yoki desktop ilovalar
   - Mobil ilovalar

2. **Application Tier (Ilova qatlami)**
   - Biznes logikasi
   - Veb-server (Apache, Nginx)
   - Ilova serverlari (Tomcat, Node.js)

3. **Data Tier (Ma'lumotlar qatlami)**
   - Ma'lumotlar bazasi serverlari
   - Ma'lumotlarni saqlash tizimlari
   - Fayl tizimlari

## Har bir komponentning vazifasi:

### Presentation Tier:
- **Vazifasi**: Foydalanuvchi bilan bevosita aloqa o'rnatish
- Foydalanuvchi ma'lumotlarini qabul qilish
- Natijalarni foydalanuvchiga ko'rsatish
- Interfeys elementlarini boshqarish

### Application Tier:
- **Vazifasi**: Biznes logikasini amalga oshirish
- So'rovlarni qayta ishlash
- Ma'lumotlarni validatsiya qilish
- Biznes qoidalarini bajarish
- Xavfsizlik nazorati

### Data Tier:
- **Vazifasi**: Ma'lumotlarni saqlash va boshqarish
- Ma'lumotlar yaxlitligini ta'minlash
- CRUD operatsiyalarni bajarish
- Ma'lumotlar bazasi optimizatsiyasi

## Tizim ishonchliligini ta'minlash usullari

### "Issiq" zahira (Hot Standby)

**Ta'rif**: Asosiy tizim bilan parallel ravishda ishlaydigan va darhol faollasha oladigan zahira tizim.

**Asosiy xususiyatlari**:
- **Tayorlik**: 99.9-99.99% (bir necha soniya ichida faollanadi)
- **Ma'lumotlar sinxronizatsiyasi**: Real vaqtda yoki deyarli real vaqtda
- **O'tish vaqti**: 1-30 soniya
- **Narxi**: Yuqori (ikki baravar resurs talab qiladi)

**Ijobiy tomonlari**:
- Juda tez tiklanish vaqti
- Ma'lumotlar yo'qolishi minimali
- Yuqori darajadagi xizmat ko'rsatish sifati
- Avtomatik o'tish imkoniyati

**Salbiy tomonlari**:
- Yuqori xarajatlar
- Murakkab konfiguratsiya
- Ikki nusxada resurs sarfi
- Sinxronizatsiya muammolari

### "Sovuq" zahira (Cold Standby)

**Ta'rif**: Asosiy tizim ishlamay qolganda qo'lda yoki avtomatik ravishda ishga tushiriladigan zahira tizim.

**Asosiy xususiyatlari**:
- **Tayorlik**: 95-99% (bir necha daqiqa yoki soat)
- **Ma'lumotlar sinxronizatsiyasi**: Davriy zaxira nusxalar orqali
- **O'tish vaqti**: 30 daqiqa - bir necha soat
- **Narxi**: Past (faqat zahira apparati kerak)

**Ijobiy tomonlari**:
- Arzon yechim
- Oddiy sozlash
- Kam texnik xizmat ko'rsatish
- Resurslarni tejash

**Salbiy tomonlari**:
- Sekin tiklanish vaqti
- Ma'lumotlar yo'qolishi ehtimoli
- Qo'lda aralashish talab qilinishi
- Pastroq xizmat ko'rsatish sifati