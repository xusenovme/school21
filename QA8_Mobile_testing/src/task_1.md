# Vazifa 1. Mobil operatsion tizimlar


- ## MUALLIF - bradyque , delorisw

## 1. iOS uchun test ilovasini olish xizmatlari

**iOS** uchun test ilovasini olish uchun quyidagi xizmatlardan foydalanish mumkin:

- **TestFlight** - Apple'ning rasmiy beta test xizmati  

- **Xcode Organizer** - ilovalarni test uchun taqsimlash va feedback yig'ish  

- **App Store Connect** - beta test jarayonini boshqarish va testerlarni boshqarish  
- **Simulator** - Xcode'da o'rnatilgan iOS simulyatori  

- **Device Testing** - haqiqiy iOS qurilmalarda to'g'ridan-to'g'ri test qilish  

**TestFlight** - eng keng tarqalgan va Apple tomonidan tavsiya etiladigan yondashuv bo'lib, u dasturchilar va beta testerlar o'rtasida qulay aloqa o'rnatishga imkon beradi.


[**Testflight**](https://developer.apple.com/testflight/)

[**Xcode Organizer**](https://developer.apple.com/xcode/)

[**App Store Connect**](https://appstoreconnect.apple.com/)

[**Simulator**](https://developer.apple.com/xcode/)

[**Device Testing**](https://developer.apple.com/documentation/xcode/running-your-app-in-simulator-or-on-a-device)

## 2. Tashqi uzilishlar (External Interrupts)

Mobil ilova ishlaganda paydo bo'lishi mumkin bo'lgan tashqi uzilishlar quyidagilardan iborat:

- **Telefon qo'ng'irog'i** – kiruvchi yoki chiquvchi qo'ng'iroqlar
- **SMS/MMS xabarlari** – matnli yoki multimedia xabarlar kelishi
- **Push notifications** – turli ilovalardan keluvchi bildirishnomalar
- **System alerts** – tizim ogohlantirishlari (masalan, past batareya, xotira tugashi)
- **Camera/Microphone access** – boshqa ilovalar tomonidan kamera yoki mikrofon so'ralishi
- **Location services** – joylashuv xizmatlariga ruxsat so'ralishi
- **Background app refresh** – fon rejimida ilovalarning yangilanishi
- **System updates** – operatsion tizimning yangilanishlari
- **Emergency calls** – favqulodda xizmatlarga qo'ng'iroqlar
- **Hardware interrupts** – qurilma tugmalari bosilishi (Home, Volume, Power)
- **Network connectivity changes** – internet yoki tarmoq ulanishining o'zgarishi
- **Screen rotation** – qurilmaning orientatsiyasi o'zgarganda ekran aylanishi
- **Control Center / Notification Center** – foydalanuvchi tomonidan tizim panellarini ochish
- **Siri activation** – ovozli yordamchi (Siri) faollashuvi

**Bu uzilishlar mobil ilovalarning ishlashiga vaqtincha yoki doimiy ta'sir ko'rsatishi mumkin. Shuning uchun dasturchilar ushbu holatlarni oldindan hisobga olib mos ravishda ilovani loyihalashi zarur.**

## 3. Mobil ilova ish rejimi (App Lifecycle Modes)

### iOS uchun:

- **Not Running** – Ilova ishga tushmagan yoki tizim tomonidan yopilgan holat.
- **Inactive** – Ilova ishga tushgan, ammo foydalanuvchidan hech qanday hodisani qabul qilmayotgan holat.
- **Active** – Ilova to‘liq ishlamoqda va foydalanuvchi bilan bevosita aloqada.
- **Background** – Ilova fonda ishlamoqda (masalan, fon yangilanishlari uchun).
- **Suspended** – Ilova fonda ishlashni to‘xtatgan, ammo hali xotirada mavjud holat.

### Android uchun:

- **Created** – `Activity` yaratilgan.
- **Started** – `Activity` foydalanuvchiga ko‘rinmoqda, ammo u bilan bevosita aloqada emas.
- **Resumed** – `Activity` faol holatda va foydalanuvchi bilan to‘liq aloqada.
- **Paused** – `Activity` boshqa `Activity` tomonidan to‘sib qo‘yilgan, lekin hali ko‘rinadi.
- **Stopped** – `Activity` to‘liq ko‘rinmayapti, ammo tizimda mavjud.
- **Destroyed** – `Activity` butunlay yo‘q qilingan.

### Umumiy rejimlar:

- **Foreground mode** – Ilova foydalanuvchi oldida faol holatda ishlamoqda.
- **Background mode** – Ilova fon rejimida ishlamoqda.
- **Multitasking mode** – Bir nechta ilovalar bir vaqtning o‘zida faol yoki fonda ishlamoqda.

---

## 4. Xotira oqishi (Memory Leak) tushunchasi

**Xotira oqishi** – bu foydalanilmayotgan obyektlarning xotiradan tozalanmasdan qolishi natijasida yuzaga keladigan muammo. Bu holatda `Garbage Collector` obyektlarni avtomatik aniqlay olmaydi va ular tizim xotirasida qolib ketadi.

### Asosiy xususiyatlar:

- **Sabab**: Obyektlarga noto‘g‘ri yoki uzoq muddatli havolalar (`references`) saqlanib qolishi.
- **Natija**: Xotira resurslari kamayadi, ilova sekin ishlay boshlaydi.
- **Oqibat**: `OutOfMemoryError`, ilovaning ishdan chiqishi yoki performance pasayishi.

### Keng tarqalgan holatlar:

- `Activity` lifecycle'da obyektlarni noto‘g‘ri tozalash (cleanup)
- `Listener` va `Callback` funksiyalarni vaqtida `unregister` qilmaslik
- `static context`lardan noto‘g‘ri foydalanish
- `Thread`, `AsyncTask` kabi jarayonlarni noto‘g‘ri boshqarish
- Katta `Bitmap` fayllarni kerakli darajada boshqarmaslik yoki tozalamaslik

### Oldini olish usullari:

- Ilova `lifecycle`ini to‘g‘ri boshqarish
- `WeakReference` ishlatish orqali xotira bog‘lanishini yumshatish
- `Listener` va `Receiver`larni kerakli vaqtda `unregister` qilish
- Xotira monitoring vositalaridan foydalanish:  
  - **Android Studio Memory Profiler**  
  - **Xcode Instruments**

> **Eslatma:** Ushbu ma’lumotlar **iOS** va **Android** platformalari uchun umumiy **tamoyillarni qamrab oladi** hamda **zamonaviy mobil dasturlash amaliyotlariga asoslanadi.**


- ## MUALLIF - bradyque , delorisw