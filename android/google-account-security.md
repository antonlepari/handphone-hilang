# Keamanan Akun Google

> Terakhir Diperbarui: 2026-06-01

## Ikhtisar

Akun Google Anda adalah kunci utama perangkat Android Anda. Ini mengendalikan:
- Find Hub (pelacakan perangkat dan penghapusan jarak jauh)
- Cadangan perangkat dan pemulihan
- Google Drive, Gmail, Google Foto
- Pembelian Play Store dan instalasi aplikasi
- Sinkronisasi Chrome (kata sandi tersimpan, bookmark)
- Perlindungan Reset Pabrik (FRP)

Jika penyerang mendapatkan akses ke Akun Google Anda, mereka dapat menonaktifkan Find Hub, melakukan penghapusan jarak jauh, mengakses cadangan Anda, dan memulihkan semua kredensial tersimpan. **Mengamankan Akun Google Anda sama pentingnya dengan mengamankan perangkat itu sendiri.**

*Referensi: https://support.google.com/accounts/answer/46892*

---

## Autentikasi Dua Faktor (2FA)

### Mengaktifkan 2FA

1. Buka **https://myaccount.google.com/security**
2. Di bawah "Cara Anda masuk ke Google," klik **Verifikasi 2 Langkah**
3. Klik **Mulai** dan ikuti petunjuknya
4. Pilih faktor kedua Anda (lihat opsi di bawah)

### Perbandingan Metode 2FA

| Metode | Tingkat Keamanan | Ketahanan terhadap SIM Swap | Direkomendasikan? |
|---|---|---|---|
| **Kunci Keamanan Perangkat Keras** (YubiKey, Titan) | Tertinggi | Ya — kepemilikan fisik diperlukan | Sangat direkomendasikan |
| **Google Prompt** (notifikasi perangkat) | Tinggi | Ya — kepemilikan perangkat diperlukan | Direkomendasikan |
| **Aplikasi Autentikator** (TOTP) | Tinggi | Ya — seed aplikasi offline | Direkomendasikan |
| **Kode Cadangan** | Sedang | Ya | Hanya untuk cadangan darurat |
| **SMS / Panggilan Telepon** | Rendah | Tidak — rentan terhadap SIM swap | Tidak direkomendasikan sebagai utama |

> **⚠️ PERINGATAN:** 2FA berbasis SMS (menerima kode melalui pesan teks) adalah faktor kedua yang paling lemah. Serangan SIM swap dapat menyadap kode SMS. Jika Anda menggunakan 2FA SMS di Akun Google, serangan SIM swap memungkinkan penyerang mengambil alih akun Anda — dan karenanya perangkat Anda — dari jarak jauh.

### Beralih dari 2FA SMS

1. Buka **https://myaccount.google.com/two-step-verification**
2. Daftarkan kunci perangkat keras atau aplikasi autentikator terlebih dahulu
3. Hapus SMS sebagai metode 2FA

---

## Opsi Pemulihan

Opsi pemulihan adalah mekanisme yang digunakan Google untuk memverifikasi identitas Anda jika Anda terkunci. Itu juga merupakan mekanisme yang dieksploitasi penyerang jika tidak diamankan.

### Email Pemulihan

1. Buka **https://myaccount.google.com/recovery/email**
2. Tetapkan alamat email pemulihan yang menggunakan **penyedia email yang berbeda**
3. Email pemulihan tersebut juga harus mengaktifkan 2FA
4. Jangan gunakan email pemulihan yang meneruskan ke akun yang sama yang dilindungi

### Nomor Telepon Pemulihan

- Nomor telepon pemulihan memungkinkan pemulihan akun berbasis SMS
- Jika SIM Anda disusupi, begitu pula pemulihan SMS
- Pertimbangkan untuk menghapus nomor telepon pemulihan dan mengandalkan kode pemulihan + kunci perangkat keras
- Jika Anda menyimpan telepon pemulihan, gunakan nomor terpisah yang tidak terkait dengan perangkat yang dicuri

### Kode Pemulihan

1. Buka **https://myaccount.google.com/two-step-verification/backup-codes**
2. Buat kode cadangan
3. Cetak atau tuliskan dan simpan di lokasi fisik yang aman (bukan di cloud atau di perangkat)
4. Setiap kode digunakan sekali; buat set baru setelah menggunakan satu

---

## Perangkat Tepercaya

### Meninjau Perangkat Tepercaya

1. Buka **https://myaccount.google.com/device-activity**
2. Tinjau semua perangkat yang terdaftar
3. Hapus perangkat yang tidak dikenal atau lama dengan mengklik nama perangkat dan memilih **Keluar**

> **💡 TIPS:** Setelah perangkat hilang atau dicuri, segera keluar dari halaman ini. Ini mencegah perangkat digunakan untuk melewati prompt 2FA akun Google.

---

## Sesi Aktif

### Meninjau dan Mencabut Sesi

1. Buka **https://myaccount.google.com/security**
2. Gulir ke "Perangkat Anda"
3. Pilih **Kelola semua perangkat**
4. Untuk setiap perangkat yang tidak dikenal atau hilang: klik dan pilih **Keluar**

Untuk penghentian sesi jarak jauh segera:
1. Buka **https://myaccount.google.com/notifications** untuk meninjau aktivitas terkini

---

## Pengelola Kata Sandi Google

### Memeriksa Kata Sandi yang Tersimpan

Jika perangkat Anda dicuri saat tidak terkunci, kata sandi yang tersimpan di Chrome atau pengisian otomatis Android dapat diakses. Segera:

1. Buka **https://passwords.google.com**
2. Tinjau semua kata sandi yang tersimpan
3. Ekspor atau catat kata sandi untuk akun yang juga muncul di riwayat browser perangkat
4. Ubah kata sandi kritis (email, perbankan, akun kerja) segera

### Menghapus Kata Sandi yang Tersimpan dari Jarak Jauh

Kata sandi di Google Password Manager disinkronkan dengan cloud. Anda tidak dapat langsung menghapusnya dari pengelola kata sandi dari jarak jauh, tetapi Anda dapat:
1. Mengubah kata sandi untuk akun kritis (membuat versi yang tersimpan tidak berlaku)
2. Mengaktifkan Pemeriksaan Identitas (Android 15+) yang memerlukan biometrik untuk mengakses kata sandi yang tersimpan

---

## Pemantauan Aktivitas Akun Google

### Pemeriksaan Keamanan

1. Buka **https://myaccount.google.com/security-checkup**
2. Tinjau semua item yang ditandai di bawah:
   - Peristiwa keamanan terkini
   - Masuk dan pemulihan
   - Akses pihak ketiga
   - Aplikasi Google dengan akses akun

### Tinjauan Aktivitas Masuk

1. Buka **https://myaccount.google.com/notifications**
2. Tinjau peristiwa masuk terkini, terutama:
   - Masuk perangkat baru
   - Perubahan kata sandi
   - Perubahan opsi pemulihan
   - Perubahan metode 2FA

---

## Program Perlindungan Lanjutan Google

Untuk pengguna berisiko tinggi (eksekutif, jurnalis, politisi, peneliti keamanan), pertimbangkan untuk mendaftar ke **Program Perlindungan Lanjutan Google**:

- Memerlukan kunci keamanan perangkat keras fisik untuk masuk
- Memblokir semua aplikasi tidak sah dari mengakses data Akun Google
- Memberikan perlindungan phishing dan pengambilalihan akun yang lebih kuat
- Membatasi pemulihan akun hanya ke kunci perangkat keras

*Daftar di: https://landing.google.com/advancedprotection/*

---

## Tindakan Segera Pasca-Pencurian

Ketika perangkat dengan Akun Google Anda hilang atau dicuri:

```
SEGERA (5 menit pertama):
1. Buka https://myaccount.google.com/device-activity
2. Keluar dari perangkat yang hilang
3. Buka https://android.com/find
4. Kunci atau hapus perangkat

DALAM 30 MENIT:
5. Ubah kata sandi Akun Google Anda
6. Tinjau dan cabut akses aplikasi OAuth yang tampak mencurigakan
7. Unduh kode cadangan dan simpan secara offline

DALAM 24 JAM:
8. Ubah kata sandi semua akun yang dapat diakses melalui Gmail
9. Periksa email yang diterima/dikirim setelah pencurian
10. Tinjau Google Drive untuk akses atau berbagi file yang tidak terduga
```

---

## Dokumen Terkait

- [Find Hub](find-my-device.md)
- [Perlindungan Reset Pabrik](factory-reset-protection.md)
- [Pemeriksaan Identitas](identity-check.md)
- [5 Menit Pertama](../incident-response/first-5-minutes.md)

---

*Terakhir Diperbarui: 2026-06-01 | Sumber: https://support.google.com/accounts | https://myaccount.google.com/security*
