# Pemeriksaan Identitas — Android

> Terakhir Diperbarui: 2026-06-01

## Ikhtisar

**Pemeriksaan Identitas** adalah fitur keamanan Android yang memerlukan **autentikasi biometrik** (sidik jari atau pemindaian wajah) — tanpa fallback kode sandi atau PIN — untuk mengakses pengaturan dan data perangkat yang sensitif ketika perangkat berada **di luar lokasi tepercaya** (seperti rumah atau kantor Anda).

Pemeriksaan Identitas diperkenalkan oleh Google pada Januari 2025 dan awalnya diluncurkan ke **perangkat Pixel yang menjalankan Android 15** dan **perangkat Samsung Galaxy yang menjalankan One UI 7**. Ketersediaan Android yang lebih luas diumumkan untuk akhir 2025.

> **ℹ️ CATATAN:** Pemeriksaan Identitas secara konseptual mirip dengan Perlindungan Perangkat Dicuri Apple (iOS 17.3+). Kedua fitur mencegah pencuri yang telah mencuri perangkat beserta kode sandi yang diamati untuk melakukan perubahan keamanan kritis.

*Referensi: https://support.google.com/pixelphone/answer/9463625*

---

## Mengapa Pemeriksaan Identitas Penting

### Rantai Serangan Pencurian Kode Sandi

Sebelum Pemeriksaan Identitas, serangan berikut memungkinkan:

1. Penyerang mengamati korban memasukkan PIN di tempat umum (shoulder surfing)
2. Penyerang mencuri perangkat yang terkunci atau terbuka
3. Penyerang menggunakan PIN yang diamati untuk membuka kunci perangkat
4. Penyerang membuka Pengaturan dan mengubah biometrik ke wajah/sidik jarinya sendiri
5. Penyerang menonaktifkan Find My Device
6. Penyerang mengakses Google Password Manager dan mengekspor semua kredensial
7. Penyerang menggunakan kredensial untuk mengambil alih email, perbankan, dan akun lainnya

**Pemeriksaan Identitas memutus langkah 4 dan langkah 6-7**: di luar lokasi tepercaya, PIN tidak lagi cukup — biometrik diperlukan tanpa fallback. Pencuri yang memiliki PIN tetapi tidak memiliki sidik jari atau wajah pemilik tidak dapat mengubah pengaturan keamanan atau mengakses kata sandi.

---

## Cara Kerja Pemeriksaan Identitas

### Lokasi Tepercaya

Pemeriksaan Identitas menggunakan lokasi perangkat untuk menentukan konteks:

- **Lokasi tepercaya** (ditentukan oleh pengguna): Rumah, kantor, atau tempat familiar lainnya di mana pengguna secara teratur menggunakan perangkat. Keamanan yang dilonggarkan berlaku — PIN dapat digunakan seperti biasa.
- **Lokasi tidak tepercaya/tidak familiar** (semua tempat lain): Keamanan yang ditingkatkan berlaku — biometrik diperlukan untuk tindakan sensitif, tanpa fallback kode sandi.

### Apa yang Memerlukan Biometrik di Luar Lokasi Tepercaya

Ketika Pemeriksaan Identitas diaktifkan dan perangkat berada di luar lokasi tepercaya, **autentikasi biometrik eksplisit** diperlukan untuk:

| Tindakan yang Dilindungi | Detail |
|---|---|
| Akses kata sandi dan passkey yang tersimpan | Konten Google Password Manager |
| Isi otomatis kata sandi di aplikasi | Dari Google Password Manager (kecuali Chrome) |
| Ubah PIN atau kata sandi kunci layar | Mencegah perubahan PIN oleh penyerang |
| Ubah biometrik (sidik jari/wajah) | Mencegah penyerang mendaftarkan biometrik mereka |
| Reset pabrik | Mencegah penghancuran data atau upaya bypass |
| Matikan Find My Device | Mencegah penonaktifan pelacakan lokasi |
| Matikan fitur perlindungan pencurian | Termasuk Pemeriksaan Identitas itu sendiri |

*Sumber: The Hacker News, Januari 2025 — https://thehackernews.com/2025/01/androids-new-identity-check-feature.html*

---

## Persyaratan

Untuk mengaktifkan Pemeriksaan Identitas:

- [ ] Perangkat: Google Pixel yang menjalankan **Android 15** atau Samsung Galaxy yang menjalankan **One UI 7**
- [ ] Play Services: Versi stabil terbaru terinstal
- [ ] Biometrik: Buka kunci wajah atau pemindai sidik jari terdaftar di perangkat
- [ ] Kunci layar: PIN, kata sandi, atau pola dikonfigurasi
- [ ] Lokasi: Layanan Lokasi diaktifkan (untuk deteksi lokasi tepercaya)
- [ ] Find My Device: Harus diaktifkan

---

## Cara Mengaktifkan Pemeriksaan Identitas (Pixel)

1. Buka **Pengaturan**
2. Ketuk **Keamanan & privasi** atau **Keamanan**
3. Ketuk **Keamanan & privasi lainnya**
4. Ketuk **Pemeriksaan Identitas**
5. Aktifkan **Pemeriksaan Identitas** ke **Aktif**
6. Ikuti petunjuk untuk mengonfirmasi autentikasi biometrik Anda
7. Opsional: Tambahkan lokasi tepercaya

### Menambahkan Lokasi Tepercaya

1. Dalam pengaturan Pemeriksaan Identitas, ketuk **Tambah lokasi tepercaya**
2. Perangkat akan menggunakan lokasi Anda saat ini (pastikan GPS akurat)
3. Beri nama lokasi (mis., "Rumah," "Kantor")
4. Konfirmasi

> **💡 TIPS:** Hanya tambahkan lokasi di mana Anda benar-benar menggunakan perangkat secara teratur dan di mana Anda memiliki ekspektasi keamanan yang wajar. Menambahkan terlalu banyak lokasi tepercaya mengurangi nilai perlindungan fitur ini.

---

## Cara Mengaktifkan Pemeriksaan Identitas (Samsung Galaxy)

Perangkat Samsung Galaxy yang menjalankan **One UI 7** memiliki Pemeriksaan Identitas di jalur yang sedikit berbeda:

1. Buka **Pengaturan**
2. Ketuk **Keamanan dan privasi**
3. Ketuk **Pengaturan keamanan lainnya**
4. Ketuk **Pemeriksaan Identitas**
5. Aktifkan fitur dan konfirmasi biometrik

*Referensi: Dokumentasi keamanan Samsung Knox — https://security.samsungmobile.com*

---

## Tambahan Android 16

Perangkat yang menjalankan **Android 16** mendapatkan kontrol tambahan:

**Kunci Autentikasi Gagal**: Perangkat secara otomatis terkunci setelah beberapa upaya autentikasi yang gagal. Sakelar khusus di Pengaturan memungkinkan pengguna mengontrol perilaku ini. Ini melengkapi Pemeriksaan Identitas dengan mencegah upaya PIN brute-force.

---

## Perbandingan: Pemeriksaan Identitas vs. Perlindungan Perangkat Dicuri

| Fitur | Pemeriksaan Identitas (Android 15+) | Perlindungan Perangkat Dicuri (iOS 17.3+) |
|---|---|---|
| Platform | Android (Pixel, Samsung, kemudian lebih luas) | iOS 17.3+ |
| Kondisi pemicu | Di luar lokasi tepercaya | Jauh dari lokasi familiar |
| Tindakan hanya biometrik | Ya — tanpa fallback kode sandi | Ya — tanpa fallback kode sandi |
| Tindakan keamanan yang ditunda | Tidak (per 2025) | Ya — penundaan 1 jam untuk perubahan kritis |
| Pengaturan yang diperlukan | Biometrik, Lokasi, Find My Device | 2FA, Face/Touch ID, Lokasi Signifikan, Find My |
| Memblokir perubahan biometrik? | Ya | Ya |
| Memblokir penonaktifan Find My Device? | Ya | Ya (melalui penundaan) |

---

## Batasan dan Pertimbangan

| Pertimbangan | Detail |
|---|---|
| **Spoofing biometrik** | Serangan spoofing biometrik tingkat lanjut secara teoritis dapat melewati; selalu perbarui perangkat |
| **Akurasi lokasi** | Lokasi GPS/Wi-Fi harus akurat; lokasi yang tidak tepat dapat memicu dalam konteks yang salah |
| **Akses darurat** | Panggilan darurat dan layanan tetap dapat diakses terlepas dari status Pemeriksaan Identitas |
| **Pendaftaran lokasi tepercaya** | Harus dilakukan saat berada di lokasi tepercaya dengan GPS yang akurat |
| **Dampak baterai dan lokasi** | Memantau lokasi secara terus-menerus untuk konteks Pemeriksaan Identitas memiliki dampak baterai minimal tetapi tidak nol |

---

## Dokumen Terkait

- [Panduan Penguatan Android](../hardening/android-hardening.md)
- [Keamanan Akun Google](google-account-security.md)
- [Find Hub](find-my-device.md)
- [Perlindungan Perangkat Dicuri iOS (perbandingan)](../ios/stolen-device-protection.md)

---

*Terakhir Diperbarui: 2026-06-01 | Sumber: https://support.google.com/pixelphone/answer/9463625 | https://thehackernews.com/2025/01/androids-new-identity-check-feature.html*
