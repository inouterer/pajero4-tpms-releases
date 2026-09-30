<p align="center">
  <img src="https://tpms.ivlebedev.ru/logo.png" width="110" alt="Pajero IV TPMS">
</p>

<h3 align="center">Pajero IV TPMS &amp; Dashboard</h3>

<p align="center">
  Tyre pressure, A/T oil temperature and trip computer for Mitsubishi <b>Pajero IV / Montero IV / Shogun</b><br>
  and other high-speed CAN Mitsubishi models — on any Android head unit or phone with an ELM327 adapter.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Android-7.0%2B-3DDC84?logo=android&logoColor=white" alt="Android 7.0+">
  <img src="https://img.shields.io/badge/core-free%20forever-brightgreen" alt="Core version is free">
  <img src="https://img.shields.io/badge/PRO-one--time%20purchase%20%C2%B7%20lifetime-blue" alt="PRO is a one-time purchase">
  <a href="https://www.rustore.ru/catalog/app/com.pajero4.tpms"><img src="https://img.shields.io/badge/RuStore-available-blueviolet" alt="RuStore"></a>
  <a href="../../releases/latest"><img src="https://img.shields.io/github/v/release/inouterer/pajero4-tpms-releases?label=latest&sort=semver" alt="Latest release"></a>
</p>

<p align="center">
  <img src="https://tpms.ivlebedev.ru/img/hor/photo_7_2026-09-12_11-29-16.jpg" width="800" alt="Pajero IV TPMS running on an Android head unit">
</p>

> **This repository is the download page and the release archive.** Only ready-to-install APKs and release notes are published here — the application source code is not public.

Reads the factory TPMS ECU, the transmission control module and the engine ECU directly over Bluetooth OBD-II. No dealer MUT-III scanner, no wiring, no additional hardware beyond a compatible ELM327 adapter.

---

## Download

| Channel | What you get |
| :--- | :--- |
| ⬇️ **[GitHub Releases — latest APK](../../releases/latest)** | Direct APK for Android 7.0+. No store account and no Google services required. Download it on the head unit (or copy it to a USB stick) and install. |
| 🛒 **[RuStore](https://www.rustore.ru/catalog/app/com.pajero4.tpms)** | Store install with automatic updates and in-app purchase of the PRO modules. Listed in the store as *«Pajero IV TPMS &amp; температура АКПП»*. |
| 🌐 **[tpms.ivlebedev.ru](https://tpms.ivlebedev.ru)** | Official website: full description, FAQ, licence purchase (Mir / Visa / Mastercard, SBP, international cards). |

**Current version: 1.7** (build 9) · APK ≈ 4 MB · Android 7.0+ (minSdk 24, target Android 14) · no account required.

### Install from an APK (5 steps)

1. Download the APK from the [latest release](../../releases/latest).
2. Allow installation from unknown sources for the app you open the file with (file manager or browser).
3. Install and launch the app; grant the Bluetooth permission (required on Android 12+).
4. Pair your ELM327 adapter in the Android Bluetooth settings, plug it into the OBD-II port and switch the ignition on.
5. Select the adapter inside the app — wheel data appears within a few seconds.

The adapter must be a **genuine ELM327 v1.5 (PIC18F25K80)**. Cheap v2.1 clones cannot send the extended CAN requests this app relies on and will not work.

---

## What the app does

### Tyre monitoring (TPMS) — free

Direct polling of the factory TPMS ECU: pressure and temperature for each wheel, on a live chassis layout.

- Pressure in bar, psi or kPa; temperature in °C or °F
- Factory sensor ID (hex) and raw sensor status per wheel
- 4 wheels by default, 5th (spare) wheel once it is registered
- Colour-coded states and vibration alert on a critical pressure drop
- Read and clear TPMS diagnostic trouble codes (DTC)

### Live dashboard: A/T oil and engine — PRO

Keeps an eye on the transmission before it overheats — towing, sand, snow, long traffic jams.

- Automatic transmission fluid temperature (A/T Oil Temp)
- Engine coolant temperature (ECT)
- Battery / alternator voltage
- Outside temperature from the climate control unit

### Sensor registration — PRO

Write new sensor IDs into the vehicle memory when swapping between summer and winter wheel sets — no dealership, no MUT-III.

- Step-by-step registration wizard (FL → FR → RR → RL → spare)
- Activation by deflating each wheel, as in the factory procedure
- Current sensor IDs are read for free; only writing requires PRO

### Trip computer — PRO

Fuel metrics calculated from injector pulses and vehicle speed.

- Instant consumption (l/100 km and l/h at idle)
- Remaining fuel in the tank in litres and distance to empty (DTE)
- Current trip and cumulative totals that survive app restarts
- User calibration multiplier for accurate consumption

### Diagnostics and terminal — free

- Adapter communication log (last 300 lines) with copy and clear actions
- OBD-II terminal for sending manual commands and PIDs to the adapter
- One-tap diagnostic report to the developer with your own comment
- Automatic warning when another OBD application is sharing the adapter

---

## Screenshots

| Main menu | Tyre pressure & temps | A/T oil & live metrics | Trip computer |
| :---: | :---: | :---: | :---: |
| <img src="https://tpms.ivlebedev.ru/img/vert/photo_4_2026-09-12_11-29-16.jpg" width="190" alt="Main menu and cover"> | <img src="https://tpms.ivlebedev.ru/img/vert/photo_3_2026-09-12_11-29-16.jpg" width="190" alt="Tyre pressure and temperature"> | <img src="https://tpms.ivlebedev.ru/img/vert/photo_2_2026-09-12_11-29-16.jpg" width="190" alt="A/T oil temperature and live metrics"> | <img src="https://tpms.ivlebedev.ru/img/vert/photo_1_2026-09-12_11-29-16.jpg" width="190" alt="Trip computer and fuel economy"> |
| Theme (Classic / Restyle / Auto) and units | Chassis layout with pressure, temperature and sensor IDs | A/T fluid temp, coolant temp, battery voltage | Instant l/100 km, gear indicator, tank litres |

Dark automotive interface designed to stay readable in daylight and at night. The layout adapts to phone screens and to landscape head units (Teyes CC3, Mekede, Dasaita and similar).

---

## Compatibility

Works with Mitsubishi high-speed CAN vehicles equipped with a factory TPMS ECU:

- Pajero IV (3.0 / 3.8 petrol, 3.2 Di-D diesel) — including NMPS
- Outlander III (2012–2021, key or KOS)
- Outlander XL (2006–2012)
- ASX / RVR / Outlander Sport
- Pajero Sport 3 (early models with CAN TPMS)
- Eclipse Cross (1st generation)
- Lancer X / Ralliart / Evolution X
- Citroën C-Crosser / Peugeot 4007

**Hardware:** Bluetooth OBD-II adapter ELM327 v1.5 on the PIC18F25K80 chip, Android 7.0 or newer. The ELM327 serves one application at a time — close Car Scanner, Torque or any other scanner before starting this app, otherwise CAN replies get mixed up (version 1.7 detects this and shows a warning).

---

## Free vs PRO

The core is **free forever** and not a trial: tyre pressure and temperature monitoring plus TPMS DTC reading and clearing.

Two optional PRO modules can be unlocked inside the app:

| Module | Unlocks |
| :--- | :--- |
| **Live Dashboard** | A/T oil temperature, coolant temperature, battery voltage, trip computer, fuel consumption and DTE |
| **TPMS Registration** | Step-by-step writing of sensor IDs into the vehicle memory, seasonal wheel set swaps |
| **All-in-one bundle** | Both modules at once |

How licensing works:

- **One-time purchase, lifetime licence** — no subscription, no recurring fees.
- The licence is bound to **your e-mail**, not to the adapter or the head unit, and covers up to **3 personal devices** (head unit, phone, tablet).
- Activation takes one online request: enter your e-mail in the app, receive a 4-digit code, and the app then works **100% offline**.
- Purchases can be made in-app (RuStore) or on the official website (SBP, Mir / Visa / Mastercard, international cards). Current prices are shown in the app and on the website — they differ per channel.

---

## FAQ

**Which adapter should I buy?**
A genuine ELM327 Bluetooth v1.5 with the PIC18F25K80 chip. Mini v2.1 clones and BLE-only dongles generally fail — they cannot send extended CAN requests.

**Nothing is being read from my car. Why?**
In most cases the adapter is busy: another OBD app (Car Scanner, Torque, the built-in head unit scanner) is still running in the background. Close it, restart Bluetooth and reconnect. Version 1.7 shows a red warning banner when it detects such a conflict. Also check that the ignition is on and the adapter is plugged in firmly.

**Do I need internet in the car?**
Only once, for a couple of seconds, when activating a licence. After activation the app works fully offline — and so does the free version from the start.

**Do I need an account or Google services?**
No. No account, no Google Play services, no ads.

**What happens if I change the head unit, phone or adapter?**
Nothing is lost: the licence lives on your e-mail. Install the app, request a new code and activate the new device (up to 3 devices total).

**How many wheels are supported?**
Four by default. The spare wheel is polled once it has been registered.

**Why do sensors show no data after the car has been parked?**
The sensors sleep to save their batteries (5–7 years of service life). Drive 1–2 km above 25 km/h and the readings return.

**Is the source code available?**
Not currently — this repository hosts release binaries, this page and the release notes. Bug reports and questions about the builds are welcome in [Issues](../../issues).

**Does the app send any data anywhere?**
There is no background telemetry. A diagnostic report (adapter exchange log plus your comment) is sent to the developer only when you explicitly tap the send button in the log dialog. Licence activation performs a single online request to verify the code — everything else works offline.

---

## Support

- E-mail: **lebedev77@gmail.com**
- Telegram: **[@inouter](https://t.me/inouter)**
- Website and FAQ: **[tpms.ivlebedev.ru](https://tpms.ivlebedev.ru)**

---

## Кратко по-русски

**Pajero IV TPMS & Dashboard** — приложение для Android-магнитол и телефонов: давление и температура в шинах со штатного блока TPMS, температура масла АКПП и ОЖ, вольтметр, бортовой компьютер.

- Нужен адаптер **ELM327 Bluetooth v1.5** на чипе PIC18F25K80 — дешёвые клоны v2.1 не работают.
- Базовая версия — **бесплатно и без ограничений**: мониторинг шин и сброс ошибок TPMS.
- PRO-модули (параметры авто, привязка датчиков) — разовая покупка, лицензия навсегда, до 3 своих устройств, привязка к e-mail, после активации интернет не нужен.
- Скачать: [последний релиз](../../releases/latest) · [RuStore](https://www.rustore.ru/catalog/app/com.pajero4.tpms) · описание и оплата: [tpms.ivlebedev.ru](https://tpms.ivlebedev.ru)
- Поддержка: lebedev77@gmail.com, Telegram [@inouter](https://t.me/inouter)

---

## Legal

Independent software product. Mitsubishi, Pajero, Montero, Shogun, Outlander and MUT-III are trademarks of Mitsubishi Motors Corporation; this application is not affiliated with, sponsored or endorsed by Mitsubishi Motors.

Seller: sole proprietor Ivan V. Lebedev (ИП Лебедев Иван Вениаминович), ОГРНИП 316723200103570, ИНН 890507421407, Tyumen, Russia. The public offer, privacy policy and digital goods delivery terms are published on [tpms.ivlebedev.ru](https://tpms.ivlebedev.ru).
