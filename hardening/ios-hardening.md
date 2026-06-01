# Panduan Penguatan iOS

> Terakhir Diperbarui: 2026-06-01

Untuk daftar periksa lengkap (40+ item), lihat [Daftar Periksa Penguatan iOS](../checklists/ios-hardening-checklist.md).

---

## 1. Kode Sandi dan Face ID / Touch ID

**Konfigurasi kode sandi yang direkomendasikan:**

| Opsi | Keamanan | Pengaturan |
|---|---|---|
| 4 digit | ❌ Lemah | Jangan gunakan |
| 6 digit | ✅ Minimum | Pengaturan > Face ID & Kode Sandi > Ubah Kode Sandi > Kode Numerik Kustom |
| Alfanumerik | ✅✅ Terbaik | Pengaturan > Face ID & Kode Sandi > Kode Alfanumerik Kustom |

**Face ID:**
- Aktifkan untuk: Buka kunci, App Store, Apple Pay, Isi Otomatis Kata Sandi
- Aktifkan "Perlu Perhatian": Wajah harus menatap layar, mencegah buka kunci saat tertidur

**Auto-Lock:** Atur ke **30 detik** (Pengaturan > Layar & Kecerahan > Kunci Otomatis)

---

## 2. Perlindungan Perangkat Dicuri (iOS 17.3+)

Fitur ini adalah salah satu peningkatan keamanan terpenting di iOS:

- Memblokir akses ke kata sandi dan pengaturan kritis **tanpa biometrik** saat jauh dari lokasi familiar
- Memberlakukan **penundaan 1 jam** untuk perubahan akun kritis
- Melindungi terhadap serangan shoulder surfing + pencurian

**Aktifkan:** Pengaturan > Face ID & Kode Sandi > Perlindungan Perangkat Dicuri

Panduan lengkap: [Perlindungan Perangkat Dicuri](../ios/stolen-device-protection.md)

---

## 3. Find My

**Konfigurasi wajib:**
- Find My iPhone: **Aktif**
- Aktifkan Pencarian Offline: **Aktif** (melacak tanpa internet)
- Kirim Lokasi Terakhir: **Aktif** (kirim lokasi sebelum baterai habis)

**Verifikasi:** Buka https://icloud.com/find — pastikan perangkat Anda terlihat.

---

## 4. Keamanan Apple ID

Apple ID adalah identitas utama iOS — keamanannya sama pentingnya dengan perangkat:

- 2FA: **Wajib aktif**
- Kunci Pemulihan: Buat dan simpan secara offline (fisik)
- Kontak Pemulihan: Tunjuk 1-2 orang tepercaya
- Nomor telepon tepercaya: Gunakan nomor yang bukan di perangkat yang mungkin hilang

Panduan lengkap: [Pemulihan Apple ID](../ios/apple-id-recovery.md)

---

## 5. Screen Time sebagai Lapisan Keamanan Tambahan

Screen Time bukan hanya untuk pembatasan anak — ini adalah lapisan keamanan tambahan:

```
Aktifkan Screen Time dengan kode sandi BERBEDA dari kode sandi perangkat

Kemudian aktifkan pembatasan:
├── Perubahan Kode Sandi: "Jangan Izinkan"
├── Perubahan Akun: "Jangan Izinkan"
└── Perubahan Layanan Lokasi: "Jangan Izinkan Perubahan"
```

Ini mencegah pencuri yang tahu kode sandi perangkat untuk mengubah pengaturan kritis.

---

## 6. Privasi Aplikasi

**Audit berkala (setiap 3 bulan):**
- Pengaturan > Privasi & Keamanan > Laporan Privasi Aplikasi — aktifkan untuk memantau penggunaan aktual
- Tinjau izin lokasi: ubah "Selalu" ke "Saat Menggunakan" untuk semua aplikasi non-esensial
- Tinjau akses mikrofon, kamera, dan kontak

---

## 7. Mode Penguncian (Lockdown Mode) — Untuk Pengguna Berisiko Tinggi

Mode Penguncian adalah perlindungan ekstrem untuk:
- Jurnalis dan aktivis
- Eksekutif tingkat tinggi
- Peneliti keamanan yang menjadi target

**Efek Mode Penguncian:**
- Menonaktifkan attachment pesan (kecuali gambar)
- Memblokir panggilan FaceTime dari kontak tidak dikenal
- Menonaktifkan browsing fitur web yang kompleks
- Memblokir aksesori USB saat terkunci
- Membatasi koneksi ke jaringan Wi-Fi yang belum pernah digunakan

**Aktifkan:** Pengaturan > Privasi & Keamanan > Mode Penguncian

*Referensi: https://support.apple.com/en-us/105120*

---

## 8. Keamanan Safari dan Browsing

- Fraudulent Website Warning: **Aktif**
- Prevent Cross-Site Tracking: **Aktif**
- Hide IP Address: **Dari Pelacak**
- iCloud Private Relay (iCloud+): Aktifkan untuk menyembunyikan IP dari semua situs

---

## Dokumen Terkait

- [Daftar Periksa Penguatan iOS](../checklists/ios-hardening-checklist.md)
- [Find My](../ios/find-my.md)
- [Perlindungan Perangkat Dicuri](../ios/stolen-device-protection.md)
- [Keamanan SIM](sim-security.md)

---

*Terakhir Diperbarui: 2026-06-01 | Referensi: https://support.apple.com/guide/security/welcome/web*
