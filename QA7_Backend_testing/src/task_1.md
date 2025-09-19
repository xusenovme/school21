# Vazifa 1: REST API va JSON

## REST API metodlari

REST API da 7 ta asosiy HTTP metodi mavjud:

### 1. GET
**Maqsadi:** Serverdan ma'lumot olish uchun ishlatiladi
- Faqat ma'lumot o'qiydi, o'zgartirmaydi
- Xavfsiz (safe) va idempotent (bir necha marta chaqirish natijasi bir xil)

### 2. POST
**Maqsadi:** Yangi resurs yaratish uchun ishlatiladi
- Ma'lumot yuboradi va yangi resurs hosil qiladi
- Xavfsiz emas, idempotent emas

### 3. PUT
**Maqsadi:** Mavjud resursni to'liq yangilash yoki yangi resurs yaratish
- Butun resursni almashtiradi
- Idempotent (bir necha marta chaqirish natijasi bir xil)

### 4. PATCH
**Maqsadi:** Mavjud resursni qisman yangilash
- Faqat o'zgartirilgan qismlarni yangilaydi
- Idempotent bo'lishi mumkin

### 5. DELETE
**Maqsadi:** Resursni o'chirish uchun ishlatiladi
- Idempotent
- Xavfsiz emas

### 6. HEAD
**Maqsadi:** GET kabi, lekin faqat sarlavhalarni (headers) qaytaradi
- Response body qaytarmaydi
- Resurs mavjudligini tekshirish uchun ishlatiladi

### 7. OPTIONS
**Maqsadi:** Server qo'llab-quvvatlaydigan metodlarni aniqlash
- CORS (Cross-Origin Resource Sharing) da ishlatiladi
- Xavfsiz va idempotent

## PUT va PATCH farqlari

| PUT | PATCH |
|-----|-------|
| Butun resursni almashtiradi | Faqat ma'lum qismlarni yangilaydi |
| Barcha maydonlarni yuborish kerak | Faqat o'zgartirilgan maydonlarni yuborish kifoya |
| Agar resurs yo'q bo'lsa, yangi yaratadi | Odatda mavjud resursni yangilaydi |
| Har doim idempotent | Idempotent bo'lishi mumkin |

**Misol:**
```
PUT /users/123 - foydalanuvchining barcha ma'lumotlarini yangilash
PATCH /users/123 - foydalanuvchining faqat email yoki ismini yangilash
```

## GET va HEAD farqlari

| GET | HEAD |
|-----|-------|
| To'liq javob qaytaradi (headers + body) | Faqat headers qaytaradi |
| Ma'lumotni ko'rish uchun ishlatiladi | Resurs mavjudligini tekshirish uchun |
| Response body bor | Response body yo'q |
| Ko'proq trafik sarflaydi | Kam trafik sarflaydi |

**Misol:**
```
GET /users/123 - foydalanuvchi ma'lumotlarini olish
HEAD /users/123 - foydalanuvchi mavjudligini tekshirish
```

## HTTP Status kodlari

### 1XX — Ma'lumot beruvchi javoblar
- **100 Continue:** So'rovni davom ettirish mumkin
- **101 Switching Protocols:** Protokol o'zgartirilmoqda

### 2XX — Muvaffaqiyatli javoblar
- **200 OK:** So'rov muvaffaqiyatli bajarildi
- **201 Created:** Yangi resurs yaratildi
- **204 No Content:** Muvaffaqiyatli, lekin qaytariladigan kontent yo'q

### 3XX — Qayta yo'naltirish
- **301 Moved Permanently:** Resurs butunlay boshqa manzilga ko'chirildi
- **302 Found:** Resurs vaqtincha boshqa manzilda
- **304 Not Modified:** Resurs o'zgartirilmagan

### 4XX — Mijoz xatosi
- **400 Bad Request:** Noto'g'ri so'rov
- **401 Unauthorized:** Autentifikatsiya talab qilinadi
- **403 Forbidden:** Ruxsat yo'q
- **404 Not Found:** Resurs topilmadi
- **405 Method Not Allowed:** Metod ruxsat etilmagan

### 5XX — Server xatosi
- **500 Internal Server Error:** Serverda ichki xato
- **502 Bad Gateway:** Noto'g'ri gateway
- **503 Service Unavailable:** Xizmat mavjud emas

## JSON haqida

### JSON qanday ochiladi?
**JSON** - **J**ava**S**cript **O**bject **N**otation

### JSON ning XML va YAML ustidan afzalliklari

#### JSON vs XML:
**JSON afzalliklari:**
- Yengilroq va ixchamroq
- Tezroq parse qilinadi
- O'qish va yozish osonroq
- JavaScript bilan bevosita ishlay oladi
- Kam memory talab qiladi

**XML ning afzalliklari:**
- Namespace qo'llab-quvvatlaydi
- Sxema validatsiyasi kuchliroq
- Atributlar va kommentlar qo'llab-quvvatlaydi

#### JSON vs YAML:
**JSON afzalliklari:**
- Tezroq parse qilinadi
- Keng qo'llab-quvvatlanadi
- Xatolarga kamroq moyil
- Minifikatsiya qilish oson

**YAML ning afzalliklari:**
- Inson uchun o'qish osonroq
- Kommentlar qo'llab-quvvatlanadi
- Ko'p qatorli matnlar bilan yaxshi ishlaydi
- Konfiguratsiya fayllari uchun qulay

### JSON Schema nima?
**JSON Schema** - JSON ma'lumotlarining tuzilishi va qoidalarini aniqlash uchun standart.

**Maqsadi:**
- Ma'lumot validatsiyasi
- Dokumentatsiya
- Kod generatsiyasi
- Ma'lumot tuzilishini aniqlash

**Misol:**
```json
{
  "type": "object",
  "properties": {
    "name": {"type": "string"},
    "age": {"type": "number", "minimum": 0}
  },
  "required": ["name"]
}
```

### Serialization va Deserialization

#### Serialization (Serializatsiya)
- **Nima:** Obyekt yoki ma'lumot tuzilishini JSON formatiga o'tkazish
- **Qachon:** Ma'lumotni saqlash yoki yuborish kerak bo'lganda
- **Misol:** JavaScript obyektni JSON stringga o'tkazish

```javascript
const user = {name: "Ali", age: 25};
const jsonString = JSON.stringify(user); // '{"name":"Ali","age":25}'
```

#### Deserialization (Deserializatsiya)
- **Nima:** JSON formatidagi ma'lumotni obyekt yoki ma'lumot tuzilishiga o'tkazish
- **Qachon:** Olingan JSON ma'lumotni ishlatish kerak bo'lganda
- **Misol:** JSON stringni JavaScript obyektga o'tkazish

```javascript
const jsonString = '{"name":"Ali","age":25}';
const user = JSON.parse(jsonString); // {name: "Ali", age: 25}
```

## Xulosa

**REST API va JSON zamonaviy web-dasturlashda asosiy texnologiyalar hisoblanadi. REST API orqali turli xil HTTP metodlar yordamida ma'lumot almashish mumkin, JSON esa ma'lumotlarni saqlash va uzatish uchun eng mashhur format hisoblanadi.**