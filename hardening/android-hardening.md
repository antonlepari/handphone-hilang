# Panduan Penguatan Android

> Terakhir Diperbarui: 2026-06-01

Untuk daftar periksa lengkap (40+ item), lihat [Daftar Periksa Penguatan Android](../checklists/android-hardening-checklist.md).

---

## 1. Keamanan Kunci Layar

**PIN vs. Pola vs. Kata Sandi:**

| Jenis | Keamanan | Rekomendasi |
|---|---|---|
| Geser | Tidak ada | ❌ Tidak digunakan |
| Pola | Rendah (meninggalkan jejak minyak) | ❌ Hindari |
| PIN 4 digit | Rendah (10.000 kombinasi) | ❌ Hindari |
| PIN 6 digit | Sedang (1 juta kombinasi) | ✅ Minimum |
| PIN 8+ digit | Tinggi | ✅ Direkomendasikan |
| Alfanumerik | Sangat tinggi | ✅✅ Terbaik |

**Konfigurasi:**
- Pengaturan > Keamanan > Kunci layar
- Batas waktu kunci: **30 detik**
- Kunci segera setelah layar mati: **Aktif**

---

## 2. Biometrik

Biometrik nyaman tetapi memiliki kelemahan:
- Sidik jari: Aman, tetapi bisa dipaksa secara fisik
- Pengenalan wajah 2D: **Tidak aman** — bisa ditipu dengan foto
- Pengenalan wajah 3D (IR + depth): Lebih aman

**Rekomendasi:**
- Gunakan sidik jari sebagai biometrik utama
- Aktifkan Identity Check (Android 15+) untuk memblokir fallback PIN di luar rumah
- Nonaktifkan "Bangunkan layar untuk buka kunci wajah" pada perangkat dengan kamera 2D biasa

---

## 3. Find Hub dan Anti-Pencurian

**Aktifkan semua lapisan perlindungan:**

```
Find Hub (Pelacakan) ─────────────────── Aktifkan
Pencarian Offline ────────────────────── Aktifkan
Kunci Deteksi Pencurian (AI) ────────── Aktifkan (Android 10+)
Kunci Perangkat Offline ─────────────── Aktifkan (Android 10+)
Kunci Jarak Jauh via SMS ────────────── Aktifkan (Android 10+)
Identity Check ──────────────────────── Aktifkan (Android 15+)
```

**Verifikasi:** Masuk ke https://android.com/find dari browser lain dan pastikan perangkat Anda terlihat.

---

## 4. Keamanan Akun Google

Akun Google adalah kunci utama Android. Penguatannya sama pentingnya dengan perangkat:

- 2FA dengan aplikasi autentikator (bukan SMS)
- Tinjau perangkat tepercaya setiap 3 bulan
- Simpan kode cadangan offline
- Gunakan email pemulihan dari provider berbeda (bukan Gmail)
- Pertimbangkan Program Perlindungan Lanjutan Google untuk pengguna berisiko tinggi

Panduan lengkap: [Keamanan Akun Google](../android/google-account-security.md)

---

## 5. Manajemen Izin Aplikasi

**Prinsip least privilege** — berikan izin minimal yang diperlukan:

| Izin | Siapa yang Butuh | Yang Tidak Perlu |
|---|---|---|
| Lokasi "Selalu" | Maps, Ride-sharing | Media sosial, game |
| Mikrofon | WhatsApp, telepon | Kalkulator, cuaca |
| Kamera | Kamera, video call | Browser, kalender |
| Kontak | Pesan, telepon | Game, utilitas |

**Audit berkala:** Pengaturan > Privasi > Manajer Izin — tinjau setiap 3 bulan.

---

## 6. Keamanan Jaringan

- **Wi-Fi MAC acak**: Aktifkan per jaringan (Android 10+) untuk mencegah pelacakan
- **DNS Pribadi**: Gunakan dns.google atau 1dot1dot1dot1.cloudflare-dns.com
- **VPN**: Gunakan saat terhubung ke Wi-Fi publik (Mullvad, ProtonVPN)
- **Bluetooth**: Nonaktifkan saat tidak digunakan
- **Jangan** auto-connect ke Wi-Fi publik terbuka

---

## 7. Opsi Pengembang

> **⚠️** Nonaktifkan semua opsi berikut jika Anda bukan pengembang:

- USB Debugging: **Nonaktif**
- OEM Unlocking: **Nonaktif** (jika diaktifkan, memungkinkan bypass FRP)
- Lokasi Palsu: **Nonaktif**
- Opsi Pengembang (keseluruhan): **Nonaktif**

---

## 8. Samsung Knox (Khusus Samsung)

Untuk pengguna Samsung Galaxy, aktifkan perlindungan tambahan:

- **Samsung Knox**: Aktif secara default di Samsung Galaxy
- **Find My Mobile**: Aktifkan sebagai redundansi Find Hub
- **Reactivation Lock**: Aktifkan di Pengaturan > Biometrik dan Keamanan > Find My Mobile
- **Secure Folder**: Untuk data sangat sensitif

*Referensi: https://www.samsungknox.com*

---

## Dokumen Terkait

- [Daftar Periksa Penguatan Android](../checklists/android-hardening-checklist.md)
- [Find Hub](../android/find-my-device.md)
- [Pemeriksaan Identitas](../android/identity-check.md)
- [Keamanan SIM](sim-security.md)

---

*Terakhir Diperbarui: 2026-06-01 | Referensi: https://source.android.com/docs/security*
