# Vazifa 4. Loglar va loglash

## Android tizimidagi log darajalari

- **VERBOSE (V)**  
  Eng batafsil log darajasi. Dastur ishlashini chuqur tahlil qilish va nosozliklarni topishda ishlatiladi.

- **DEBUG (D)**  
  Dasturchilar uchun qulay bo‘lgan log darajasi. Dastur xatolarini tuzatishda yordam beradi, VERBOSE ga nisbatan kamroq tafsilot beradi.

- **INFO (I)**  
  Oddiy ish faoliyati haqida ma’lumot beruvchi loglar. Masalan, muvaffaqiyatli bajarilgan amallar.

- **WARN (W)**  
  Ogohlantirishlar, muammolar bo‘lishi mumkinligini bildiradi, lekin dastur to‘xtamaydi.

- **ERROR (E)**  
  Xatoliklar haqida xabar beradi. Dastur ishida muammo yuzaga kelganini ko‘rsatadi, lekin to‘liq to‘xtashga sabab bo‘lmasligi mumkin.

- **ASSERT (A)**  
  Juda jiddiy xatoliklar yoki mantiqiy xatolar haqida xabar beradi, ular dastur ishlashida katta muammo tug‘diradi.

## Android tizimidagi log turlari

- **System Logs**  
  Android tizimining o‘zidan keladigan loglar, ya’ni yadroviy va tizim xizmatlari haqida ma’lumot.

- **Application Logs**  
  Dasturchilar tomonidan ilovada yozilgan loglar (masalan, `Log.d()`, `Log.e()` kabi).

- **Event Logs**  
  Tizim va ilovalardagi voqealar (eventlar) haqida ma’lumotlar.

- **Radio Logs**  
  GSM, WiFi, Bluetooth kabi radiomuloqot modullari haqidagi loglar.

- **Crash Logs**  
  Ilovaning ishdan chiqishi yoki xatoliklari haqida ma’lumot.

## Androidda loglarni yozish usullari

- **Logcat**  
  Loglarni real vaqt rejimida ko‘rish va yig‘ish uchun standart tizim vositasi.

- **File Logging**  
  Loglarni qurilmada fayllarga yozish, keyinchalik tahlil qilish uchun saqlash.

- **Remote Logging**  
  Loglarni masofaviy serverlarga yoki bulut xizmatlariga yuborish, markazlashgan monitoring uchun.

- **Third-party Logging Libraries**  
  Timber, Crashlytics kabi uchinchi tomon kutubxonalaridan foydalangan holda loglashni qulay va samarali qilish.

- ## MUALLIF - bradyque , delorisw