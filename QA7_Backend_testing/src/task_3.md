# Vazifa 3: Ma'lumotlar bazalari

## 1. Relyatsion va norelyatsion ma'lumotlar bazalarining farqlari

### Relyatsion ma'lumotlar bazalari (SQL)

**Ta'rif:** Ma'lumotlar jadvallar (tables) ko'rinishida saqlanadi va jadvallar orasida bog'lanishlar (relationships) mavjud.

**Misol tuzilishi:**
```
Foydalanuvchilar jadvali:
ID | Ism    | Email           | Telefon
1  | Ali    | ali@mail.com    | +998901234567
2  | Olim   | olim@mail.com   | +998907654321

Buyurtmalar jadvali:
ID | Foydalanuvchi_ID | Mahsulot      | Narx
1  | 1                | Telefon       | 1000000
2  | 2                | Noutbuk       | 5000000
```

### Norelyatsion ma'lumotlar bazalari (NoSQL)

**Ta'rif:** Ma'lumotlar turli formatlarda saqlanadi: dokumentlar, kalit-qiymat juftliklari, graf strukturalar.

**Misol tuzilishi (JSON document):**
```json
{
  "id": 1,
  "ism": "Ali",
  "email": "ali@mail.com",
  "telefon": "+998901234567",
  "buyurtmalar": [
    {
      "mahsulot": "Telefon",
      "narx": 1000000,
      "sana": "2024-01-15"
    }
  ]
}
```

## Asosiy farqlar

| Jihat | Relyatsion (SQL) | Norelyatsion (NoSQL) |
|-------|------------------|---------------------|
| **Ma'lumot tuzilishi** | Qat'iy jadval tuzilishi | Moslashuvchan tuzilish |
| **Til** | SQL | Turli API/tillari |
| **Bog'lanishlar** | Jadvallar orasida bog'lanish | Ko'pincha bog'lanishsiz |
| **Masshtablanish** | Vertikal (server quvvatini oshirish) | Gorizontal (server sonini oshirish) |
| **Tranzaksiyalar** | ACID xususiyatlari | BASE xususiyatlari |

## 2. Relyatsion ma'lumotlar bazalarining afzalliklari va kamchiliklari

### ✅ Afzalliklari:
1. **Ma'lumot yaxlitligi** - qat'iy qoidalar va cheklovlar
2. **Murakkab so'rovlar** - JOIN, GROUP BY kabi kuchli operatorlar
3. **Standartlashtirilgan** - SQL tili universal
4. **ACID xususiyatlari** - tranzaksiyalar ishonchliligi
5. **Yetuk texnologiya** - ko'p yillik tajriba va qo'llab-quvvatlash
6. **Xavfsizlik** - riblangan huquqlar tizimi

### ❌ Kamchiliklari:
1. **Qat'iy struktura** - o'zgartirishlar qiyin
2. **Vertikal masshtablash** - faqat server quvvatini oshirish orqali
3. **Murakkab ma'lumotlar** - JSON, XML kabi formatlar bilan qiyin ishlash
4. **Yuqori narx** - litsenziya va qo'llab-quvvatlash
5. **Sekinlik** - katta hajmdagi ma'lumotlarda
6. **NoSQL ga nisbatan kam moslashuvchanlik**

## 3. Norelyatsion ma'lumotlar bazalarining afzalliklari va kamchiliklari

### ✅ Afzalliklari:
1. **Moslashuvchanlik** - struktura o'zgartirilishi oson
2. **Gorizontal masshtablash** - ko'p serverlarga tarqatish
3. **Yuqori tezlik** - oddiy operatsiyalarda
4. **Katta ma'lumotlar** - Big Data bilan yaxshi ishlash
5. **Arzon** - ko'pincha open-source
6. **Zamonaviy formatlar** - JSON, XML bilan yaxshi ishlash
7. **Cloud-ready** - bulutli muhit uchun mos

### ❌ Kamchiliklari:
1. **Ma'lumot yaxlitligi** - kamroq nazorat
2. **Murakkab so'rovlar** - JOIN operatsiyalari yo'q yoki cheklangan
3. **Standart yo'q** - har bir tizim o'z API sine ega
4. **Eventual Consistency** - ma'lumotlar darhol sinxronlanmasligi mumkin
5. **Yetuk mutaxassislar kam** - nisbatan yangi texnologiya
6. **Xavfsizlik** - kamroq riblangan huquqlar tizimi

## 4. SUBBD larning farqlari

### MySQL vs PostgreSQL

| Jihat | MySQL | PostgreSQL |
|-------|--------|------------|
| **Turi** | Relyatsion SUBBD | Obyekt-relyatsion SUBBD |
| **Litsenziya** | GPL va tijoriy | PostgreSQL (bepul) |
| **Tezlik** | Tez (oddiy so'rovlarda) | Sekinroq (murakkab so'rovlarda yaxshi) |
| **Ma'lumot turlari** | Standart SQL turlari | Keng spektr (JSON, XML, Array) |
| **Tranzaksiyalar** | Cheklangan | To'liq ACID qo'llab-quvvatlash |
| **Replikatsiya** | Master-Slave | Master-Master, Master-Slave |
| **Kengaytirish** | Cheklangan | Keng imkoniyatlar (extensions) |
| **Qo'llanish** | Web-ilovalar, CMS | Murakkab ilovalar, analitika |

### MySQL vs SQLite

| Jihat | MySQL | SQLite |
|-------|--------|---------|
| **Arxitektura** | Mijoz-server | Fayl asosida |
| **O'rnatish** | Server talab qiladi | Faqat kutubxona |
| **Foydalanuvchilar** | Ko'p foydalanuvchi | Bitta foydalanuvchi (ko'pincha) |
| **Hajmi** | Katta bazalar uchun | Kichik-o'rta bazalar uchun |
| **Sozlash** | Murakkab sozlash | Sozlash talab etmaydi |
| **Qo'llanish** | Web-saytlar, katta ilovalar | Mobil ilovalar, prototipar |

### PostgreSQL vs MongoDB

| Jihat | PostgreSQL | MongoDB |
|-------|------------|---------|
| **Turi** | Relyatsion | Dokument asosida (NoSQL) |
| **Ma'lumot formati** | Jadvallar | JSON dokumentlari |
| **So'rov tili** | SQL | MongoDB Query Language |
| **Schema** | Qat'iy schema | Schema yo'q |
| **Tranzaksiyalar** | To'liq ACID | Cheklangan ACID |
| **Masshtablash** | Vertikal | Gorizontal |
| **Qo'llanish** | Murakkab biznes logika | Kontent boshqaruvi, real-time |

### Oracle vs MySQL

| Jihat | Oracle | MySQL |
|-------|---------|--------|
| **Narx** | Juda qimmat | Bepul/Arzon |
| **Imkoniyatlar** | Juda boy | Oddiy |
| **Samaradorlik** | Juda yuqori | Yaxshi |
| **Qo'llab-quvvatlash** | Professional | Community/Tijoriy |
| **Murakkablik** | Juda murakkab | Oddiy |
| **Qo'llanish** | Korporativ tizimlar | Web-ilovalar |

## 5. Qaysi SUBBD ni tanlash?

### Relyatsion (SQL) tanlang agar:
- Ma'lumotlar orasida murakkab bog'lanishlar bor
- Ma'lumot yaxlitligi juda muhim
- Murakkab hisobotlar va analitika kerak
- Tranzaksiyalar ko'p (bank tizimlari)
- Jamoa SQL biladi

**Masalan:** Bank tizimi, CRM, ERP tizimlari

### Norelyatsion (NoSQL) tanlang agar:
- Ma'lumot strukturasi tez-tez o'zgaradi
- Juda katta hajmdagi ma'lumotlar
- Yuqori tezlik kerak
- Gorizontal masshtablash zarur
- JSON kabi formatlar bilan ishlash

**Masalan:** Ijtimoiy tarmoqlar, IoT tizimlari, real-time analytics

## Xulosa

Har bir SUBBD o'z maqsadi va vazifasi uchun yaratilgan. To'g'ri tanlash loyiha talablariga bog'liq:

- **Kichik loyihalar uchun:** SQLite
- **Web-saytlar uchun:** MySQL
- **Murakkab ilovalar uchun:** PostgreSQL  
- **Katta ma'lumotlar uchun:** MongoDB, Cassandra
- **Korporativ uchun:** Oracle, SQL Server

Eng muhimi - loyiha ehtiyojlarini to'g'ri baholash va shunga mos SUBBD tanlashdir.