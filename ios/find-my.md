# Find My — iOS

> Terakhir Diperbarui: 2026-06-01

## Ikhtisar

**Find My** adalah platform Apple untuk menemukan iPhone, iPad, Mac, Apple Watch, AirPods, dan AirTag yang hilang atau dicuri. Platform ini menggunakan GPS, pemosisian Wi-Fi, triangulasi seluler, dan jaringan Bluetooth terenkripsi berbasis kerumunan dari ratusan juta perangkat Apple untuk menemukan item bahkan saat offline.

Find My berbeda dari, tetapi terkait dengan, Kunci Aktivasi — mengaktifkan Find My secara otomatis mengaktifkan Kunci Aktivasi.

*Referensi: https://support.apple.com/en-us/104978*

---

## Prasyarat

Agar Find My dapat membantu Anda memulihkan perangkat, hal-hal berikut harus dikonfigurasi **sebelum** kehilangan:

- [ ] **Find My** diaktifkan di perangkat (Pengaturan > [Nama Anda] > Find My > Find My iPhone: Aktif)
- [ ] **Aktifkan Pencarian Offline** diaktifkan (memungkinkan lokasi bahkan tanpa seluler/Wi-Fi)
- [ ] **Kirim Lokasi Terakhir** diaktifkan (mengirim lokasi ke Apple ketika baterai kritis rendah)
- [ ] **Autentikasi Dua Faktor** diaktifkan di Apple ID Anda
- [ ] Anda mengetahui alamat email Apple ID dan kata sandi Anda

> **⚠️ PERINGATAN:** Find My tidak dapat diaktifkan dari jarak jauh. Harus diaktifkan sebelum perangkat hilang. Jika Perlindungan Perangkat Dicuri diaktifkan, Find My tidak dapat dimatikan tanpa autentikasi biometrik.

---

## Cara Mengaktifkan Find My

1. Buka **Pengaturan**
2. Ketuk nama Anda di bagian atas (Apple ID)
3. Ketuk **Find My**
4. Ketuk **Find My iPhone**
5. Aktifkan **Find My iPhone**: Aktifkan ke **Aktif**
6. Aktifkan **Aktifkan Pencarian Offline**: Aktifkan ke **Aktif**
7. Aktifkan **Kirim Lokasi Terakhir**: Aktifkan ke **Aktif**

![Pengaturan Find My](../images/ios-find-my-settings.png)
*Gambar 1: Pengaturan Find My di iOS — Pengaturan > [Nama Anda] > Find My > Find My iPhone*

---

## Mengakses Find My dari Jarak Jauh

### Melalui iCloud.com

1. Buka **https://www.icloud.com/find**
2. Masuk dengan Apple ID Anda
3. Pilih perangkat Anda dari peta atau daftar perangkat

### Melalui Aplikasi Find My (Perangkat Apple Lain)

1. Buka aplikasi **Find My** di iPhone, iPad, atau Mac lain
2. Ketuk tab **Perangkat**
3. Pilih perangkat yang hilang

### Melalui Family Sharing

Jika Anda adalah bagian dari grup Family Sharing, anggota keluarga tepercaya dapat melihat lokasi perangkat Anda dan membantu tindakan Find My:
1. Buka aplikasi Find My
2. Ketuk tab **Orang**
3. Anggota keluarga dapat berbagi lokasi dan membantu jika Anda telah memberikan izin

---

## Tindakan Jarak Jauh yang Tersedia

### Putar Suara

Menyebabkan perangkat memutar nada peringatan keras selama sekitar 2 menit, bahkan dalam mode senyap. Berguna ketika perangkat hilang di dekatnya.

### Tandai sebagai Hilang (Mode Hilang)

Mengaktifkan Mode Hilang — lihat [Mode Hilang](lost-mode.md) untuk detail lengkap. Ketika Anda menandai perangkat sebagai hilang:
- Perangkat dikunci dengan kode sandi Anda
- Pesan kustom dan nomor telepon ditampilkan di layar kunci
- Perangkat mulai melaporkan pembaruan lokasi secara berkelanjutan
- Apple Pay dinonaktifkan
- Perangkat tidak dapat dipasangkan dengan aksesori baru

### Hapus Perangkat Ini

Melakukan penghapusan jarak jauh lengkap pada perangkat:
- Semua data pribadi dihapus
- Perangkat dikembalikan ke pengaturan pabrik
- **Kunci Aktivasi tetap aktif** — perangkat tidak dapat diatur tanpa kredensial Apple ID Anda

> **⚠️ PERINGATAN:** Setelah Anda menghapus perangkat, Anda tidak dapat lagi melacak lokasinya melalui Find My. Perangkat akan menampilkan status "Dihapus" di Find My setelah tindakan selesai. Jangan hapus sampai Anda yakin pemulihan tidak mungkin dan perlindungan data menjadi prioritas.

---

## Pencarian Offline

### Cara Kerjanya

iPhone menyiarkan sinyal Bluetooth terenkripsi yang dapat dideteksi oleh perangkat Apple terdekat lainnya. Perangkat tersebut secara diam-diam menyampaikan sinyal lokasi terenkripsi ke server Apple. Hanya pemilik perangkat yang dapat mendekripsi dan melihat lokasi — bukan Apple, dan bukan perangkat yang menyampaikan sinyal.

### Kirim Lokasi Terakhir

Ketika diaktifkan, iPhone secara otomatis mengirimkan lokasi GPS terakhirnya ke server Apple ketika baterai mencapai level yang sangat rendah, sebelum mati. Lokasi terakhir ini terlihat di Find My.

### Pelacakan Pasca-Mati

iPhone yang lebih baru (iPhone 11 dan lebih baru) dapat terus ditemukan untuk suatu periode **setelah baterai habis atau perangkat dimatikan**, menggunakan sinyal Bluetooth daya rendah. Ini memerlukan:
- "Aktifkan Pencarian Offline" dihidupkan sebelum mati daya
- Perangkat Apple lain berada dalam jangkauan Bluetooth untuk menyampaikan sinyal

---

## Status Perbaikan iOS 17.5

Diperkenalkan di **iOS 17.5**, **Status Perbaikan** memungkinkan Anda mengirim iPhone untuk servis tanpa menonaktifkan Find My dan Kunci Aktivasi:

- Perangkat tetap dapat dilacak di Find My
- Tidak dapat dihapus tanpa kata sandi Apple ID pemilik
- Dapat ditempatkan dalam Mode Hilang sehingga teknisi perbaikan melihat informasi kontak
- Kunci Aktivasi tetap aktif selama perbaikan

Ini mencegah akses data yang tidak sah selama servis perangkat.

*Sumber: https://support.apple.com/en-us/105092*

---

## Family Sharing dan Find My

Dengan **Family Sharing**, hingga 5 anggota keluarga dapat:
- Berbagi lokasi perangkat mereka satu sama lain
- Saling membantu dengan tindakan Mode Hilang
- Melacak AirTag bersama

**Menyiapkan berbagi lokasi:**
1. Pengaturan > [Nama Anda] > Family Sharing
2. Atur atau bergabung dengan grup Family Sharing
3. Aktifkan "Bagikan Lokasi Saya"

---

## Integrasi AirTag

**AirTag** adalah perangkat pelacak kecil yang terintegrasi dengan Find My:
- Pasang ke kunci, dompet, bagasi, atau tas
- Dapat dideteksi di Find My bahkan di luar jangkauan Bluetooth perangkat Anda
- Gunakan Pencarian Presisi (UWB di iPhone yang didukung) untuk lokasi tingkat sentimeter saat berada di dekatnya

> **ℹ️ CATATAN:** AirTag dirancang untuk menemukan barang yang hilang, bukan orang. Apple telah menerapkan langkah-langkah anti-stalking: AirTag yang tidak dikenal yang bepergian bersama Anda untuk waktu yang lama akan memicu peringatan di iPhone Anda.

---

## Privasi dan Keamanan

- Semua data lokasi Find My **dienkripsi end-to-end**
- Apple tidak dapat membaca lokasi perangkat Anda
- Sinyal berbasis kerumunan dienkripsi dengan kunci yang hanya Anda pegang
- Partisipasi jaringan Find My adalah opt-out hanya untuk pengguna yang menonaktifkan Find My sepenuhnya

---

## Daftar Periksa: Konfigurasi Find My

- [ ] Find My iPhone: **Diaktifkan**
- [ ] Aktifkan Pencarian Offline: **Diaktifkan**
- [ ] Kirim Lokasi Terakhir: **Diaktifkan**
- [ ] Autentikasi dua faktor di Apple ID: **Diaktifkan**
- [ ] Kata sandi Apple ID dihafal atau disimpan di pengelola kata sandi aman
- [ ] Family sharing dengan kontak tepercaya yang dapat membantu tindakan jarak jauh

---

## Dokumen Terkait

- [Mode Hilang](lost-mode.md)
- [Kunci Aktivasi](activation-lock.md)
- [Perlindungan Perangkat Dicuri](stolen-device-protection.md)
- [Pemulihan Apple ID](apple-id-recovery.md)
- [5 Menit Pertama](../incident-response/first-5-minutes.md)

---

*Terakhir Diperbarui: 2026-06-01 | Sumber: https://support.apple.com/en-us/104978*
