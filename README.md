# Panduan Respons Kehilangan & Pencurian Perangkat Mobile

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Platform: Android](https://img.shields.io/badge/Platform-Android-green.svg)
![Platform: iOS](https://img.shields.io/badge/Platform-iOS-blue.svg)
![Terakhir Diperbarui](https://img.shields.io/badge/Terakhir%20Diperbarui-2026--06--01-brightgreen)
![OWASP](https://img.shields.io/badge/Referensi-OWASP%20%7C%20NIST%20%7C%20CISA-red)

> **Panduan open-source paling lengkap untuk merespons smartphone yang hilang atau dicuri — mencakup mitigasi, pencegahan, respons insiden, pemulihan, dan penguatan keamanan untuk Android dan iOS.**

---

## Untuk Siapa Repositori Ini

| Pengguna | Cara Menggunakan Repositori Ini |
|---|---|
| **Pengguna Umum** | Mulai dengan [Daftar Darurat](checklists/emergency-checklist.md) dan [Pencegahan Sebelum Kehilangan](checklists/before-loss-prevention.md) |
| **Profesional Keamanan** | Lihat [Model Ancaman](threat-models/) dan [Playbook Respons Insiden](incident-response/) |
| **Analis SOC** | Lihat [Respons Perangkat Korporat](incident-response/corporate-device-response.md) dan [Matriks Risiko](threat-models/risk-matrix.md) |
| **Praktisi Forensik Digital** | Lihat [Alat](tools/recommended-tools.md) dan [Skenario Serangan](threat-models/attack-scenarios.md) |
| **Administrator IT** | Lihat [MDM & Enterprise](hardening/mdm-enterprise.md) dan [Panduan Penguatan Android/iOS](hardening/) |
| **Tim Korporat** | Lihat [Template Laporan Insiden](templates/incident-report-template.md) dan [Respons Perangkat Korporat](incident-response/corporate-device-response.md) |
| **Mahasiswa & Peneliti** | Lihat [Lanskap Ancaman](docs/threat-landscape.md), [Referensi](references/), dan [Terminologi](docs/terminology.md) |

---

## Daftar Periksa Darurat — Mulai Cepat

> **⚠️ PERINGATAN:** Jika perangkat Anda baru saja hilang atau dicuri, lakukan 5 tindakan ini segera — secara berurutan.

1. **Buka Find My Device / Find My** di komputer atau ponsel lain dan periksa lokasi terakhir yang diketahui
2. **Aktifkan Mode Hilang / Kunci Jarak Jauh** untuk menampilkan informasi kontak Anda dan mencegah akses tidak sah
3. **Keluar dari semua sesi aktif** dari Akun Google atau Apple ID Anda melalui browser web
4. **Hubungi operator seluler Anda** untuk menangguhkan kartu SIM dan mencegah panggilan, SMS, dan penggunaan data yang tidak sah
5. **Ubah kata sandi terpenting Anda** — email terlebih dahulu, lalu perbankan — dari perangkat tepercaya

Untuk prosedur darurat lengkap, lihat [Daftar Periksa Darurat](checklists/emergency-checklist.md) dan [5 Menit Pertama](incident-response/first-5-minutes.md).

---

## Tujuan & Ruang Lingkup Repositori

Repositori ini mendokumentasikan semua yang perlu Anda ketahui tentang kejadian kehilangan smartphone — sebelum terjadi, saat kejadian, dan sesudahnya. Mencakup:

- **Pencegahan**: Penguatan keamanan sebelum kejadian kehilangan terjadi
- **Respons Insiden**: Prosedur langkah demi langkah dari 5 menit pertama hingga minggu pertama
- **Pemulihan**: Memulihkan akun, data, dan kepercayaan setelah kehilangan atau pencurian perangkat
- **Intelijen Ancaman**: Skenario serangan yang dipetakan ke MITRE ATT&CK Mobile Matrix
- **Panduan Enterprise**: Kebijakan perangkat korporat dan pertimbangan MDM
- **Alat Forensik**: Alat profesional untuk praktisi forensik digital

Ini adalah dokumen yang terus berkembang, dikelola dengan referensi ke dokumentasi vendor resmi (Apple, Google, Samsung), NIST, OWASP, CISA, ENISA, dan MITRE ATT&CK.

---

## Daftar Isi

### Dokumentasi
- [Ikhtisar](docs/overview.md)
- [Lanskap Ancaman](docs/threat-landscape.md)
- [Terminologi](docs/terminology.md)

### Android
- [Ikhtisar Android](android/README.md)
- [Find Hub (sebelumnya Find My Device)](android/find-my-device.md)
- [Perlindungan Reset Pabrik (FRP)](android/factory-reset-protection.md)
- [Keamanan Akun Google](android/google-account-security.md)
- [Play Protect](android/play-protect.md)
- [Pemeriksaan Identitas](android/identity-check.md)

### iOS
- [Ikhtisar iOS](ios/README.md)
- [Find My](ios/find-my.md)
- [Mode Hilang](ios/lost-mode.md)
- [Kunci Aktivasi](ios/activation-lock.md)
- [Perlindungan Perangkat Dicuri](ios/stolen-device-protection.md)
- [Pemulihan Apple ID](ios/apple-id-recovery.md)

### Daftar Periksa
- [Ikhtisar Daftar Periksa](checklists/README.md)
- [Sebelum Kehilangan — Daftar Periksa Pencegahan](checklists/before-loss-prevention.md)
- [Daftar Periksa Penguatan Android](checklists/android-hardening-checklist.md)
- [Daftar Periksa Penguatan iOS](checklists/ios-hardening-checklist.md)
- [Daftar Periksa Darurat](checklists/emergency-checklist.md)

### Respons Insiden
- [Ikhtisar Respons Insiden](incident-response/README.md)
- [Ikhtisar Playbook & Diagram Alur](incident-response/playbook-overview.md)
- [5 Menit Pertama](incident-response/first-5-minutes.md)
- [30 Menit Pertama](incident-response/first-30-minutes.md)
- [Jam Pertama](incident-response/first-hour.md)
- [24 Jam Pertama](incident-response/first-24-hours.md)
- [Minggu Pertama](incident-response/first-week.md)
- [Respons Perangkat Korporat](incident-response/corporate-device-response.md)

### Penguatan Keamanan
- [Ikhtisar Penguatan](hardening/README.md)
- [Panduan Penguatan Android](hardening/android-hardening.md)
- [Panduan Penguatan iOS](hardening/ios-hardening.md)
- [Keamanan SIM](hardening/sim-security.md)
- [MDM & Enterprise](hardening/mdm-enterprise.md)

### Model Ancaman
- [Ikhtisar Model Ancaman](threat-models/README.md)
- [Ikhtisar Model Ancaman](threat-models/threat-model-overview.md)
- [Skenario Serangan](threat-models/attack-scenarios.md)
- [Matriks Risiko](threat-models/risk-matrix.md)

### Alat
- [Ikhtisar Alat](tools/README.md)
- [Alat yang Direkomendasikan](tools/recommended-tools.md)

### Referensi
- [Ikhtisar Referensi](references/README.md)
- [Kutipan](references/citations.md)

### Template
- [Ikhtisar Template](templates/README.md)
- [Template Laporan Insiden](templates/incident-report-template.md)
- [Template Laporan Polisi](templates/police-report-template.md)
- [Template Notifikasi Operator](templates/carrier-notification-template.md)

---

## Kontribusi

Kontribusi sangat disambut. Untuk berkontribusi:

1. Fork repositori ini
2. Buat cabang fitur: `git checkout -b fitur/kontribusi-anda`
3. Lakukan perubahan mengikuti struktur dokumen yang ada
4. Pastikan semua referensi berasal dari sumber resmi dan otoritatif
5. Kirim pull request dengan deskripsi yang jelas

Jangan menambahkan statistik yang tidak terverifikasi, klaim yang bias terhadap vendor, atau tautan ke sumber tidak resmi/tidak andal.

---

## Lisensi

Repositori ini dilisensikan di bawah **Lisensi MIT**. Lihat [LICENSE](LICENSE) untuk detailnya.

Anda bebas menggunakan, memodifikasi, dan mendistribusikan konten ini dengan atribusi.

---

*Terakhir Diperbarui: 2026-06-01 | Dikelola oleh komunitas keamanan open-source*
