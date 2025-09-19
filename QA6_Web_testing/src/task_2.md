# Vazifa 2. Chrome DevTools

## Chrome DevTools haqida umumiy ma'lumot

Chrome DevTools - bu Google Chrome brauzerida o'rnatilgan kuchli vositalar to'plami bo'lib, veb-sahifalarni tekshirish, nosozliklarni tuzatish va optimallashtirish uchun ishlatiladi.

## DevTools-ni chaqirish usullari:

1. **F12** tugmasini bosish
2. **Ctrl+Shift+I** (Windows/Linux) yoki **Cmd+Option+I** (Mac)
3. Sahifada o'ng tugma bosib, "Inspect" ni tanlash
4. Chrome menyusidan: **More Tools → Developer Tools**

## DevTools vaqtalarining vazifasi testlovchi nuqtai nazaridan:

### 1. Elements (Elementlar)
**Vazifasi**: HTML va CSS kodini tekshirish va o'zgartirish
**Testlovchi uchun foydasi**:
- DOM strukturasini tekshirish
- CSS stillarini real vaqtda o'zgartirish
- Responsiv dizaynni tekshirish
- Element o'lchamlarini aniqlash
- Accessibility xususiyatlarini tekshirish

### 2. Console (Konsol)
**Vazifasi**: JavaScript xatolarini ko'rish va kodlarni bajarish
**Testlovchi uchun foydasi**:
- JavaScript xatolarini aniqlash
- Log xabarlarini kuzatish
- Oddiy JavaScript kodlarini bajarish
- API so'rovlarini test qilish
- Performance muammolarini aniqlash

### 3. Sources (Manbalar)
**Vazifasi**: JavaScript kodini debug qilish
**Testlovchi uchun foydasi**:
- Kod breakpoint-larini qo'yish
- O'zgaruvchilar qiymatlarini kuzatish
- Kod bajarilish jarayonini kuzatish
- Minifikatsiya qilingan kodlarni o'qilishi mumkin holatga keltirish

### 4. Network (Tarmoq)
**Vazifasi**: Tarmoq so'rovlarini kuzatish
**Testlovchi uchun foydasi**:
- HTTP so'rovlar va javoblarini tekshirish
- Yuklash vaqtlarini o'lchash
- API so'rovlarini tahlil qilish
- Response va Request headerlarini ko'rish
- Network xatolarini aniqlash
- Cookies va Cache holatini tekshirish

### 5. Performance (Unumdorlik)
**Vazifasi**: Sahifa ishlash tezligini tahlil qilish
**Testlovchi uchun foydasi**:
- Sahifa yuklash vaqtini o'lchash
- Sekin ishlaydigan kodlarni aniqlash
- Memory leaks-larni topish
- CPU ishlatilishini kuzatish
- Rendering muammolarini aniqlash

### 6. Memory (Xotira)
**Vazifasi**: Xotira ishlatilishini tahlil qilish
**Testlovchi uchun foydasi**:
- Memory leaks-larni aniqlash
- Xotira sarfini kuzatish
- Garbage collection jarayonini tahlil qilish
- Heap snapshot-larini taqqoslash

### 7. Application (Ilova)
**Vazifasi**: Veb-ilova ma'lumotlarini tekshirish
**Testlovchi uchun foydasi**:
- Cookies-larni ko'rish va o'zgartirish
- Local Storage va Session Storage-ni tekshirish
- Service Workers holatini kuzatish
- Cache-ni boshqarish
- IndexedDB ma'lumotlarini ko'rish
- Manifest faylini tekshirish

### 8. Security (Xavfsizlik)
**Vazifasi**: Sahifa xavfsizligini tekshirish
**Testlovchi uchun foydasi**:
- SSL sertifikatlarini tekshirish
- Mixed content xatolarini aniqlash
- HTTPS holatini nazorat qilish
- Xavfsizlik ogohlantirish va xatolarini ko'rish

### 9. Lighthouse
**Vazifasi**: Sahifa sifatini baholash
**Testlovchi uchun foydasi**:
- Performance auditini o'tkazish
- Accessibility tekshiruvi
- SEO tahlili
- Best practices tekshiruvi
- PWA xususiyatlarini baholash

### 10. Recorder
**Vazifasi**: Foydalanuvchi harakatlarini yozib olish
**Testlovchi uchun foydasi**:
- Test stsenariylarini avtomatik yozib olish
- Takrorlanuvchi harakatlarni qayd qilish
- Regression testlari uchun skriptlar yaratish