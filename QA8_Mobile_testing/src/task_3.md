# Vazifa 3. Android Studio bilan ishlash

## 1. Android Studio o‘rnatilishi  
[Rasmiy Sayt](https://www.googleadservices.com/pagead/aclk?sa=L&ai=DChsSEwiTv-qYgYCOAxX6KqIDHf_vKd0YACICCAEQABoCbGU&co=1&ase=2&gclid=Cj0KCQjwjdTCBhCLARIsAEu8bpLBsuBpgyiTvFmAUqHChPF6GobbYHoI1y11aPOx8rrKlbJ088NvmIEaAnjlEALw_wcB&ohost=www.google.com&cid=CAESV-D2EOljU7C9_G22m5g-ODUGsCiL0Bc4XU7DP0u9rRbS-RhfCxXdsinlsLMcqTnbXRm3wKBmdEdsAm-JUo0WS8u5WHXFihZzaIjwBijm3iHqtoT_PIgVUQ&category=acrcp_v1_45&sig=AOD64_2OUZioic-WVf60h-G0C5F9cU6wnQ&q&nis=4&adurl&ved=2ahUKEwjYw-WYgYCOAxUmHBAIHYOFIA0Q0Qx6BAgJEAE)
- Rasmiy sayt orqali o‘rnatildi.  
- Standart o‘rnatish turi tanlandi.  
- SDK `/home/bradyque/Android/Sdk` ga o‘rnatildi.

## 2. Emulyator yaratish  
> AVD yaratishga harakat qilganda xato yuz berdi:  
An error occurred while creating the AVD. See idea.log for details.  
Tekshirildi: virtualizatsiya qo‘llab-quvvatlanadi (vmx).  
O‘rnatilgan paketlar:  
bash sudo apt install qemu-kvm libvirt-daemon-system libvirt-clients bridge-utils virt  
manager sudo adduser $USER kvm sudo adduser $USER libvirt  
Qayta ishga tushirish bajarildi. AVD yaratishni qayta sinash rejalashtirilmoqda.

- ## MUALLIF - bradyque , delorisw

## 3. Ishlab chiquvchi rejimi (emulyator)  
Yoqilgan orqali: Settings → About phone → Build number (7 marta)  
USB Debugging Developer options da yoqilgan.

## 4. Logcat  
Logcat ishlatildi ilova loglarini ko‘rish uchun.  
Filtrlar qo‘llanildi: **ActivityManager, System.err.**

## 5. Xcode da emulyator yaratish (macOS)  
Xcode o‘rnatish.  
O‘tilish: **Xcode → Settings → Components — iOS** ni yuklab olish.  
Ochish: **Window → Devices and Simulators.**  
Simulators yorlig‘ida **+ → model va versiya tanlash.**  
- **Create tugmasini bosish.**


- ## MUALLIF - bradyque , delorisw