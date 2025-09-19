# Vazifa 3. Brauzer dvigatellari testi

## Sayt: https://21-school.ru/

## Turli brauzerlarda test natijalar

### Google Chrome (Blink dvigatel)
**Versiya**: Chrome 120+
**Kuzatilgan xususiyatlar**:
- Barcha elementlar to'g'ri ko'rsatilmoqda
- CSS animatsiyalar silliq ishlaydi
- Font rendering aniq va tushunarli
- Flexbox va Grid layoutlar to'liq qo'llab-quvvatlanadi

### Mozilla Firefox (Gecko dvigatel)
**Versiya**: Firefox 121+
**Kuzatilgan xususiyatlar**:
- Umumiy layout Chrome bilan deyarli bir xil
- Ba'zi CSS filter effectlar biroz farq qiladi
- Font rendering biroz qalinroq ko'rinadi
- Scroll animatsiya biroz sekinroq

### Microsoft Edge (Blink dvigatel)
**Versiya**: Edge 120+
**Kuzatilgan xususiyatlar**:
- Chrome bilan deyarli bir xil ko'rinish
- Har qanday sezilarli farq yo'q
- Performance yaxshi

## Aniqlangan farqlar

### 1. Font Rendering
- **Chrome**: O'rtacha qalinlikda, aniq ko'rinish
- **Firefox**: Biroz qalinroq va kontrastli
- **Edge**: Chrome bilan bir xil

### 2. CSS Shadows va Effects
- **Chrome**: Barcha shadow effectlar to'liq qo'llab-quvvatlanadi
- **Firefox**: Ba'zi murakkab shadow effectlar biroz farq qiladi
- **Edge**: Chrome bilan bir xil

### 3. Scrolling Performance
- **Chrome**: Juda silliq scroll
- **Firefox**: Biroz sekinroq, lekin qabul qilinadigan darajada
- **Edge**: Chrome bilan bir xil

### 4. CSS Grid va Flexbox
- **Chrome**: To'liq qo'llab-quvvatlash
- **Firefox**: To'liq qo'llab-quvvatlash, biroz farq yo'q
- **Edge**: To'liq qo'llab-quvvatlash

### 5. JavaScript Performance
- **Chrome**: Tez bajarilish
- **Firefox**: Biroz sekinroq, lekin yetarli
- **Edge**: Chrome bilan bir xil

### 6. Mobile Responsiveness
- **Chrome**: Barcha breakpoint-lar to'g'ri ishlaydi
- **Firefox**: Bir xil natija
- **Edge**: Bir xil natija

## Xulosa

21-school.ru sayti barcha asosiy brauzerlarda deyarli bir xil ko'rinishda ishlaydi. Eng katta farqlar font rendering va ba'zi CSS effect-larda kuzatiladi. Umumiy holatda sayt cross-browser compatibility jihatidan yaxshi holatda.

### Tavsiyalar:
1. Font rendering farqlarini kamaytirish uchun `-webkit-font-smoothing` va `-moz-osx-font-smoothing` CSS xususiyatlaridan foydalanish
2. CSS prefix-larni qo'shish (autoprefixer ishlatish)
3. Barcha brauzerlarda muntazam test o'tkazish