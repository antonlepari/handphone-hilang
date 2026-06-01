# Perlindungan Perangkat Dicuri — iOS 17.3+

> Terakhir Diperbarui: 2026-06-01

## Ikhtisar

**Perlindungan Perangkat Dicuri** adalah fitur keamanan iOS yang diperkenalkan di **iOS 17.3** (Januari 2024) yang menambahkan persyaratan autentikasi biometrik — tanpa fallback kode sandi — untuk tindakan sensitif tertentu ketika iPhone Anda berada di lokasi yang tidak familiar. Untuk beberapa perubahan keamanan kritis, **periode tunggu wajib satu jam** juga diberlakukan.

Fitur ini dirancang sebagai respons terhadap pola serangan yang terdokumentasi di mana pencuri mengamati pemilik iPhone memasukkan kode sandi di tempat umum (shoulder surfing), mencuri perangkat, dan kemudian menggunakan kode sandi untuk mengambil alih Apple ID, menonaktifkan Find My, dan menguras akun keuangan sebelum korban dapat merespons.

*Referensi: https://support.apple.com/en-us/120340*

---

## Pola Serangan yang Diatasi

The Wall Street Journal melaporkan pada 2023 tentang serangkaian pencurian iPhone yang dimungkinkan oleh pengamatan kode sandi. Rantai serangan tersebut adalah:

1. Pencuri mengamati korban memasukkan kode sandi (dari atas bahu di bar, kafe, transportasi umum)
2. Pencuri mencuri iPhone (copet, sambaran)
3. Menggunakan kode sandi yang diamati, pencuri:
   - Mengubah kata sandi Apple ID (Pengaturan > Apple ID > Kata Sandi & Keamanan)
   - Menonaktifkan Find My, mencegah pelacakan jarak jauh
   - Menambahkan wajah/sidik jari mereka sendiri sebagai biometrik, mengunci korban
   - Mengakses kata sandi yang tersimpan di iCloud Keychain
   - Mentransfer uang dari aplikasi perbankan
   - Meminta kode perangkat tepercaya yang dikirim ke ponsel yang dicuri (menyelesaikan pengambilalihan akun Apple ID)

Perlindungan Perangkat Dicuri memutus beberapa langkah dalam rantai ini dengan memerlukan autentikasi biometrik yang tidak dimiliki pencuri.

---

## Cara Kerjanya

### Tindakan Hanya Biometrik (Tanpa Fallback Kode Sandi)

Ketika Perlindungan Perangkat Dicuri diaktifkan dan iPhone berada di **lokasi yang tidak familiar**, tindakan berikut memerlukan **Face ID atau Touch ID** tanpa alternatif kode sandi:

| Tindakan yang Dilindungi | Mengapa Penting |
|---|---|
| Lihat/gunakan kata sandi tersimpan di iCloud Keychain | Mencegah pencurian kredensial |
| Gunakan metode pembayaran tersimpan (non-Apple Pay) | Mencegah akses keuangan |
| Ajukan permohonan Apple Card baru | Mencegah penipuan |
| Lihat nomor kartu virtual Apple Card | Mencegah penipuan kartu |
| Matikan Mode Hilang | Mencegah pencuri membatalkan pelacakan |
| Hapus Semua Konten dan Pengaturan | Mencegah penghapusan perangkat untuk bypass pelacakan |
| Gunakan iPhone untuk mereset kata sandi Apple ID di perangkat baru | Mencegah pengambilalihan akun |
| Buat atau akses Kunci Pemulihan | Mencegah penguncian permanen akun korban |
| Ubah nomor telepon tepercaya | Mencegah perubahan mekanisme pemulihan akun |

### Penundaan Keamanan (Tunggu Satu Jam)

Untuk perubahan keamanan akun yang paling kritis, **periode tunggu wajib satu jam** diberlakukan, diikuti oleh konfirmasi Face ID atau Touch ID kedua:

| Tindakan yang Dikenai Penundaan | Mengapa Penundaan Penting |
|---|---|
| Ubah kata sandi Apple ID | Memberi waktu bagi korban untuk merespons dan mengunci perangkat dari jarak jauh |
| Keluar dari Apple ID | Mencegah pemutusan akun segera |
| Perbarui pengaturan keamanan Akun Apple | Mencegah penguncian akun cepat terhadap korban |
| Tambah atau hapus kunci pemulihan | Menjaga opsi pemulihan akun untuk korban |
| Tambah atau hapus nomor telepon tepercaya | Mencegah perubahan mekanisme pemulihan akun |
| Ubah kode sandi iPhone | Mencegah penguncian korban dari perangkat mereka sendiri |
| Ubah Face ID atau Touch ID | Mencegah penyerang mendaftarkan biometrik mereka sendiri |
| Matikan Find My | Menjaga kemampuan korban untuk melacak dan menghapus jarak jauh |
| Matikan Perlindungan Perangkat Dicuri | Perlindungan diri |

Penundaan satu jam berarti bahwa bahkan jika pencuri memiliki biometrik (mis., dalam skenario yang dipaksakan), korban memiliki setidaknya satu jam untuk menggunakan perangkat Apple lain untuk mengunci atau menghapus iPhone yang dicuri melalui Find My.

---

## Persyaratan

Untuk mengaktifkan Perlindungan Perangkat Dicuri, hal-hal berikut harus sudah dikonfigurasi:

- [ ] iPhone menjalankan **iOS 17.3 atau lebih baru**
- [ ] **Autentikasi dua faktor** diaktifkan untuk Apple ID
- [ ] **Kode sandi perangkat** dikonfigurasi
- [ ] **Face ID atau Touch ID** terdaftar
- [ ] **Find My** dihidupkan
- [ ] **Lokasi Signifikan** (Layanan Lokasi) diaktifkan
  - Buka: Pengaturan > Privasi & Keamanan > Layanan Lokasi > Layanan Sistem > Lokasi Signifikan

> **⚠️ PERINGATAN:** Lokasi Signifikan harus diaktifkan agar fitur dapat menentukan lokasi "familiar" vs. "tidak familiar". Data ini disimpan terenkripsi di perangkat dan tidak dibagikan dengan Apple.

---

## Cara Mengaktifkan Perlindungan Perangkat Dicuri

1. Buka **Pengaturan**
2. Ketuk **Face ID & Kode Sandi** (atau **Touch ID & Kode Sandi**)
3. Masukkan kode sandi perangkat Anda
4. Gulir ke bawah ke **Perlindungan Perangkat Dicuri**
5. Ketuk **Aktifkan Perlindungan**

![Pengaturan Perlindungan Perangkat Dicuri](../images/ios-stolen-device-protection.png)
*Gambar 1: Sakelar Perlindungan Perangkat Dicuri di Pengaturan > Face ID & Kode Sandi*

---

## Lokasi Familiar vs. Tidak Familiar

### Bagaimana Lokasi Familiar Ditentukan

iOS menggunakan **Lokasi Signifikan** (di bawah Layanan Lokasi > Layanan Sistem) untuk mempelajari tempat yang sering dikunjungi:
- Alamat rumah Anda
- Tempat kerja Anda
- Tempat yang Anda kunjungi secara teratur

Data ini diproses di perangkat menggunakan pembelajaran mesin dan tidak pernah dikirim ke server Apple.

### Kapan Perlindungan Berlaku

| Lokasi | Persyaratan Biometrik | Penundaan Keamanan |
|---|---|---|
| Lokasi familiar (rumah, kerja) | Kode sandi diizinkan sebagai fallback | Tidak diberlakukan |
| Lokasi tidak familiar (semua tempat lain) | Biometrik diperlukan, tanpa fallback kode sandi | Diberlakukan untuk perubahan kritis |

---

## Perbandingan: Perlindungan Biometrik Anti-Pencurian iOS vs. Android

| Fitur | Perlindungan Perangkat Dicuri (iOS 17.3+) | Pemeriksaan Identitas (Android 15+) |
|---|---|---|
| Tindakan sensitif hanya biometrik | Ya | Ya |
| Tanpa fallback kode sandi di luar rumah | Ya | Ya |
| Penundaan keamanan satu jam | Ya | Tidak (per 2025) |
| Memerlukan Lokasi Signifikan | Ya | Ya (lokasi tepercaya) |
| Memerlukan Find My / Find Hub aktif | Ya | Ya |
| Tersedia di semua perangkat | iOS 17.3+, semua iPhone yang didukung | Android 15, Pixel + Samsung |

---

## Keterbatasan

| Pertimbangan | Detail |
|---|---|
| **Skenario paksaan** | Tidak melindungi dari paksaan fisik ("buka kunci dengan wajah Anda") |
| **Akurasi lokasi familiar** | Di awal penggunaan, Lokasi Signifikan mungkin belum mempelajari semua tempat familiar |
| **Ketidaknyamanan penundaan satu jam** | Jika Anda berada di lokasi yang tidak familiar dan secara sah perlu mengubah pengaturan ini, Anda harus menunggu satu jam |
| **Kompatibilitas Mode Penguncian** | Mode Penguncian (iOS 16+) memberikan penguatan ekstrem terpisah; keduanya dapat digunakan bersama |

---

## Daftar Periksa: Konfigurasi Perlindungan Perangkat Dicuri

- [ ] iOS 17.3 atau lebih baru terinstal
- [ ] Perlindungan Perangkat Dicuri: **Diaktifkan** (Pengaturan > Face ID & Kode Sandi > Perlindungan Perangkat Dicuri)
- [ ] Face ID / Touch ID: **Terdaftar**
- [ ] Find My: **Diaktifkan**
- [ ] Lokasi Signifikan: **Diaktifkan** (Pengaturan > Privasi & Keamanan > Layanan Lokasi > Layanan Sistem > Lokasi Signifikan)
- [ ] Autentikasi dua faktor di Apple ID: **Diaktifkan**

---

## Dokumen Terkait

- [Find My](find-my.md)
- [Mode Hilang](lost-mode.md)
- [Kunci Aktivasi](activation-lock.md)
- [Pemulihan Apple ID](apple-id-recovery.md)
- [Panduan Penguatan iOS](../hardening/ios-hardening.md)
- [Pemeriksaan Identitas Android (perbandingan)](../android/identity-check.md)

---

*Terakhir Diperbarui: 2026-06-01 | Sumber: https://support.apple.com/en-us/120340*
