# Alat yang Direkomendasikan

> Terakhir Diperbarui: 2026-06-01

---

## 1. Mobile Verification Toolkit (MVT)

| Field | Detail |
|---|---|
| **GitHub** | https://github.com/mvt-project/mvt |
| **Platform** | Android & iOS (dijalankan dari komputer) |
| **Lisensi** | MVT License (non-commercial) |
| **Dikembangkan oleh** | Amnesty International Security Lab |

**Deskripsi:** MVT adalah alat forensik open-source yang dirancang untuk mendeteksi tanda-tanda kompromi perangkat mobile, termasuk spyware canggih seperti Pegasus (NSO Group). MVT menganalisis cadangan perangkat dan artefak sistem untuk menemukan Indicators of Compromise (IOC).

**Kasus Penggunaan:**
- Deteksi spyware dan stalkerware pada perangkat yang dipulihkan
- Analisis forensik cadangan iOS (iTunes backup)
- Pemindaian artefak Android (APK, log sistem)
- Verifikasi integritas perangkat pasca-pencurian

**Kelebihan:**
- Digunakan oleh peneliti keamanan dan jurnalis di seluruh dunia
- Diperbarui secara aktif dengan IOC terbaru
- Mendukung iOS dan Android
- Output terstruktur yang mudah dianalisis

**Keterbatasan:**
- Memerlukan pengetahuan teknis untuk menginterpretasikan hasil
- Tidak dapat mendeteksi spyware yang benar-benar baru (zero-day)
- Analisis iOS memerlukan cadangan lengkap

---

## 2. MobSF (Mobile Security Framework)

| Field | Detail |
|---|---|
| **GitHub** | https://github.com/MobSF/Mobile-Security-Framework-MobSF |
| **Platform** | Android & iOS |
| **Lisensi** | GNU GPL v3 |

**Deskripsi:** MobSF adalah framework pengujian keamanan aplikasi mobile all-in-one yang mendukung analisis statis dan dinamis untuk APK Android dan IPA iOS.

**Kasus Penggunaan:**
- Analisis APK mencurigakan yang ditemukan di perangkat
- Audit keamanan aplikasi sebelum instalasi
- Deteksi permission berbahaya dan perilaku mencurigakan

**Kelebihan:**
- Antarmuka web yang mudah digunakan
- Mendukung analisis batch
- Laporan terstruktur

**Keterbatasan:**
- Memerlukan server atau Docker untuk deployment
- Analisis dinamis memerlukan emulator atau perangkat nyata

---

## 3. Frida

| Field | Detail |
|---|---|
| **GitHub** | https://github.com/frida/frida |
| **Platform** | Android, iOS, Windows, Linux, macOS |
| **Lisensi** | wxWindows Library Licence |

**Deskripsi:** Frida adalah toolkit instrumentasi dinamis yang memungkinkan injeksi JavaScript ke dalam proses native di berbagai platform. Digunakan secara luas dalam penelitian keamanan mobile.

**Kasus Penggunaan:**
- Bypass SSL pinning untuk analisis lalu lintas aplikasi
- Analisis perilaku aplikasi runtime
- Reverse engineering aplikasi mobile
- Deteksi mekanisme anti-analisis

**Kelebihan:**
- Sangat fleksibel dan powerful
- Komunitas dan ekosistem skrip yang besar
- Mendukung banyak platform

**Keterbatasan:**
- Memerlukan perangkat yang di-root (Android) atau di-jailbreak (iOS) untuk penggunaan penuh
- Kurva pembelajaran tinggi
- Beberapa aplikasi mendeteksi dan memblokir Frida

---

## 4. Objection

| Field | Detail |
|---|---|
| **GitHub** | https://github.com/sensepost/objection |
| **Platform** | Android & iOS |
| **Lisensi** | Apache 2.0 |

**Deskripsi:** Objection adalah toolkit eksplorasi runtime mobile yang dibangun di atas Frida, menyederhanakan pengujian keamanan mobile tanpa memerlukan perangkat yang di-jailbreak/rooted.

**Kasus Penggunaan:**
- Eksplorasi sistem file aplikasi
- Bypass root/jailbreak detection
- Dump kredensial dari penyimpanan aman
- Analisis SSL pinning

**Kelebihan:**
- Antarmuka CLI yang ramah pengguna
- Tidak selalu memerlukan root/jailbreak
- Integrasi langsung dengan Frida

**Keterbatasan:**
- Bergantung pada Frida
- Memerlukan pemahaman dasar tentang keamanan mobile

---

## 5. AirGuard

| Field | Detail |
|---|---|
| **GitHub** | https://github.com/seemoo-lab/AirGuard |
| **Platform** | Android & iOS |
| **Lisensi** | GPL v3 |
| **Dikembangkan oleh** | Secure Mobile Networking Lab, TU Darmstadt |

**Deskripsi:** AirGuard adalah aplikasi open-source yang memindai pelacak Bluetooth (AirTag, Tile, dll.) yang tidak dikenal yang mungkin mengikuti Anda tanpa sepengetahuan Anda.

**Kasus Penggunaan:**
- Deteksi pelacak tersembunyi di tas, kendaraan, atau barang pribadi
- Perlindungan anti-stalking
- Audit keamanan fisik

**Kelebihan:**
- Tersedia di Play Store dan App Store
- Berbasis penelitian akademis yang divalidasi
- Mendeteksi berbagai merek pelacak (bukan hanya AirTag)
- Open source dan dapat diaudit

**Keterbatasan:**
- Memerlukan Bluetooth aktif
- Mungkin ada false positive di lingkungan ramai

---

## 6. Android Debug Bridge (ADB)

| Field | Detail |
|---|---|
| **Sumber** | https://developer.android.com/tools/adb |
| **Platform** | Android |
| **Lisensi** | Apache 2.0 (Android SDK) |

**Deskripsi:** ADB adalah alat baris perintah resmi Google yang memungkinkan komunikasi dengan perangkat Android. Digunakan dalam pengembangan, debugging, dan forensik.

**Kasus Penggunaan:**
- Backup dan restore data perangkat
- Instalasi dan penghapusan aplikasi
- Akses shell perangkat
- Pengambilan log sistem untuk forensik

**Kelebihan:**
- Alat resmi dan terdokumentasi dengan baik
- Tersedia di semua platform desktop
- Sangat powerful untuk forensik

**Keterbatasan:**
- Memerlukan USB Debugging diaktifkan (risiko keamanan jika dibiarkan aktif)
- Akses terbatas tanpa root
- Tidak boleh diaktifkan di perangkat produksi

---

## 7. iLEAPP (iOS Logs, Events, And Properties Parser)

| Field | Detail |
|---|---|
| **GitHub** | https://github.com/abrignoni/iLEAPP |
| **Platform** | iOS (dianalisis dari komputer) |
| **Lisensi** | MIT |

**Deskripsi:** iLEAPP adalah parser artefak forensik iOS yang mengekstrak dan menganalisis ratusan jenis artefak dari cadangan iOS dan ekstraksi filesystem.

**Kasus Penggunaan:**
- Forensik iOS untuk investigasi kriminal atau insiden korporat
- Analisis riwayat lokasi, pesan, dan aktivitas aplikasi
- Rekonstruksi timeline kejadian di perangkat iOS

**Kelebihan:**
- Menghasilkan laporan HTML yang mudah dibaca
- Mendukung ratusan artefak
- Diperbarui aktif

**Keterbatasan:**
- Memerlukan cadangan iOS atau ekstraksi filesystem
- Tidak mengenkripsi hasil analisis secara otomatis

---

## 8. ALEAPP (Android Logs Events And Protobuf Parser)

| Field | Detail |
|---|---|
| **GitHub** | https://github.com/abrignoni/ALEAPP |
| **Platform** | Android (dianalisis dari komputer) |
| **Lisensi** | MIT |

**Deskripsi:** ALEAPP adalah rekan Android dari iLEAPP — parser artefak forensik untuk perangkat Android yang menganalisis cadangan, image filesystem, dan ekstraksi data.

**Kasus Penggunaan:**
- Forensik Android
- Analisis artefak Google, WhatsApp, aplikasi media sosial
- Rekonstruksi aktivitas pengguna

**Kelebihan:**
- Laporan HTML komprehensif
- Mendukung banyak aplikasi populer
- Aktif dikembangkan

**Keterbatasan:**
- Memerlukan akses ke data perangkat (cadangan atau ekstraksi)

---

## 9. Autopsy

| Field | Detail |
|---|---|
| **GitHub** | https://github.com/sleuthkit/autopsy |
| **Platform** | Windows, Linux, macOS (analisis dari komputer) |
| **Lisensi** | Apache 2.0 |

**Deskripsi:** Autopsy adalah platform forensik digital open-source berbasis GUI yang mendukung analisis berbagai jenis media digital termasuk perangkat mobile.

**Kasus Penggunaan:**
- Analisis forensik perangkat mobile secara menyeluruh
- Pemulihan file yang terhapus
- Analisis timeline aktivitas
- Investigasi insiden korporat

**Kelebihan:**
- GUI yang ramah pengguna
- Mendukung banyak format media
- Plugin marketplace yang ekstensif
- Digunakan oleh lembaga penegak hukum

**Keterbatasan:**
- Resource intensif (memori dan CPU tinggi)
- Memerlukan akses penuh ke media perangkat

---

## 10. Scrcpy

| Field | Detail |
|---|---|
| **GitHub** | https://github.com/Genymobile/scrcpy |
| **Platform** | Android |
| **Lisensi** | Apache 2.0 |

**Deskripsi:** Scrcpy memungkinkan tampilan dan kontrol perangkat Android dari komputer melalui USB atau Wi-Fi, tanpa instalasi aplikasi di perangkat.

**Kasus Penggunaan:**
- Akses dan kontrol perangkat Android dari komputer (forensik/respons insiden)
- Demonstrasi keamanan
- Backup interaktif data

**Kelebihan:**
- Tidak memerlukan root
- Latensi sangat rendah
- Mendukung Wi-Fi

**Keterbatasan:**
- Memerlukan USB Debugging aktif
- Tidak berfungsi jika layar terkunci (tergantung Android versi)

---

## Catatan Penggunaan

> **⚠️ PERINGATAN:** Alat-alat di atas hanya boleh digunakan pada perangkat yang Anda miliki atau yang Anda memiliki izin tertulis untuk menganalisis. Penggunaan alat forensik tanpa izin pada perangkat orang lain dapat melanggar hukum.

---

*Terakhir Diperbarui: 2026-06-01*
