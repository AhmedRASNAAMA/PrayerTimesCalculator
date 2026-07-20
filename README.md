# 🕌 Prayer Times & Lunar Observation Calculator (TV Display & Server)
## خادم وشاشة عرض مواقيت الصلاة وحساب رؤية الهلال

Welcome to the **Prayer Times & Lunar Observation Calculator** repository. This project features a highly accurate, lightweight Rust-based calculation server combined with an elegant, customizable mosque-themed television display dashboard and web administration panel.

هذا المستودع يحتوي على **برنامج وحساب مواقيت الصلاة ورصد الهلال**. يتميز المشروع بخادم ذكي خفيف الوزن ومبني بلغة Rust عالية الأداء، بالإضافة إلى شاشة عرض تلفزيونية أنيقة للمساجد والبيوت مع لوحة تحكم وإدارة كاملة عبر الويب.

---

## 📱 Mobile & Smart TV Apps / تطبيقات الهواتف الذكية والتلفاز

* 📺 **`Android TV App`**: can be found in the following link (Google Play Store): 
* *📺 **تطبيق تلفاز أندرويد الذكي**: يمكن العثور عليه في الرابط التالي (متجر جوجل بلاي):*
https://play.google.com/store/apps/details?id=com.BestDevelopers.PrayerTimesTV

* 📱 **`Android Phone App`**: can be found in the following link (Google Play Store): 
* *📱 **تطبيق هواتف أندرويد**: يمكن العثور عليه في الرابط التالي (متجر جوجل بلاي):*
   *https://play.google.com/store/apps/details?id=com.BestDevelopers.PrayerTimes*

---

## 📦 Downloadable Deployment Packages / حزم التشغيل الجاهزة للتحميل

This repository contains precompiled, ready-to-run binary packages for various platforms. Select the ZIP file that matches your hardware and operating system:

يحتوي هذا المستودع على حزم تشغيل مجمعة مسبقاً لمختلف الأنظمة والأنظمة الفرعية. يرجى تحميل الملف المضغوط المناسب لجهازك:

* 1. 💻 **`Windows_Deploy.zip`**
   * Precompiled for Windows PCs (x86_64 architecture).
   * *نسخة مخصصة لأجهزة الكمبيوتر التي تعمل بنظام تشغيل ويندوز (معمارية 64 بت).*
* 2. 🐧 **`Linux_Deploy.zip`**
   * Precompiled for Linux PCs (x86_64 architecture like Ubuntu, Debian, Fedora, Mint).
   * *نسخة مخصصة لأجهزة الكمبيوتر التي تعمل بنظام تشغيل لينكس.*
* 3. 🍓 **`RaspberryPi_AArch64_Deploy.zip`**
   * Precompiled for 64-bit Raspberry Pi OS (Pi 3, 4, 5, Zero 2 running a 64-bit OS).
   * *نسخة مخصصة لأجهزة راسبري باي بنظام تشغيل 64 بت.*
* 4. 🍓 **`RaspberryPi_ARMv7_Deploy.zip`**
   * Precompiled for 32-bit Raspberry Pi OS (older models or 32-bit OS).
   * *نسخة مخصصة لأجهزة راسبري باي بنظام تشغيل 32 بت.*
* 5. 📺 **`AndroidTV_Server_Deploy.zip`**
   * Precompiled standalone server binary to run directly inside Termux on Android TVs.
   * *نسخة الخادم المستقل للتشغيل مباشرة داخل بيئة Termux على أجهزة تلفاز أندرويد الذكية.*

---

## 🛠️ Features / مميزات النظام

* 🕋 **High-Accuracy Calculations**: Supports worldwide preset methods (MWL, ISNA, Egypt, Umm Al-Qura, Karachi, JAKIM, MUIS, etc.) with custom offsets, Asr schools (Standard/Hanafi), and high-latitude adjustments.
   * *🕋 **حسابات عالية الدقة**: يدعم طرق الحساب العالمية المعدة مسبقًا (رابطة العالم الإسلامي، الجمعية الإسلامية لأمريكا الشمالية، الهيئة العامة للمساحة المصرية، أم القرى، كراتشي، جاكيم، مجلس علماء الإسلام، إلخ) مع تعديلات مخصصة للوقت، ومذاهب صلاة العصر (القياسي/الحنفي)، وتعديلات خطوط العرض العليا.*
* 📺 **Elegant TV Screen**: Mosque-style digital signage display showing local times, custom mosque names, Hijri date, prayer times, Iqamah countdowns, customizable announcements, and sound alerts.
   * *📺 **شاشة تلفاز أنيقة**: عرض لافتات رقمية بأسلوب المساجد يوضح الأوقات المحلية، وأسماء المساجد المخصصة، والتاريخ الهجري، ومواقيت الصلاة، والعد التنازلي للإقامة، وإعلانات قابلة للتخصيص، وتنبيهات صوتية.*
* ⚙️ **Web Dashboard**: An administration panel accessible via any web browser on your network to modify locations, coordinates, offsets, active themes, colors, and audio options.
   * *⚙️ **لوحة تحكم عبر الويب**: لوحة إدارة يمكن الوصول إليها عبر أي متصفح ويب على شبكتك لتعديل المواقع، والإحداثيات، وتعديلات الوقت، والقوالب النشطة، والألوان، والخيارات الصوتية.*
* 🌙 **Lunar Crescent API**: Predicts new moon crescent visibility based on astronomical criteria (Yallop and Odeh models), and generates global visibility grid maps.
   * *🌙 **واجهة برمجة تطبيقات (API) للهلال**: تتوقع رؤية هلال القمر الجديد بناءً على المعايير الفلكية (نماذج يالوب وعودة)، وتنشئ خرائط شبكية عالمية للرؤية.*
* ⚡ **High Performance**: Built with Rust, meaning low memory usage (typically less than 15MB RAM) and extremely fast execution.
   * *⚡ **أداء عالي**: مبني بلغة Rust، مما يعني استهلاكاً منخفضاً للذاكرة (عادة أقل من 15 ميغابايت من ذاكرة الوصول العشوائي) وتنفيذاً سريعاً للغاية.*

---

## 🚀 Installation & Running Guide / دليل التركيب والتشغيل

Select your platform below to set up and run the application:

اختر نظام التشغيل الخاص بك أدناه للاطلاع على خطوات تشغيل النظام:

### 1. 💻 Windows / نظام ويندوز

* 1. Download and extract **`Windows_Deploy.zip`** to a directory on your PC.
   * *قم بتحميل وفك ضغط ملف `Windows_Deploy.zip` في مجلد على جهازك.*
* 2. **System Requirement**: Ensure you have the **MSVC C++ Redistributable** installed to prevent missing DLL errors (like `vcruntime140.dll`):
   * *متطلب هام: تأكد من تثبيت حزمة MSVC الرسمية لتجنب مشاكل نقص ملفات النظام:*
     * [Download 64-bit (x64) Redistributable](https://aka.ms/vc14/vc_redist.x64.exe)
     * [Download 32-bit (x86) Redistributable](https://aka.ms/vc14/vc_redist.x86.exe)
* 3. Double-click the **`start.bat`** file. A terminal window will open to start the server. Keep this window open.
   * *انقر نقراً مزدوجاً على ملف `start.bat` لتشغيل خادم البرنامج. اترك النافذة السوداء المفتوحة تعمل في الخلفية.*
* 4. Open your web browser and access the interfaces:
   * *افتح متصفح الويب الخاص بك وادخل إلى الواجهات:*
   * **Dashboard**: `http://localhost:8080/`
     * **لوحة التحكم**: `http://localhost:8080/`
   * **TV Screen**: `http://localhost:8080/tv`
     * **شاشة التلفاز**: `http://localhost:8080/tv`

---

### 2. 🐧 Linux PC / نظام لينكس

* 1. Download and extract **`Linux_Deploy.zip`** on your machine.
   * *قم بتحميل وفك ضغط ملف `Linux_Deploy.zip`.*
* 2. Open terminal inside the extracted folder and grant execution permissions to files:
   * *افتح الطرفية (Terminal) داخل المجلد وامنح صلاحيات التشغيل للملفات:*
   `chmod +x start_tv.sh prayer-times-calculator`
* 3. Launch the application:
   * *قم بالتشغيل:*
   `./start_tv.sh`
   * *This script starts the server and automatically opens your browser in full-screen kiosk mode.*
   * *يقوم هذا البرنامج النصي بتشغيل الخادم ويفتح متصفحك تلقائياً في وضع ملء الشاشة.*
* 4. To configure it to **start on boot**, open your system's "Startup Applications" settings and add a startup item pointing to the absolute path of `start_tv.sh`.
   * *لضبط البرنامج بحيث **يعمل عند الإقلاع**، افتح إعدادات "تطبيقات بدء التشغيل" (Startup Applications) في نظامك وأضف عنصر بدء تشغيل يشير إلى المسار المطلق لملف `start_tv.sh`.*

---

### 3. 🍓 Raspberry Pi / جهاز راسبري باي

* 1. Download and extract the appropriate package based on your OS type:
   * *قم بتحميل وفك ضغط الحزمة المناسبة بناءً على نوع نظام التشغيل الخاص بك:*
   * **`RaspberryPi_AArch64_Deploy.zip`** (for 64-bit OS) or **`RaspberryPi_ARMv7_Deploy.zip`** (for 32-bit OS).
   * *`RaspberryPi_AArch64_Deploy.zip` (لنظام 64 بت) أو `RaspberryPi_ARMv7_Deploy.zip` (لنظام 32 بت).*
* 2. Open terminal in the folder and set execution permissions:
   * *افتح الطرفية (Terminal) في المجلد وامنح صلاحيات التشغيل:*
   `chmod +x start_tv.sh prayer-times-calculator`
* 3. Run the startup script:
   * *قم بالتشغيل:*
   `./start_tv.sh`
* 4. **Auto-Start on Boot (LXDE Desktop)**:
   * **التشغيل التلقائي عند الإقلاع (واجهة LXDE)**:
   * Create the autostart folder if needed: `mkdir -p ~/.config/autostart`
     * *أنشئ مجلد بدء التشغيل التلقائي إذا لزم الأمر: `mkdir -p ~/.config/autostart`*
   * Create an entry file: `nano ~/.config/autostart/prayertimes.desktop`
     * *أنشئ ملف إدخال: `nano ~/.config/autostart/prayertimes.desktop`*
   * Paste the following content (adjusting path to your location):
     * *الصق المحتوى التالي (مع تعديل المسار حسب موقعك):*
     
         [Desktop Entry]
         Type=Application
         Name=Prayer Times TV
         Exec=/absolute/path/to/start_tv.sh
         StartupNotify=false
         Terminal=true

---

### 4. 📺 Android TV / أجهزة التلفاز أندرويد

There are two primary methods to display the prayer times on an Android TV:
*هناك طريقتان أساسيتان لعرض مواقيت الصلاة على أجهزة تلفاز أندرويد:*

#### Method A: Networked Mode (Recommended / موصى بها)
Run the server on a local PC, Raspberry Pi, or your phone on your home/mosque Wi-Fi network, and use the TV simply as a viewer.
*قم بتشغيل الخادم على جهاز كمبيوتر محلي، أو راسبري باي، أو هاتفك على شبكة الواي فاي الخاصة بالمنزل/المسجد، واستخدم التلفاز كشاشة عرض فقط.*
* 1. Start the server on your local PC or Pi (e.g. at `http://192.168.1.100:8080`).
   * *ابدأ تشغيل الخادم على جهاز الكمبيوتر المحلي أو راسبري باي (على سبيل المثال في `http://192.168.1.100:8080`).*
* 2. Sideload a TV web browser from the Google Play Store on your Android TV (we highly recommend **TV Bro** because it supports disabling scroll, keeping screen awake, and starting on boot).
   * *قم بتثبيت متصفح ويب للتلفاز من متجر Google Play على تلفاز أندرويد الخاص بك (نوصي بشدة بمتصفح **TV Bro** لأنه يدعم تعطيل التمرير، وإبقاء الشاشة قيد التشغيل، والتشغيل عند الإقلاع).*
* 3. Type the URL `http://<YOUR-SERVER-IP>:8080/tv` inside the TV browser and switch it to full-screen.
   * *اكتب الرابط `http://<YOUR-SERVER-IP>:8080/tv` داخل متصفح التلفاز وقم بتحويله إلى وضع ملء الشاشة.*

#### Method B: Standalone Mode (Advanced / للمحترفين)
Run the server directly on the Android TV without needing another computer.
*قم بتشغيل الخادم مباشرة على تلفاز أندرويد دون الحاجة إلى جهاز كمبيوتر آخر.*
* 1. Sideload the **Termux** app on your Android TV.
   * *قم بتثبيت تطبيق **Termux** على تلفاز أندرويد الخاص بك.*
* 2. Download and extract **`AndroidTV_Server_Deploy.zip`** on your TV (you can transfer files using a USB flash drive or apps like *Send Files to TV*).
   * *قم بتحميل وفك ضغط **`AndroidTV_Server_Deploy.zip`** على التلفاز (يمكنك نقل الملفات باستخدام محرك أقراص USB أو تطبيقات مثل Send Files to TV).*
* 3. Inside Termux, navigate to the folder: `cd /path/to/extracted/folder`
   * *داخل تطبيق Termux، انتقل إلى المجلد: `cd /path/to/extracted/folder`*
* 4. Set permissions and run:
   * *قم بتعيين الصلاحيات والتشغيل:*
   
         chmod +x start_tv.sh prayer-times-calculator
         ./start_tv.sh

* 5. Open your TV's web browser and go to `http://localhost:8080/tv`.
   * *افتح متصفح الويب الخاص بالتلفاز وانتقل إلى `http://localhost:8080/tv`.*

---

## ⚙️ Customization & Configuration / الإعدادات والضبط

All settings can be modified graphically by opening the admin panel at `http://localhost:8080/` (or `http://<server-ip>:8080/` from other devices on the same network).
*يمكن تعديل جميع الإعدادات رسومياً عن طريق فتح لوحة الإدارة على `http://localhost:8080/` (أو `http://<server-ip>:8080/` من الأجهزة الأخرى على نفس الشبكة).*

Alternatively, configurations can be directly edited inside the **`tv_config.json`** file. Key parameters include:
*بدلاً من ذلك، يمكن تعديل الإعدادات مباشرة داخل ملف **`tv_config.json`**. تشمل المتغيرات الرئيسية ما يلي:*
* `latVal` / `lngVal`: Latitude and longitude of the location.
   * *خطوط الطول والعرض للموقع.*
* `elvVal`: Elevation above sea level in meters.
   * *الارتفاع عن مستوى سطح البحر بالأمتار.*
* `tzVal`: Timezone offset from UTC.
   * *فرق المنطقة الزمنية عن التوقيت العالمي المنسق (UTC).*
* `calcMethod`: Preset calculation method (options: `MWL`, `ISNA`, `Egypt`, `UmmAlQura`, `Gulf`, `Karachi`, `Tehran`, `Jafari`, `Kuwait`, `UOIF`, `Kemenag`, `MUIS`, `JAKIM`, `Moonsighting`).
   * *طريقة الحساب المعدة مسبقًا (الخيارات: رابطة العالم الإسلامي، الجمعية الإسلامية لأمريكا الشمالية، مصر، أم القرى، الخليج، كراتشي، طهران، الجعفري، الكويت، اتحاد المنظمات الإسلامية في فرنسا، كيميناغ، مجلس علماء الإسلام، جاكيم، رؤية الهلال).*
* `asrSchool`: Standard (Shafi'i, Maliki, Hanbali) or Hanafi.
   * *مذهب صلاة العصر: القياسي (الشافعي، المالكي، الحنبلي) أو الحنفي.*
* `mosqueName`: Mosque name text displayed on screen (supports Arabic/UTF-8 characters).
   * *نص اسم المسجد المعروض على الشاشة (يدعم الحروف العربية/UTF-8).*
* `clockTheme`: The appearance skin (e.g., `gold`, `green`, etc.).
   * *مظهر أو قالب الساعة (مثل: الذهبي، الأخضر، إلخ).*

---

## 🌐 HTTP API Reference / مرجع واجهة المبرمجين

* **`The API Documentation`**: is found in this repository.
   * ***`وثائق واجهة برمجة التطبيقات`**: موجودة في هذا المستودع.*
* 1. Single-Day Prayer Times API: Calculates high-accuracy astronomical prayer times for a specific location and date.
   * *1. واجهة مواقيت الصلاة ليوم واحد: تحسب مواقيت الصلاة الفلكية بدقة عالية لموقع وتاريخ محددين.*
* 2. Date Range Prayer Times API: Calculates prayer times for a range of dates (up to 366 days).
   * *2. واجهة مواقيت الصلاة لنطاق زمني: تحسب مواقيت الصلاة لنطاق من التواريخ (حتى 366 يومًا).*
* 3. Lunar Observation API: Predicts the new moon crescent visibility and the start of the Hijri month for a given range of dates.
   * *3. واجهة رصد الهلال: تتوقع رؤية هلال القمر الجديد وبداية الشهر الهجري لنطاق زمني محدد.*
* 4. Global Visibility Map API: Generates a packed global grid representing crescent visibility categories for mapping engines (like Leaflet).
   * *4. واجهة خريطة الرؤية العالمية: تنشئ شبكة عالمية مضغوطة تمثل فئات رؤية الهلال لمحركات الخرائط (مثل Leaflet).*

---

## ⚖️ License & Credits / الترخيص والحقوق

* Created by **Mr. Ahmed RASNAAMA**.
* Made with devotion to support mosque communities and astronomy observers worldwide.