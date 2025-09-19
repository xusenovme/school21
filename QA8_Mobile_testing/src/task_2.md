# Vazifa 2. Mobil ilovalar turlari

## 1. Mobil ilovalar turlarining ta'rifi

- ## MUALLIF - bradyque , delorisw

### 1.1 Native Apps (Mahalliy ilovalar)

Native mobil ilovalar ularni qurilayotgan qurilmaga xos bo'lgan kod yordamida quriladi. Agar siz iOS ilovasi yaratsangiz, Objective-C yoki Swift dasturlash tillaridan foydalanasiz. Android uchun esa Java yoki Kotlin ishlatiladi.

**Asosiy xususiyatlari:**
- Platformaga xos dasturlash tillari ishlatiladi
- To'g'ridan-to'g'ri App Store va Google Play orqali tarqatiladi
- Qurilmaning barcha funksiyalariga to'liq kirish imkoniyati
- Optimal performance va user experience

### 1.2 Web Apps (Veb ilovalar)

> Web ilovalar - bu brauzer orqali ishlaydigan veb-saytlarning rivojlangan shakli. Ular HTML, CSS va JavaScript texnologiyalari yordamida yaratiladi va har qanday qurilmada brauzer orqali ishlay oladi.

**Asosiy xususiyatlari:**
- Brauzer orqali ishleydi
- Platform mustaqil
- Internet aloqasi talab qiladi
- Yuklab olish shart emas

- ## MUALLIF - bradyque , delorisw

### 1.3 Hybrid Apps (Gibrid ilovalar)

> Gibrid ilovalar - bu veb texnologiyalar (HTML, CSS, JavaScript) yordamida yaratilgan, lekin native container ichida ishlaydigan ilovalar. Ular bir nechta platformada ishlay oladi.

**Asosiy xususiyatlari:**
- Bir kod bazasi, bir nechta platforma
- Native va web texnologiyalarning kombinatsiyasi
- WebView komponentidan foydalanadi
- App Store'larda tarqatiladi

### 1.4 Progressive Web Apps (PWA)

> Progressive Web Apps (PWA) - bu native mobil ilovalar xatti-harakatini taqlid qiluvchi veb ilovalar (ular bildirishnomalar yuborishi, kamera ishlatishi, joylashuv so'rashi mumkin). Ular odatda veb brauzer orqali kirish mumkin, lekin qurilmaga o'rnatilishi va unga kirish ham mumkin.

**Asosiy xususiyatlari:**
- Offline ishlash imkoniyati
- Push notifications
- Native ilova kabi tuyg'u
- Brauzerda ham, qurilmada ham ishleydi

### 1.5 Cross-Platform Apps (Ko'p platformali ilovalar)

> Cross-platform ilovalar - bu bir kod bazasi yordamida bir nechta platforma uchun yaratilgan ilovalar. Flutter, React Native, Xamarin kabi framework'lar ishlatiladi.

**Asosiy xususiyatlari:**
- Bir kod bazasi, ko'p platforma
- Native performance'ga yaqin
- Platformaga xos UI komponentlari
- Tez rivojlantirish jarayoni

## 2. Har bir tur uchun ijobiy va salbiy tomonlar

### 2.1 Native Apps

#### Ijobiy tomonlar:
- Yuqori performance: Ilova ma'lum bir platforma uchun qurilganligi sababli, u qurilmaning apparat va dasturiy ta'minotiga optimallashtirilgan bo'lishi mumkin
- To'liq qurilma funksiyalariga kirish: Kamera, GPS, sensörlar, push notifications
- Eng yaxshi foydalanuvchi tajribasi: Platform dizayn standartlariga to'liq mos keladi
- Yuqori xavfsizlik: Platformaning xavfsizlik imkoniyatlaridan to'liq foydalanish
- Offline ishlash: To'liq offline funksionallik
- App Store optimizatsiyasi: Platform do'konlarida yaxshi ko'rinadi

#### Salbiy tomonlar:
- Yuqori xarajat: Har bir platforma uchun alohida dasturchi kerak
- Uzoq rivojlantirish vaqti: Har bir platforma uchun alohida kod yozish
- Murakkab maintenance: Bir nechta kod bazasini saqlash
- Maxsus ko'nikmalar kerak: Har bir platforma uchun maxsus bilim
- Yangilanishlar murakkab: Har bir platforma uchun alohida yangilanish

### 2.2 Web Apps

#### Ijobiy tomonlar:
- Arzon rivojlantirish: Bir kod bazasi, barcha platformalar
- Tez deployment: Darhol yangilanishlar
- Platform mustaqilligi: Har qanday qurilmada ishleydi
- Oson maintenance: Faqat bitta kod bazasi
- SEO imkoniyatlari: Qidiruv tizimlarida topilishi mumkin
- Yuklab olish shart emas: Brauzer orqali darhol kirish

#### Salbiy tomonlar:
- Cheklangan funksionallik: Qurilma xususiyatlariga cheklangan kirish
- Internet bog'liqligi: Offline ishlash cheklangan
- Sekinroq performance: Native ilovalardan sekinroq
- Brauzer cheklovlari: Har xil brauzerlarda turlicha ishlashi
- App Store'da yo'q: Platformalar do'konida bo'lmaydi

### 2.3 Hybrid Apps

#### Ijobiy tomonlar:
- Cross-platform rivojlantirish: Bir kod, ko'p platforma
- Arzonroq: Native'ga nisbatan kamroq xarajat
- Tezroq rivojlantirish: Veb texnologiyalar ishlatish
- Plugin'lar orqali native funksiyalar: Qurilma xususiyatlariga kirish
- Mavjud veb jamoadan foydalanish: HTML/CSS/JS bilganlar ishlashi mumkin
- App Store'da mavjud: Platform do'konlarida tarqatiladi

#### Salbiy tomonlar:
- Performance muammolari: Native'ga nisbatan sekinroq
- UI/UX cheklovlari: Platform-specific dizayn qiyinroq
- WebView bog'liqligi: Browser engine limitatsiyalari
- Debugging murakkabligi: Ko'p qatlamli arxitektura
- Plugin'larga bog'liqlik: Uchinchi tomon yechimlariga tayaniş

### 2.4 Progressive Web Apps (PWA)

#### Ijobiy tomonlar:
- Offline ishlash: Service worker texnologiyasi
- Push notifications: PWA'lar qurilma apparat xususiyatlariga kirish imkoniyatiga ega
- Responsive dizayn: Barcha qurilmalarda yaxshi ko'rinadi
- Tez yuklash: Caching strategiyalari
- SEO uchun yaxshi: Qidiruv tizimlarida indekslanadi
- Arzon va tezkor bozorga chiqish: Veb texnologiyalar ishlatish

#### Salbiy tomonlar:
- To'liq funksionallik va performance native ilovalarga nisbatan cheklangan
- iOS'da cheklangan qo'llab-quvvatlash: Safari'da ba'zi funksiyalar ishlamaydi
- App Store'da cheklangan: Ba'zi platformalarda qabul qilinmaydi
- Brauzer bog'liqligi: Browser capabilities'ga cheklangan
- Native API'larga cheklangan kirish: Barcha qurilma funksiyalari mavjud emas

### 2.5 Cross-Platform Apps

#### Ijobiy tomonlar:
- Performance, xarajat va platformalar qamrovi o'rtasidagi muvozanat
- Bir kod bazasi: Ko'p platformada ishleydi
- Native performance'ga yaqin: Zamonaviy framework'lar
- Tez rivojlantirish: Kod qayta ishlatish
- Katta hamjamiyat: React Native, Flutter kabi mashhur framework'lar
- Hot reload: Tez debug va test qilish

#### Salbiy tomonlar:
- Framework bog'liqligi: Maxsus texnologiya o'rganish kerak
- Platformaga xos xususiyatlar: Ba'zi native funksiyalar cheklangan
- Performance trade-off'lari: Cross-platform va hybrid yechimlar ozgina performance savdosini keltirib chiqarishi mumkin
- Debugging murakkabligi: Ko'p qatlamli abstraksiya
- Framework yangilanishlari: Uchinchi tomon texnologiyaga bog'liqlik

## Xulosa

**Native ilovalar ajoyib foydalanuvchi tajribasini taqdim etsa-da, cross-platform rivojlantirish xarajat va vaqtni kamaytiradi. Ikkala yondashuvning o'rtasi sifatida, progressive web app rivojlantirish barcha xususiyatlarning eng yaxshisini birlashtirishi mumkin.**

> **Har bir tur o'zining afzalliklari va kamchiliklariga ega bo'lib, loyihaning talablari, byudjet, vaqt va maqsadli auditoriyaga qarab tanlanishi kerak.**

- ## MUALLIF - bradyque , delorisw