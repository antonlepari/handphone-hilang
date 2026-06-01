# Find Hub (sebelumnya Find My Device) — Android

> Terakhir Diperbarui: 2026-06-01

## Ikhtisar

**Find Hub** (diganti namanya dari "Find My Device" pada Mei 2025) adalah platform pelacakan dan pemulihan perangkat Google untuk Android. Platform ini menggunakan kombinasi GPS, pemosisian Wi-Fi, triangulasi seluler, dan jaringan Bluetooth berbasis kerumunan dari lebih dari satu miliar perangkat Android untuk menemukan ponsel, tablet, earbud, dan aksesori yang hilang atau dicuri.

> **ℹ️ CATATAN:** Aplikasi ini secara resmi berganti nama dari "Find My Device" menjadi "Find Hub" pada Mei 2025. Kedua nama merujuk pada layanan yang sama. Semua fungsi yang ada dipertahankan selama penggantian nama.

*Referensi: https://android.com/articles/what-is-find-hub-and-how-to-use-it/*

---

## Prasyarat

Sebelum Find Hub dapat membantu Anda memulihkan perangkat, hal-hal berikut harus dikonfigurasi **sebelum** kehilangan:

- [ ] Find Hub diaktifkan pada perangkat
- [ ] Perangkat masuk ke Akun Google
- [ ] Izin lokasi diaktifkan
- [ ] Perangkat memiliki koneksi internet aktif (atau telah berada di dekat perangkat Android lain untuk lokasi offline)
- [ ] Perangkat dihidupkan (atau merupakan Pixel yang didukung untuk pelacakan pasca-mati)

> **⚠️ PERINGATAN:** Jika Find Hub dinonaktifkan sebelum perangkat hilang, Anda tidak akan dapat melacak, mengunci, atau menghapusnya dari jarak jauh. Aktifkan sekarang.

---

## Cara Mengaktifkan Find Hub

### Di Perangkat Android Anda

1. Buka **Pengaturan**
2. Ketuk **Keamanan** (atau **Keamanan & privasi** di beberapa perangkat)
3. Ketuk **Find My Device** atau **Find Hub**
4. Aktifkan **Gunakan Find My Device** ke **Aktif**
5. Konfirmasi lokasi diaktifkan: ketuk **Lokasi** dan pastikan disetel ke **Aktif**

Atau: **Pengaturan > Google > Find My Device > Aktif**

> **💡 TIPS:** Di perangkat Samsung, aktifkan juga Find My Mobile Samsung di: **Pengaturan > Keamanan dan privasi > Find My Mobile**. Memiliki keduanya memberikan redundansi.

![Pengaturan Find Hub](../images/android-find-my-device.png)
*Gambar 1: Sakelar pengaturan Find Hub di Android (Pengaturan > Keamanan > Find My Device)*

---

## Mengakses Find Hub dari Jarak Jauh

### Melalui Browser Web

1. Buka **https://myaccount.google.com/find-your-phone** atau **https://android.com/find**
2. Masuk dengan Akun Google yang terhubung ke perangkat yang hilang
3. Pilih perangkat dari daftar

### Melalui Aplikasi Find Hub (Perangkat Android Lain)

1. Instal atau buka aplikasi **Find Hub** (tersedia di Google Play)
2. Masuk sebagai **Tamu** menggunakan Akun Google yang terhubung ke perangkat yang hilang

### Melalui Google Home (Pixel)

Beberapa perangkat Pixel dapat ditemukan melalui aplikasi Google Home saat masuk ke Akun Google yang sama.

---

## Tindakan Jarak Jauh yang Tersedia

Setelah Anda mengakses perangkat di Find Hub, tiga tindakan utama tersedia:

### 1. Putar Suara

Menyebabkan perangkat berbunyi dengan volume maksimum selama 5 menit, bahkan jika dalam mode senyap atau getar. Berguna ketika perangkat hilang di dekatnya (jatuh di balik furnitur, tertinggal di mobil, dll.).

- Tidak memerlukan perangkat untuk dibuka kuncinya
- Berfungsi melalui Wi-Fi atau seluler

### 2. Amankan Perangkat (Kunci Jarak Jauh)

Mengunci perangkat dengan PIN/kata sandi kunci layar dan secara opsional:
- Menampilkan pesan kustom di layar kunci (mis., "Ponsel ini hilang. Hubungi +62-XXX-XXXX")
- Menambahkan nomor telepon yang dapat dihubungi dari layar kunci tanpa membuka kunci
- Keluar dari perangkat dari Akun Google

> **⚠️ PERINGATAN:** Setelah "Amankan Perangkat" mengeluarkan Akun Google, Find Hub tidak lagi dapat mengakses perangkat. Gunakan tindakan ini hanya setelah mengonfirmasi pemulihan tidak segera mungkin, atau gunakan **tanpa** opsi "Keluar dari Akun Google" terlebih dahulu.

### 3. Hapus Perangkat

Melakukan reset pabrik lengkap pada perangkat, menghapus semua data termasuk:
- Foto dan file
- Aplikasi yang terinstal
- Kredensial akun
- Kartu dan kunci Google Wallet

> **⚠️ PERINGATAN:** Menghapus perangkat bersifat **permanen**. Setelah dihapus, Anda tidak dapat melacak perangkat kecuali diatur dengan Akun Google setelah penghapusan (dalam hal ini Perlindungan Reset Pabrik akan aktif). Gunakan ini hanya ketika:
> - Pemulihan perangkat dikonfirmasi tidak mungkin
> - Perangkat berisi data sensitif yang tidak boleh diakses oleh penyerang
> - Anda memiliki cadangan data terkini

---

## Pelacakan Perangkat Offline

Find Hub mendukung menemukan perangkat bahkan saat offline (tanpa Wi-Fi atau seluler):

### Cara Kerjanya

Perangkat Android dalam jaringan Find Hub secara berkala menyiarkan sinyal Bluetooth terenkripsi. Perangkat Android terdekat lainnya — bahkan milik orang asing — diam-diam mendeteksi sinyal ini dan melaporkan lokasi terenkripsi ke Google. Hanya pemilik perangkat yang dapat mendekripsi dan melihat lokasi ini.

### Mengaktifkan Berbagi Lokasi Offline

1. Buka aplikasi **Find Hub** di perangkat Anda
2. Ketuk nama perangkat Anda
3. Buka **Pengaturan**
4. Aktifkan **Simpan lokasi** atau **Temukan perangkat offline**
5. Pilih **Dengan jaringan di semua area** untuk cakupan maksimum, atau **Dengan jaringan di area ramai saja** untuk opsi yang lebih menjaga privasi

### Lokasi Pasca-Mati (Pixel 8 dan Lebih Baru)

Google Pixel 8, 8a, dan model Pixel berikutnya dapat ditemukan selama **beberapa jam setelah baterai habis**, asalkan pengaturan "temukan perangkat offline" sebelumnya telah diaktifkan.

---

## Tambahan Fitur 2025

Google memperluas kemampuan Find Hub pada 2025 dengan:

**Dukungan Ultra-Wideband (UWB)**
Memberikan presisi tingkat sentimeter untuk menemukan item saat berada dalam jarak dekat. Didukung pada perangkat Pixel dan Motorola yang kompatibel dengan perangkat keras UWB.

**Konektivitas Satelit**
Memungkinkan pelaporan lokasi perangkat melalui satelit ketika seluler dan Wi-Fi tidak tersedia. Diluncurkan secara bertahap sepanjang 2025.

**Integrasi Bagasi Maskapai**
Tag pelacak Bluetooth dapat berbagi lokasi dengan maskapai pilihan (Aer Lingus, British Airways, Cathay Pacific, Iberia, Singapore Airlines) untuk menemukan bagasi yang diperiksa.

**Dukungan Pelacak Pihak Ketiga**
Kompatibel dengan Chipolo, Pebblebee, tag Motorola, dan koper dari merek seperti Mokobara, July, dan Peak.

*Sumber: Blog Google, Mei 2025 — https://security.googleblog.com*

---

## Keamanan dan Privasi

- Semua data lokasi di Find Hub **dienkripsi end-to-end**
- Hanya pemilik akun yang dapat melihat lokasi perangkat
- Sinyal lokasi berbasis kerumunan dienkripsi; perangkat yang berpartisipasi dalam jaringan tidak dapat membaca data lokasi yang mereka relai

---

## Fitur Perlindungan Pencurian (Android 10+)

Selain Find Hub, Android menyertakan perlindungan pencurian di perangkat:

### Kunci Deteksi Pencurian

Menggunakan AI di perangkat (akselerometer, giroskop, Wi-Fi, dan Bluetooth) untuk mendeteksi pola gerakan yang konsisten dengan pencurian sambaran — sentakan tiba-tiba, gerakan cepat, berlari, bersepeda. Jika terdeteksi, layar otomatis terkunci sebelum pencuri dapat menonaktifkan pelacakan.

*Referensi: https://security.googleblog.com/2024/10/android-theft-protection.html*

### Kunci Perangkat Offline

Jika perangkat offline (internet dinonaktifkan) saat tidak terkunci setelah dicuri, perangkat secara otomatis mengunci layarnya setelah periode singkat. Ini mencegah pencuri menonaktifkan pelacakan Find Hub dengan mematikan Wi-Fi.

### Kunci Jarak Jauh (Tanpa Internet)

Android 10+ memungkinkan penguncian perangkat bahkan tanpa koneksi internet menggunakan PIN tersimpan atau melalui tantangan berbasis SMS.

---

## Langkah demi Langkah: Yang Harus Dilakukan Sekarang

```
PERANGKAT HILANG? Ikuti langkah berikut:

Langkah 1: Buka https://android.com/find
Langkah 2: Masuk dengan Akun Google Anda
Langkah 3: Pilih perangkat Anda
Langkah 4: Pilih "Putar Suara" — jika ada di dekatnya
Langkah 5: Pilih "Amankan Perangkat" — untuk mengunci dan menampilkan info kontak
Langkah 6: (Jika pemulihan tidak mungkin) — Pilih "Hapus Perangkat"
```

---

## Dokumen Terkait

- [Perlindungan Reset Pabrik](factory-reset-protection.md)
- [Keamanan Akun Google](google-account-security.md)
- [Pemeriksaan Identitas](identity-check.md)
- [5 Menit Pertama](../incident-response/first-5-minutes.md)
- [Daftar Periksa Darurat](../checklists/emergency-checklist.md)

---

*Terakhir Diperbarui: 2026-06-01 | Sumber: https://support.google.com/android | https://android.com/articles/what-is-find-hub-and-how-to-use-it/*
