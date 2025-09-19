# Vazifa 4. HTTP va HTTPS protokollari

## HTTPS protokolining ishlash sxemasi

### HTTPS aloqa o'rnatish bosqichlari:

1. **Client Hello**
   - Kliyent serverga ulanish so'rovi yuboradi
   - Qo'llab-quvvatlanadigan SSL/TLS versiyalarini ko'rsatadi
   - Cipher suite-lar ro'yxatini yuboradi
   - Random sonlar generatsiya qiladi

2. **Server Hello**
   - Server SSL/TLS versiyasini tanlaydi
   - Cipher suite-ni tanlaydi
   - O'zining random sonini yuboradi
   - Session ID beradi

3. **Server Certificate**
   - Server o'zining SSL sertifikatini yuboradi
   - Sertifikat server identifikatsiyasini tasdiqlaydi
   - Ochiq kalitni o'z ichiga oladi

4. **Certificate Verification**
   - Kliyent sertifikatni tekshiradi
   - Certificate Authority (CA) orqali tasdiqlaydi
   - Sertifikat amal qilish muddatini tekshiradi

5. **Key Exchange**
   - Kliyent pre-master secret yaratadi
   - Uni server ochiq kaliti bilan shifrlaydi
   - Serverga yuboradi

6. **Session Key Generation**
   - Ikkala tomon ham master secret yaratadi
   - Pre-master secret va random sonlardan foydalanadi
   - Session kalitlari hosil qiladi

7. **Finished Messages**
   - Har ikkala tomon "Finished" xabarini yuboradi
   - Handshake jarayoni tugaydi
   - Xavfsiz aloqa boshlanadi

8. **Encrypted Communication**
   - Barcha ma'lumotlar shifrlanadi
   - Session kalitlari ishlatiladi
   - Ma'lumotlar yaxlitligi nazorat qilinadi

## HTTP Status Code guruhlari

### 1xx - Informational (Ma'lumot beruvchi)
**Ma'nosi**: So'rov qabul qilindi va jarayon davom etmoqda

**Asosiy kodlar**:
- **100 Continue**: Server so'rovning boshini qabul qildi, davom etsin
- **101 Switching Protocols**: Server protokolni o'zgartirmoqda
- **102 Processing**: Server so'rovni qayta ishlamoqda (WebDAV)

### 2xx - Success (Muvaffaqiyat)
**Ma'nosi**: So'rov muvaffaqiyatli qabul qilindi va bajarildi

**Asosiy kodlar**:
- **200 OK**: So'rov muvaffaqiyatli bajarildi
- **201 Created**: Yangi resurs yaratildi
- **202 Accepted**: So'rov qabul qilindi, lekin hali bajarilmadi
- **204 No Content**: So'rov bajarildi, lekin kontent yo'q
- **206 Partial Content**: Qisman kontent qaytarildi

### 3xx - Redirection (Qayta yo'naltirish)
**Ma'nosi**: So'rovni bajarish uchun qo'shimcha harakatlar kerak

**Asosiy kodlar**:
- **301 Moved Permanently**: Resurs butunlay boshqa manzilga ko'chirildi
- **302 Found**: Resurs vaqtincha boshqa manzilda
- **304 Not Modified**: Resurs o'zgartirilmagan (cache uchun)
- **307 Temporary Redirect**: Vaqtincha qayta yo'naltirish
- **308 Permanent Redirect**: Doimiy qayta yo'naltirish

### 4xx - Client Error (Mijoz  xatosi)
**Ma'nosi**: So'rovda xato bor yoki uni bajarib bo'lmaydi

**Asosiy kodlar**:
- **400 Bad Request**: Noto'g'ri so'rov
- **401 Unauthorized**: Autentifikatsiya talab qilinadi
- **403 Forbidden**: Ruxsat yo'q
- **404 Not Found**: Resurs topilmadi
- **405 Method Not Allowed**: HTTP usuli ruxsat etilmagan
- **408 Request Timeout**: So'rov vaqti tugadi
- **409 Conflict**: So'rov konflikt yaratdi
- **422 Unprocessable Entity**: Sintaksis to'g'ri, lekin jarayon amalga oshmadi
- **429 Too Many Requests**: Juda ko'p so'rov yuborildi

### 5xx - Server Error (Server xatosi)
**Ma'nosi**: Server so'rovni bajara olmadi

**Asosiy kodlar**:
- **500 Internal Server Error**: Serverda ichki xato
- **501 Not Implemented**: Server bu funksiyani qo'llab-quvvatlamaydi
- **502 Bad Gateway**: Gateway orqali noto'g'ri javob
- **503 Service Unavailable**: Server vaqtincha mavjud emas
- **504 Gateway Timeout**: Gateway vaqti tugadi
- **505 HTTP Version Not Supported**: HTTP versiyasi qo'llab-quvvatlanmaydi