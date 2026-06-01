# Ikhtisar

> Terakhir Diperbarui: 2026-06-01

## Tujuan

Dokumen ini memberikan pengenalan tentang Panduan Respons Kehilangan & Pencurian Perangkat Mobile — referensi open-source yang komprehensif untuk individu, profesional keamanan, administrator IT, dan tim korporat yang berurusan dengan smartphone yang hilang atau dicuri.

Smartphone bukan lagi sekadar perangkat komunikasi. Mereka adalah brankas kredensial, terminal pembayaran, dokumen identitas, dan kunci akses ke sistem korporat. Kehilangan smartphone — baik secara tidak sengaja maupun melalui pencurian — merupakan insiden keamanan multi-dimensi yang membutuhkan respons terstruktur dan sensitif terhadap waktu.

---

## Ruang Lingkup

Panduan ini mencakup:

- **Perangkat dalam lingkup**: Smartphone Android (Android 10 dan lebih baru), iPhone (iOS 15 dan lebih baru)
- **Jenis pengguna dalam lingkup**: Pengguna pribadi, karyawan bring-your-own-device (BYOD), pengguna perangkat yang dikelola perusahaan
- **Skenario dalam lingkup**: Kehilangan tidak sengaja, pencurian oportunistik, pencurian bertarget, penyitaan perangkat, serangan SIM swap
- **Di luar lingkup**: Insiden khusus tablet (meskipun banyak panduan berlaku), perangkat yang di-jailbreak/rooted dalam konteks enterprise

---

## Cara Membaca Panduan Ini

```
┌───────────────────────────────────────────────────────────────────────────┐
│                   PANDUAN KEHILANGAN PERANGKAT MOBILE                     │
├──────────────────┬──────────────────────────┬─────────────────────────────┤
│  SEBELUM HILANG  │     SELAMA INSIDEN       │       SETELAH HILANG        │
│                  │                          │                             │
│  checklists/     │  incident-response/      │  incident-response/         │
│  before-loss     │  first-5-minutes.md      │  first-24-hours.md          │
│  android/        │  first-30-minutes.md     │  first-week.md              │
│  ios/            │  first-hour.md           │  templates/                 │
│  hardening/      │                          │                             │
└──────────────────┴──────────────────────────┴─────────────────────────────┘
```

### Jika Perangkat Anda Baru Saja Hilang atau Dicuri

Langsung ke [Daftar Periksa Darurat](../checklists/emergency-checklist.md) atau [5 Menit Pertama](../incident-response/first-5-minutes.md).

### Jika Anda Ingin Mencegah Kehilangan di Masa Depan

Baca [Sebelum Kehilangan — Pencegahan](../checklists/before-loss-prevention.md), kemudian panduan penguatan khusus platform untuk [Android](../hardening/android-hardening.md) atau [iOS](../hardening/ios-hardening.md).

### Jika Anda Merespons Insiden Perangkat Korporat

Lihat [Respons Perangkat Korporat](../incident-response/corporate-device-response.md) dan [MDM Enterprise](../hardening/mdm-enterprise.md).

### Jika Anda Peneliti Keamanan atau Praktisi Forensik

Lihat [Lanskap Ancaman](threat-landscape.md), [Skenario Serangan](../threat-models/attack-scenarios.md), dan [Alat yang Direkomendasikan](../tools/recommended-tools.md).

---

## Konsep Kunci

### Dua Fase Keamanan Perangkat

**Penguatan pra-insiden** adalah mitigasi yang paling efektif. Perangkat yang diperkuat dengan benar — dengan PIN kuat, autentikasi biometrik, Find My diaktifkan, PIN SIM diatur, dan 2FA di semua akun — secara dramatis mengurangi risiko dan dampak pencurian.

**Respons pasca-insiden** sangat sensitif terhadap waktu. 5–30 menit pertama setelah kejadian kehilangan adalah jendela paling penting untuk penahanan. Respons yang tertunda secara eksponensial meningkatkan kemungkinan akses akun yang tidak sah, penipuan keuangan, dan eksfiltrasi data.

### Perbedaan Platform

Android dan iOS mengambil pendekatan arsitektur yang berbeda terhadap keamanan perangkat:

| Fitur | Android | iOS |
|---|---|---|
| Pelacakan perangkat | Find Hub (Google) | Find My (Apple) |
| Kunci jarak jauh | Find Hub / Perlindungan Pencurian | Find My / Mode Hilang |
| Hapus jarak jauh | Find Hub | Find My |
| AI anti-pencurian | Kunci Deteksi Pencurian (Android 10+) | Perlindungan Perangkat Dicuri (iOS 17.3+) |
| Perlindungan akun | Keamanan Akun Google | Keamanan Apple ID |
| Kunci aktivasi | Perlindungan Reset Pabrik (FRP) | Kunci Aktivasi |
| Blokir fallback biometrik | Pemeriksaan Identitas (Android 15+) | Perlindungan Perangkat Dicuri |

---

## Standar Referensi

Panduan ini merujuk pada:

- **NIST SP 800-124r2** — Pedoman untuk Mengelola Keamanan Perangkat Mobile di Enterprise (2023)
- **OWASP MASTG** — Panduan Pengujian Keamanan Aplikasi Mobile
- **OWASP MASVS** — Standar Verifikasi Keamanan Aplikasi Mobile
- **CISA** — Panduan dan peringatan Keamanan Perangkat Mobile
- **ENISA** — Rekomendasi Keamanan Smartphone
- **MITRE ATT&CK Mobile Matrix** — Pustaka teknik ancaman

Lihat [Kutipan](../references/citations.md) untuk referensi lengkap.

---

*Terakhir Diperbarui: 2026-06-01*
