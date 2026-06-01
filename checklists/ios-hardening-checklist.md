# Daftar Periksa Penguatan iOS

> Terakhir Diperbarui: 2026-06-01

Daftar periksa ini mencakup 40+ item konfigurasi untuk memperkuat iPhone terhadap kehilangan, pencurian, dan akses tidak sah. Item diorganisir berdasarkan kategori. Persyaratan versi iOS dicatat di mana perilaku berbeda.

---

## Face ID / Touch ID

- [ ] **Daftarkan Face ID atau Touch ID**
  - Pengaturan > Face ID & Kode Sandi (atau Touch ID & Kode Sandi)

- [ ] **Aktifkan Face ID / Touch ID untuk**: Buka Kunci iPhone, iTunes & App Store, Apple Pay, Isi Otomatis Kata Sandi, Dompet & Apple Pay
  - Pengaturan > Face ID & Kode Sandi > centang semua opsi yang diinginkan

- [ ] **Aktifkan Perlindungan Perangkat Dicuri (iOS 17.3+)**
  - Pengaturan > Face ID & Kode Sandi > Perlindungan Perangkat Dicuri > Aktifkan Perlindungan
  - Lihat: [Perlindungan Perangkat Dicuri](../ios/stolen-device-protection.md)

- [ ] **Aktifkan Lokasi Signifikan** (diperlukan untuk Perlindungan Perangkat Dicuri)
  - Pengaturan > Privasi & Keamanan > Layanan Lokasi > Layanan Sistem > Lokasi Signifikan: Aktif

- [ ] **Jangan gunakan bypass fitur perhatian "Aksesibilitas"** — pastikan deteksi perhatian wajah aktif
  - Pengaturan > Face ID & Kode Sandi > Perlu Perhatian untuk Face ID: Aktif

---

## Kunci Layar dan Kode Sandi

- [ ] **Atur kode sandi yang kuat (6+ digit atau alfanumerik)**
  - Pengaturan > Face ID & Kode Sandi > Ubah Kode Sandi > Opsi Kode Sandi > Kode Alfanumerik Kustom

- [ ] **Atur Kunci Otomatis ke 30 detik**
  - Pengaturan > Layar & Kecerahan > Kunci Otomatis > 30 Detik

- [ ] **Aktifkan "Hapus Data" setelah 10 upaya kode sandi yang gagal**
  - Pengaturan > Face ID & Kode Sandi > Hapus Data: Aktifkan

- [ ] **Nonaktifkan akses ke fitur tertentu dari layar kunci** untuk item sensitif
  - Pengaturan > Face ID & Kode Sandi > Izinkan Akses Saat Terkunci:
    - Tampilan Hari Ini: Nonaktif (jika widget menampilkan info sensitif)
    - Pusat Notifikasi: Nonaktif (opsional — mencegah membaca notifikasi)
    - Siri: Nonaktif (opsional — mencegah kueri layar kunci Siri)
    - Aksesori USB: Nonaktif (mencegah akses data USB tanpa buka kunci)

- [ ] **Nonaktifkan akses Aksesori USB dari layar kunci**
  - Pengaturan > Face ID & Kode Sandi > Aksesori USB: Nonaktif
  - Mencegah ekstraksi data melalui USB jika perangkat terkunci lebih dari 1 jam

---

## Find My

- [ ] **Aktifkan Find My iPhone**
  - Pengaturan > [Nama Anda] > Find My > Find My iPhone: Aktif

- [ ] **Aktifkan Pencarian Offline**
  - Pengaturan > [Nama Anda] > Find My > Find My iPhone > Aktifkan Pencarian Offline: Aktif

- [ ] **Aktifkan Kirim Lokasi Terakhir**
  - Pengaturan > [Nama Anda] > Find My > Find My iPhone > Kirim Lokasi Terakhir: Aktif

- [ ] **Verifikasi Find My di https://icloud.com/find** dari perangkat lain

---

## Keamanan Apple ID dan iCloud

- [ ] **Aktifkan Autentikasi Dua Faktor di Apple ID**
  - Pengaturan > [Nama Anda] > Masuk & Keamanan > Autentikasi Dua Faktor: Aktifkan

- [ ] **Atur Kontak Pemulihan**
  - Pengaturan > [Nama Anda] > Masuk & Keamanan > Pemulihan Akun > Kontak Pemulihan

- [ ] **Buat dan simpan Kunci Pemulihan**
  - Pengaturan > [Nama Anda] > Masuk & Keamanan > Kunci Pemulihan
  - Simpan kunci di lokasi yang aman secara fisik dan offline

- [ ] **Tinjau dan hapus perangkat tepercaya yang tidak dikenal dari Apple ID**
  - Pengaturan > [Nama Anda] > gulir ke Perangkat > tinjau masing-masing

- [ ] **Tinjau nomor telepon tepercaya** untuk 2FA
  - Pengaturan > [Nama Anda] > Masuk & Keamanan > Nomor Telepon Tepercaya

- [ ] **Aktifkan Cadangan iCloud** (harian, otomatis)
  - Pengaturan > [Nama Anda] > iCloud > Cadangan iCloud > Cadangkan Sekarang / aktifkan otomatis

- [ ] **Tinjau aplikasi mana yang memiliki akses iCloud**
  - Pengaturan > [Nama Anda] > iCloud > [Daftar aplikasi] — nonaktifkan sinkronisasi untuk aplikasi sensitif jika diinginkan

---

## Izin Aplikasi

- [ ] **Audit izin Lokasi untuk semua aplikasi**
  - Pengaturan > Privasi & Keamanan > Layanan Lokasi > tinjau setiap aplikasi
  - Ubah "Selalu" ke "Saat Menggunakan" untuk aplikasi yang tidak membutuhkan lokasi latar belakang

- [ ] **Tinjau akses Mikrofon**
  - Pengaturan > Privasi & Keamanan > Mikrofon — hapus akses dari aplikasi yang tidak digunakan

- [ ] **Tinjau akses Kamera**
  - Pengaturan > Privasi & Keamanan > Kamera — hapus akses dari aplikasi yang tidak digunakan

- [ ] **Tinjau akses Kontak**
  - Pengaturan > Privasi & Keamanan > Kontak — batasi ke aplikasi yang benar-benar membutuhkannya

- [ ] **Tinjau akses data Kesehatan**
  - Pengaturan > Privasi & Keamanan > Kesehatan — batasi ke aplikasi kesehatan yang dipercaya secara eksplisit

- [ ] **Aktifkan Laporan Privasi Aplikasi** untuk memantau penggunaan izin aktual
  - Pengaturan > Privasi & Keamanan > Laporan Privasi Aplikasi: Aktifkan

---

## Keamanan Jaringan

- [ ] **Aktifkan "Batasi Pelacakan Alamat IP"** di pengaturan Wi-Fi
  - Pengaturan > Wi-Fi > [Jaringan] > Batasi Pelacakan Alamat IP: Aktif

- [ ] **Gunakan Alamat Wi-Fi Pribadi** untuk setiap jaringan
  - Pengaturan > Wi-Fi > [Jaringan] > Alamat Wi-Fi Pribadi: Aktif

- [ ] **Nonaktifkan "Gabung Otomatis"** untuk jaringan publik/tidak tepercaya
  - Pengaturan > Wi-Fi > [Jaringan] > Gabung Otomatis: Nonaktif untuk jaringan publik

- [ ] **Gunakan VPN bereputasi di jaringan yang tidak tepercaya**

- [ ] **Aktifkan iCloud Private Relay** (memerlukan langganan iCloud+)
  - Pengaturan > [Nama Anda] > iCloud > Private Relay: Aktif

---

## Keamanan Safari dan Browser

- [ ] **Aktifkan "Peringatan Situs Web Penipuan"** di Safari
  - Pengaturan > Safari > Peringatan Situs Web Penipuan: Aktif

- [ ] **Aktifkan "Cegah Pelacakan Lintas Situs"**
  - Pengaturan > Safari > Cegah Pelacakan Lintas Situs: Aktif

- [ ] **Aktifkan "Sembunyikan Alamat IP" di Safari**
  - Pengaturan > Safari > Sembunyikan Alamat IP: Dari Pelacak

- [ ] **Aktifkan Perlindungan Privasi Mail** (iOS 15+)
  - Pengaturan > Mail > Perlindungan Privasi > Lindungi Aktivitas Mail: Aktif

---

## Privasi Siri

- [ ] **Nonaktifkan "Izinkan Siri Saat Terkunci"** jika Anda tidak membutuhkan Siri layar kunci
  - Pengaturan > Face ID & Kode Sandi > Siri: Nonaktif

- [ ] **Nonaktifkan "Tampilkan Saran Siri"** untuk kategori aplikasi sensitif
  - Pengaturan > Siri & Pencarian > [Aplikasi] > Tampilkan Saran Siri: Nonaktif

- [ ] **Tinjau "Hey Siri" — nonaktifkan jika tidak diperlukan**
  - Pengaturan > Siri & Pencarian > Dengarkan "Hey Siri": Nonaktif (mencegah aktivasi suara saat perangkat di atas meja)

---

## Screen Time dan Pembatasan

- [ ] **Aktifkan Screen Time dengan kode sandi terpisah** (berbeda dari kode sandi perangkat)
  - Pengaturan > Screen Time > Gunakan Kode Sandi Screen Time
  - Ini mencegah pencuri dengan kode sandi perangkat menonaktifkan pembatasan

- [ ] **Aktifkan pembatasan "Perubahan Akun"** di bawah Pembatasan Konten & Privasi
  - Pengaturan > Screen Time > Pembatasan Konten & Privasi > Perubahan Akun: Jangan Izinkan
  - Mencegah perubahan email/kata sandi akun tanpa kode sandi Screen Time

- [ ] **Aktifkan pembatasan "Perubahan Kode Sandi"** (mencegah perubahan kode sandi perangkat)
  - Pengaturan > Screen Time > Pembatasan Konten & Privasi > Perubahan Kode Sandi: Jangan Izinkan

- [ ] **Aktifkan pembatasan "Layanan Lokasi"**
  - Pengaturan > Screen Time > Pembatasan Konten & Privasi > Privasi > Layanan Lokasi: Jangan Izinkan Perubahan

---

## Keamanan SIM

- [ ] **Aktifkan PIN SIM**
  - Pengaturan > Seluler > PIN SIM > Aktifkan

- [ ] **Atur PIN akun operator dan kunci port-out** (lihat langkah khusus operator)
  - Lihat: [Keamanan SIM](../hardening/sim-security.md)

---

## Penguatan Tambahan

- [ ] **Perbarui iOS ke versi terbaru**
  - Pengaturan > Umum > Pembaruan Perangkat Lunak

- [ ] **Aktifkan pembaruan otomatis**
  - Pengaturan > Umum > Pembaruan Perangkat Lunak > Pembaruan Otomatis: Aktif

- [ ] **Tinjau aplikasi yang baru diinstal** untuk yang tidak familiar
  - Pengaturan > Umum > Penyimpanan iPhone > tinjau aplikasi dan tanggal terakhir digunakan

- [ ] **Pertimbangkan Mode Penguncian** untuk pengguna berisiko tinggi (jurnalis, eksekutif, aktivis)
  - Pengaturan > Privasi & Keamanan > Mode Penguncian
  - Sangat membatasi permukaan serangan tetapi membatasi beberapa fungsi perangkat

---

## Persiapan Pemulihan

- [ ] **Kata sandi Apple ID dihafal atau ada di pengelola kata sandi yang dapat diakses secara offline**
- [ ] **Kunci Pemulihan disimpan secara fisik di lokasi yang aman**
- [ ] **Kontak Pemulihan disiapkan dan dikonfirmasi**
- [ ] **IMEI perangkat dicatat** (Pengaturan > Umum > Tentang > IMEI)
- [ ] **Tanda terima pembelian asli disimpan** (di email aman atau salinan fisik)

---

## Dokumen Terkait

- [Panduan Penguatan iOS](../hardening/ios-hardening.md)
- [Sebelum Kehilangan — Pencegahan](before-loss-prevention.md)
- [Daftar Periksa Darurat](emergency-checklist.md)
- [Keamanan SIM](../hardening/sim-security.md)
- [Perlindungan Perangkat Dicuri](../ios/stolen-device-protection.md)

---

*Terakhir Diperbarui: 2026-06-01*
