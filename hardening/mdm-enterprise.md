# MDM & Enterprise — Manajemen Perangkat Mobile

> Terakhir Diperbarui: 2026-06-01

## Ikhtisar

Mobile Device Management (MDM) adalah fondasi keamanan perangkat mobile di lingkungan enterprise. MDM memungkinkan IT Administrator mengelola, mengonfigurasi, memantau, dan merespons insiden pada perangkat yang dikelola secara terpusat.

*Referensi: NIST SP 800-124r2 — https://csrc.nist.gov/pubs/sp/800/124/r2/final*

---

## Model Kepemilikan Perangkat

| Model | Kepemilikan | MDM Control | Cocok Untuk |
|---|---|---|---|
| **COPE** (Corporate-Owned, Personally Enabled) | Perusahaan | Penuh | Karyawan yang butuh fleksibilitas |
| **COBO** (Corporate-Owned, Business Only) | Perusahaan | Penuh | Perangkat khusus kerja |
| **CYOD** (Choose Your Own Device) | Perusahaan | Penuh | Karyawan dengan preferensi perangkat |
| **BYOD** (Bring Your Own Device) | Karyawan | Parsial (profil kerja) | Startup, perusahaan kecil |

---

## Solusi MDM Utama

### Microsoft Intune

Platform MDM/MAM berbasis cloud dari Microsoft, terintegrasi penuh dengan ekosistem Microsoft 365.

**Kemampuan utama:**
- Remote wipe (full device atau corporate data saja)
- Compliance policies — enforcement kebijakan keamanan
- Conditional Access — blokir akses jika perangkat tidak comply
- App deployment dan manajemen
- Windows, Android, dan iOS

*Referensi: https://learn.microsoft.com/en-us/mem/intune/fundamentals/what-is-intune*

### Apple Business Manager + MDM

**Apple Business Manager (ABM)** adalah portal web Apple untuk organisasi yang mengelola perangkat Apple:

- Zero-touch deployment — perangkat baru langsung terdaftar ke MDM
- Managed Apple IDs untuk karyawan
- Manajemen aplikasi dan konten
- Kunci Aktivasi dikelola oleh organisasi (bukan akun individu)

*Referensi: https://support.apple.com/guide/apple-business-manager/welcome/web*

### Android Enterprise

Program Google untuk manajemen perangkat Android di enterprise:

**Mode deployment:**
- **Work Profile** (BYOD): Profil kerja terpisah di perangkat pribadi
- **Fully Managed**: Kontrol penuh atas perangkat korporat
- **Dedicated Device**: Kiosk mode untuk perangkat satu fungsi

*Referensi: https://androidenterprisepartners.withgoogle.com*

---

## Kebijakan Keamanan MDM Minimum

Untuk perangkat yang mengakses data korporat, terapkan kebijakan minimum berikut:

```
KEBIJAKAN MINIMUM YANG DIREKOMENDASIKAN:

Autentikasi:
├── PIN minimum 6 digit atau biometrik
├── Batas waktu kunci layar: 5 menit
└── Enkripsi perangkat: Wajib

Akses Jaringan:
├── VPN wajib untuk akses sumber daya internal
└── Batasi jaringan Wi-Fi yang diizinkan

Aplikasi:
├── Izinkan hanya aplikasi dari daftar yang disetujui
└── Blokir instalasi dari sumber tidak dikenal

Respons Insiden:
├── Remote wipe: Aktifkan
├── Remote lock: Aktifkan
└── Geolocation: Aktifkan (untuk perangkat yang hilang)
```

---

## Remote Wipe via MDM

MDM memungkinkan dua jenis remote wipe:

| Jenis | Deskripsi | Kapan Digunakan |
|---|---|---|
| **Full Wipe** | Hapus semua data, kembalikan ke pengaturan pabrik | Perangkat COPE/COBO hilang atau dicuri |
| **Selective Wipe** | Hapus hanya data dan aplikasi korporat | BYOD — proteksi data korporat tanpa menghapus data pribadi |

> **ℹ️ CATATAN:** Untuk perangkat BYOD, **Selective Wipe** adalah pilihan yang lebih tepat secara hukum dan etika, karena tidak menghapus foto, kontak, dan data pribadi karyawan.

---

## Respons Insiden dengan MDM

Ketika perangkat korporat dilaporkan hilang:

```
IT Security menerima laporan
├── Verifikasi identitas pelapor
├── Cek status perangkat di konsol MDM
│   ├── Terakhir check-in: kapan?
│   ├── Lokasi terakhir (jika diaktifkan)
│   └── Status compliance
├── Kirim remote lock segera
├── Cabut akses VPN dan email
├── Buat keputusan: Selective Wipe atau Full Wipe
│   ├── Ada data sensitif: Full Wipe
│   └── BYOD: Selective Wipe
└── Dokumentasikan semua tindakan untuk audit
```

---

## Dokumen Terkait

- [Respons Perangkat Korporat](../incident-response/corporate-device-response.md)
- [Panduan Penguatan Android](android-hardening.md)
- [Panduan Penguatan iOS](ios-hardening.md)

---

*Terakhir Diperbarui: 2026-06-01 | Referensi: NIST SP 800-124r2, https://learn.microsoft.com/en-us/mem/intune*
