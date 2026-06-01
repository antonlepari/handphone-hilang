# Daftar Periksa Penguatan Android

> Terakhir Diperbarui: 2026-06-01

Daftar periksa ini mencakup 40+ item konfigurasi untuk memperkuat perangkat Android terhadap kehilangan, pencurian, dan akses tidak sah. Item diorganisir berdasarkan kategori. Versi Android yang berlaku dicatat di mana perilaku berbeda.

---

## Kunci Layar dan Autentikasi

- [ ] **Atur jenis kunci layar ke PIN (6+ digit), kata sandi, atau frasa sandi alfanumerik**
  - Pengaturan > Keamanan > Kunci layar
  - Hindari: Geser, Pola (mudah diamati), Buka kunci wajah saja di perangkat keamanan rendah

- [ ] **Atur batas waktu kunci layar ke 30 detik**
  - Pengaturan > Layar > Batas waktu layar (atau Layar kunci > Batas waktu kunci layar)

- [ ] **Nonaktifkan "Tampilkan notifikasi saat terkunci"** untuk aplikasi sensitif
  - Pengaturan > Notifikasi > [Aplikasi] > Di Layar Kunci > Jangan tampilkan notifikasi

- [ ] **Nonaktifkan "Tampilkan konten notifikasi di layar kunci"** secara global
  - Pengaturan > Notifikasi > Privasi notifikasi > Sembunyikan konten notifikasi

- [ ] **Aktifkan "Kunci jaringan dan keamanan" saat kunci** (mencegah perubahan Wi-Fi/Bluetooth dari layar kunci)
  - Pengaturan > Keamanan > Pengaturan keamanan lainnya > Keamanan jaringan

- [ ] **Nonaktifkan fitur smart lock** kecuali benar-benar diperlukan
  - Smart Lock (perangkat tepercaya, tempat tepercaya) mengurangi keamanan; nonaktifkan jika tidak diperlukan
  - Pengaturan > Keamanan > Pengaturan keamanan lainnya > Smart Lock

- [ ] **Aktifkan "Hapus data setelah upaya gagal"**
  - Android: Pengaturan > Keamanan > Kunci otomatis ATAU periksa pengaturan khusus produsen

---

## Biometrik

- [ ] **Daftarkan autentikasi sidik jari**
  - Pengaturan > Keamanan > Sidik Jari

- [ ] **Tinjau dan pahami fallback biometrik**
  - Biometrik kembali ke PIN — pastikan PIN kuat (lihat di atas)
  - Aktifkan Pemeriksaan Identitas (Android 15+) untuk memblokir fallback kode sandi di luar rumah

- [ ] **Nonaktifkan "Bangunkan layar" untuk buka kunci wajah** di perangkat keamanan rendah
  - Pengenalan wajah di Android tanpa sensor aman (IR + kedalaman) dapat ditipu dengan foto

- [ ] **Daftarkan ulang biometrik setelah pembaruan OS baru** jika diminta (memastikan akurasi kalibrasi)

---

## Find Hub dan Anti-Pencurian

- [ ] **Aktifkan Find My Device / Find Hub**
  - Pengaturan > Keamanan > Find My Device > Aktifkan
  - Atau: Pengaturan > Google > Find My Device

- [ ] **Verifikasi Find Hub berfungsi**: masuk di https://android.com/find dari perangkat lain

- [ ] **Aktifkan Pencarian Perangkat Offline** di aplikasi Find Hub
  - Find Hub > Pengaturan perangkat > Simpan lokasi > Dengan jaringan di semua area

- [ ] **Aktifkan Kunci Deteksi Pencurian** (Android 10+)
  - Pengaturan > Keamanan > Perlindungan pencurian > Kunci Deteksi Pencurian

- [ ] **Aktifkan Kunci Perangkat Offline** (Android 10+)
  - Pengaturan > Keamanan > Perlindungan pencurian > Kunci Perangkat Offline

- [ ] **Aktifkan Kunci Jarak Jauh** (Android 10+)
  - Pengaturan > Keamanan > Perlindungan pencurian > Kunci Jarak Jauh

- [ ] **Aktifkan Pemeriksaan Identitas** (Android 15+, Pixel dan Samsung Galaxy)
  - Pengaturan > Keamanan & privasi > Keamanan & privasi lainnya > Pemeriksaan Identitas

---

## Keamanan Akun Google

- [ ] **Aktifkan Verifikasi 2 Langkah di Akun Google**
  - https://myaccount.google.com/security > Verifikasi 2 Langkah > Aktifkan

- [ ] **Gunakan aplikasi autentikator atau Google Prompt untuk 2FA** (bukan SMS)

- [ ] **Tinjau dan hapus perangkat tepercaya yang tidak dikenal**
  - https://myaccount.google.com/device-activity

- [ ] **Unduh dan simpan kode cadangan secara offline**
  - https://myaccount.google.com/two-step-verification/backup-codes

- [ ] **Atur email pemulihan yang menggunakan penyedia berbeda dan memiliki 2FA-nya sendiri**

- [ ] **Selesaikan Pemeriksaan Keamanan Google**
  - https://myaccount.google.com/security-checkup

---

## Manajemen Izin Aplikasi

- [ ] **Audit izin lokasi untuk semua aplikasi**
  - Pengaturan > Privasi > Manajer izin > Lokasi
  - Ubah semua aplikasi non-esensial dari "Selalu" ke "Hanya saat menggunakan" atau "Tolak"

- [ ] **Cabut akses mikrofon untuk aplikasi yang tidak membutuhkannya**
  - Pengaturan > Privasi > Manajer izin > Mikrofon

- [ ] **Cabut akses kamera untuk aplikasi yang tidak membutuhkannya**
  - Pengaturan > Privasi > Manajer izin > Kamera

- [ ] **Cabut akses Kontak untuk aplikasi yang tidak membutuhkannya**
  - Pengaturan > Privasi > Manajer izin > Kontak

- [ ] **Tinjau akses Notifikasi** — hanya berikan ke aplikasi tepercaya
  - Pengaturan > Privasi > Manajer izin > Notifikasi

- [ ] **Tinjau izin "Tampilkan di atas aplikasi lain"** — hapus dari aplikasi yang tidak tepercaya
  - Pengaturan > Aplikasi > Akses aplikasi khusus > Tampilkan di atas aplikasi lain

- [ ] **Tinjau izin "Instal aplikasi tidak dikenal"** — semua harus dinonaktifkan kecuali diperlukan
  - Pengaturan > Aplikasi > Akses aplikasi khusus > Instal aplikasi tidak dikenal

---

## Keamanan Jaringan

- [ ] **Nonaktifkan "Sambungkan ke jaringan terbuka" / sambungan otomatis ke Wi-Fi publik**
  - Pengaturan > Jaringan & internet > Wi-Fi > Preferensi Wi-Fi > Sambung ke jaringan publik: Nonaktif

- [ ] **Atur alamat MAC Wi-Fi ke acak** (per jaringan) untuk mencegah pelacakan lokasi
  - Pengaturan > Jaringan & internet > Wi-Fi > [Jaringan] > Privasi > Gunakan MAC acak (Android 10+)

- [ ] **Instal dan gunakan VPN bereputasi** untuk penggunaan Wi-Fi publik
  - Pilihan: Mullvad, ProtonVPN (penyedia tanpa log, diaudit)

- [ ] **Aktifkan DNS Pribadi**
  - Pengaturan > Jaringan & internet > DNS Pribadi > Otomatis atau atur ke dns.google atau 1dot1dot1dot1.cloudflare-dns.com

- [ ] **Nonaktifkan Bluetooth saat tidak digunakan**
  - Pengaturan Cepat atau Pengaturan > Bluetooth

---

## Play Protect dan Keamanan Aplikasi

- [ ] **Verifikasi Play Protect diaktifkan dan terkini**
  - Play Store > Profil > Play Protect > Status harus menampilkan "Tidak ada aplikasi berbahaya yang ditemukan"

- [ ] **Jalankan pemindaian Play Protect manual**
  - Play Store > Profil > Play Protect > Pindai

- [ ] **Aktifkan "Tingkatkan deteksi aplikasi berbahaya"**
  - Play Store > Profil > Play Protect > Pengaturan > Tingkatkan deteksi aplikasi berbahaya

- [ ] **Hapus aplikasi yang tidak Anda gunakan atau kenali**
  - Pengaturan > Aplikasi > Lihat semua aplikasi > uninstal aplikasi yang tidak digunakan

- [ ] **Jangan instal aplikasi dari luar Play Store** kecuali benar-benar diperlukan

- [ ] **Tinjau aplikasi yang memiliki akses Administrator Perangkat**
  - Pengaturan > Keamanan > Aplikasi admin perangkat > Hapus yang tidak Anda kenali

---

## Opsi Pengembang (Nonaktifkan Kecuali Anda Pengembang)

- [ ] **Nonaktifkan penelusuran USB**
  - Pengaturan > Sistem > Opsi pengembang > Penelusuran USB: Nonaktif
  - Jika Opsi pengembang tidak terlihat, itu dinonaktifkan secara default (diutamakan)

- [ ] **Nonaktifkan "Buka kunci OEM"**
  - Pengaturan > Sistem > Opsi pengembang > Buka kunci OEM: Nonaktif
  - Jika diaktifkan, memungkinkan buka kunci bootloader yang melewati FRP

- [ ] **Nonaktifkan "Lokasi palsu"**
  - Pengaturan > Sistem > Opsi pengembang > Pilih aplikasi lokasi palsu: Tidak ada

- [ ] **Nonaktifkan Opsi pengembang sepenuhnya** jika Anda tidak membutuhkannya
  - Pengaturan > Sistem > Opsi pengembang > aktifkan Nonaktif (di bagian atas layar Opsi pengembang)

---

## SIM dan Perlindungan Reset Pabrik

- [ ] **Aktifkan PIN SIM**
  - Pengaturan > Keamanan > Kunci kartu SIM > Aktifkan

- [ ] **Atur PIN akun operator / kunci port-out**
  - Hubungi operator langsung atau melalui aplikasi operator

- [ ] **Verifikasi Akun Google masuk** (mengaktifkan FRP)
  - Pengaturan > Akun > Google

- [ ] **Untuk Samsung: Aktifkan Kunci Reaktivasi**
  - Pengaturan > Biometrik dan keamanan > Find My Mobile > Kunci reaktivasi: Aktifkan

---

## Cadangan

- [ ] **Aktifkan Google Backup**
  - Pengaturan > Google > Cadangan > Cadangkan ke Google Drive: Aktifkan

- [ ] **Verifikasi cadangan terkini**
  - Pengaturan > Google > Cadangan > Cadangan terakhir: periksa stempel waktu

- [ ] **Aktifkan cadangan Google Foto untuk foto dan video**
  - Google Foto > Profil > Pengaturan Google Foto > Cadangan: Aktifkan

- [ ] **Untuk data sensitif: uji pemulihan**
  - Mulai pemulihan cadangan di perangkat uji atau perangkat yang telah direset untuk memverifikasi kelengkapan

---

## Keamanan Fisik

- [ ] **Jangan gunakan perangkat di tempat layar terlihat oleh orang asing** saat memasukkan PIN
- [ ] **Aktifkan kunci segera setelah layar mati** (tidak ditunda)
  - Pengaturan > Keamanan > Kunci layar > Kunci setelah batas waktu layar: Segera
- [ ] **Pertimbangkan pelindung layar privasi** untuk membatasi visibilitas layar hanya pada tampilan sumbu

---

## Dokumen Terkait

- [Panduan Penguatan Android](../hardening/android-hardening.md)
- [Sebelum Kehilangan — Pencegahan](before-loss-prevention.md)
- [Daftar Periksa Darurat](emergency-checklist.md)
- [Keamanan SIM](../hardening/sim-security.md)

---

*Terakhir Diperbarui: 2026-06-01*
