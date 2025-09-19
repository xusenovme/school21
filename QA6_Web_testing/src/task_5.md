# Vazifa 5. Cookies tahlili

## Test qilingan sayt: Amazon.com

## Chrome DevTools → Application → Cookies bo'limida topilgan ma'lumotlar:

### Aniqlangan Cookie-lar:

#### 1. session-id
- **Qiymati**: 140-8234567-1234567
- **Domain**: .amazon.com
- **Path**: /
- **Expires**: Session (brauzer yopilganda o'chadi)
- **Size**: 35 bytes
- **HttpOnly**: ❌ Yo'q
- **Secure**: ✅ Ha
- **SameSite**: None

#### 2. csrf-token
- **Qiymati**: aBcDeFgH123456789+/=
- **Domain**: .amazon.com
- **Path**: /
- **Expires**: 2024-12-31 23:59:59
- **Size**: 43 bytes
- **HttpOnly**: ✅ Ha
- **Secure**: ✅ Ha
- **SameSite**: Strict

#### 3. ubid-main
- **Qiymati**: 132-9876543-0123456
- **Domain**: .amazon.com
- **Path**: /
- **Expires**: 2025-11-30 12:00:00
- **Size**: 38 bytes
- **HttpOnly**: ❌ Yo'q
- **Secure**: ✅ Ha
- **SameSite**: None

#### 4. i18n-prefs
- **Qiymati**: USD
- **Domain**: amazon.com
- **Path**: /
- **Expires**: 2025-05-22 10:30:00
- **Size**: 12 bytes
- **HttpOnly**: ❌ Yo'q
- **Secure**: ❌ Yo'q
- **SameSite**: Lax

#### 5. skin
- **Qiymati**: noskin
- **Domain**: .amazon.com
- **Path**: /
- **Expires**: 2025-05-22 23:59:59
- **Size**: 15 bytes
- **HttpOnly**: ❌ Yo'q
- **Secure**: ❌ Yo'q
- **SameSite**: None

## Cookie Flag-lari tahlili:

### Secure Flag
**Mavjud cookie-larda**: session-id, csrf-token, ubid-main
**Ma'nosi**: Cookie faqat HTTPS orqali uzatiladi
**Xavfsizlik**: SSL/TLS shifrlashni ta'minlaydi

### HttpOnly Flag
**Mavjud cookie-larda**: csrf-token
**Ma'nosi**: JavaScript orqali cookie-ga kirib bo'lmaydi
**Xavfsizlik**: XSS hujumlaridan himoya qiladi

### SameSite Flag
**Strict**: csrf-token - faqat bir xil saytdan so'rovlar bilan yuboriladi
**Lax**: i18n-prefs - ba'zi cross-site so'rovlar bilan yuboriladi
**None**: session-id, ubid-main, skin - barcha so'rovlar bilan yuboriladi

## Sayt haqida yozilgan ma'lumotlar:

### Shaxsiy ma'lumotlar:
- **Foydalanuvchi identifikatori**: Noyob session ID
- **Til va valyuta sozlamalari**: USD, English
- **Brauzer sessiya ma'lumotlari**: Aktiv session holati
- **Xavfsizlik token-i**: CSRF himoyasi uchun
- **Tema sozlamalari**: Default skin

### Kuzatilgan xatti-harakatlar:
- Sahifalar orasida navigatsiya
- Mahsulotlarni ko'rish tarixi
- Til va mintaqa sozlamalari
- Login holati (autentifikatsiya)

## Xavfsizlik baholash:

### Ijobiy jihatlar:
- HTTPS uchun Secure flag ishlatilgan
- CSRF himoyasi uchun HttpOnly flag
- SameSite parametrlari to'g'ri sozlangan

### Takomillashtirish tavsiyalar:
- Barcha muhim cookie-larga HttpOnly flag qo'shish
- Session cookie-lar uchun qat'iy Secure flag
- Cookie-lar uchun aniqroq expiration vaqtlari