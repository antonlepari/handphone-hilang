# Kunci Aktivasi — iOS

> Terakhir Diperbarui: 2026-06-01

## Ikhtisar

**Kunci Aktivasi** adalah fitur keamanan iOS yang mengikat iPhone ke Apple ID terkaitnya. Ketika diaktifkan, perangkat memerlukan alamat email dan kata sandi Apple ID pemilik sebelum dapat diaktifkan kembali setelah reset pabrik, penghapusan, atau ketika sedang diatur untuk pertama kali oleh pemilik baru.

Kunci Aktivasi **otomatis diaktifkan** setiap kali Find My dihidupkan. Anda tidak perlu mengonfigurasinya secara manual — ini aktif sebagai konsekuensi dari mengaktifkan Find My.

*Referensi: https://support.apple.com/en-us/108794*

---

## Cara Kerja Kunci Aktivasi

### Aktivasi

Kunci Aktivasi aktif secara otomatis ketika:
1. Find My diaktifkan di perangkat (Pengaturan > [Nama Anda] > Find My > Find My iPhone: Aktif)
2. Perangkat masuk ke Apple ID

Tidak diperlukan konfigurasi tambahan.

### Apa yang Dilindunginya

Ketika pencuri mencoba mereset dan menggunakan kembali iPhone yang dicuri:

```
TANPA Kunci Aktivasi:
  Pencuri mencuri iPhone
  → Melakukan reset pabrik (Pengaturan atau iTunes/Finder)
  → Mengatur perangkat dengan Apple ID mereka sendiri
  → Menjual atau menggunakan perangkat dengan bebas

DENGAN Kunci Aktivasi:
  Pencuri mencuri iPhone
  → Mencoba reset pabrik
  → Perangkat mencapai layar Kunci Aktivasi saat penyiapan
  → Memerlukan email Apple ID asli + kata sandi
  → Pencuri tidak dapat melanjutkan tanpa kredensial
  → Perangkat tidak dapat digunakan untuk dijual atau digunakan kembali
  → Insentif ekonomi pencurian berkurang secara signifikan
```

### Layar Kunci Aktivasi

Perangkat dengan Kunci Aktivasi yang diaktifkan menampilkan layar ini saat penyiapan:

```
┌────────────────────────────────────────────┐
│             Kunci Aktivasi                 │
│                                            │
│   iPhone ini ditautkan ke Apple ID        │
│                                            │
│   Email: [Apple ID pemilik]                │
│   Kata Sandi: ________                     │
│                                            │
│       [Buka Kunci dengan Apple ID]         │
│                                            │
└────────────────────────────────────────────┘
```

Bahkan setelah penghapusan lengkap melalui iTunes/Finder di komputer, layar Kunci Aktivasi muncul selama proses penyiapan perangkat.

---

## Memeriksa Status Kunci Aktivasi

### Sebelum Membeli iPhone Bekas

Sebelum membeli iPhone bekas, verifikasi tidak memiliki Kunci Aktivasi aktif:

**Metode 1: Periksa perangkat langsung**
- Jika perangkat boot ke layar Kunci Aktivasi, perangkat terkunci
- Perangkat tidak dapat digunakan tanpa kredensial Apple ID pemilik sebelumnya

**Metode 2: Periksa IMEI secara online**
1. Dapatkan IMEI perangkat (tekan `*#06#` atau periksa Pengaturan > Umum > Tentang)
2. Buka: **https://checkcoverage.apple.com**
3. Masukkan IMEI atau nomor seri
4. Ini menampilkan status garansi tetapi tidak langsung menampilkan status Kunci Aktivasi

**Metode 3: Pemeriksaan Status Kunci Aktivasi Apple (untuk MDM)**
Apple menyediakan API untuk administrator MDM untuk memeriksa status Kunci Aktivasi berdasarkan IMEI/seri.

> **⚠️ PERINGATAN:** Jangan beli iPhone bekas yang boot ke layar Kunci Aktivasi. Penjual tidak dapat secara sah membukanya tanpa Apple ID asli. Penjual mana pun yang mengklaim dapat menghapus Kunci Aktivasi dari jarak jauh dengan bayaran adalah penipuan.

---

## Menghapus Kunci Aktivasi (Metode Sah)

### Metode 1: Hapus melalui iCloud.com (Jarak Jauh)

Jika Anda tidak lagi memiliki akses fisik ke perangkat:

1. Buka **https://www.icloud.com/find**
2. Masuk dengan Apple ID yang tertaut ke perangkat
3. Pilih perangkat
4. Klik **Hapus Perangkat Ini** (jika belum dihapus)
5. Setelah penghapusan selesai, klik **Hapus dari Akun**

Ini menghapus Kunci Aktivasi dari jarak jauh, memungkinkan orang berikutnya mengatur perangkat.

### Metode 2: Keluar di Perangkat

Sebelum menjual atau memberikan iPhone Anda:

1. Buka **Pengaturan**
2. Ketuk nama Anda (Apple ID)
3. Gulir ke bawah dan ketuk **Keluar**
4. Masukkan kata sandi Apple ID Anda
5. Ikuti petunjuk untuk menyelesaikan keluar
6. Kemudian lakukan reset pabrik melalui Pengaturan > Umum > Transfer atau Reset iPhone > Hapus Semua Konten dan Pengaturan

### Metode 3: Di Apple Store

Jika Anda telah kehilangan akses ke Apple ID dan tidak dapat masuk dari jarak jauh:
- Kunjungi Apple Store dengan **bukti pembelian** (tanda terima asli, faktur)
- Apple dapat menghapus Kunci Aktivasi dengan dokumentasi kepemilikan yang terverifikasi
- Tanpa bukti pembelian, Apple tidak dapat menghapus Kunci Aktivasi

> **💡 TIPS:** Simpan tanda terima pembelian perangkat asli Anda di lokasi yang aman (email ke diri sendiri, simpan di folder cloud aman). Ini adalah satu-satunya dokumentasi yang dapat membuktikan kepemilikan ke Apple jika Anda kehilangan akses Apple ID.

---

## Kunci Aktivasi dan MDM (Enterprise)

Untuk perangkat korporat yang dikelola melalui **Apple Business Manager (ABM)** atau **Apple School Manager (ASM)**:

- Perangkat yang terdaftar di ABM/ASM dapat memiliki Kunci Aktivasi yang dikelola oleh administrator MDM
- Administrator dapat menonaktifkan Kunci Aktivasi untuk perangkat organisasi selama pendaftaran
- Ketika perangkat yang dikelola dihapus, perangkat dapat didaftarkan ulang tanpa memerlukan Apple ID pengguna sebelumnya
- MDM juga dapat menghasilkan kode bypass untuk membuka Kunci Aktivasi pada perangkat yang dikelola

*Referensi: https://support.apple.com/guide/apple-business-manager/about-activation-lock*

---

## Status Perbaikan iOS 17.5 dan Kunci Aktivasi

Di **iOS 17.5**, Apple memperkenalkan **Status Perbaikan**:
- iPhone dapat dikirim untuk servis tanpa menghapus Kunci Aktivasi
- Perangkat tetap dapat dilacak melalui Find My selama perbaikan
- Teknisi perbaikan tidak dapat menghapus perangkat tanpa Apple ID pemilik
- Kunci Aktivasi bertahan sepanjang proses perbaikan

Ini mencegah akses data yang tidak sah selama perbaikan pihak ketiga atau Apple.

---

## Kunci Aktivasi TIDAK Melindungi Terhadap

| Ancaman | Perlindungan Kunci Aktivasi? | Pertahanan Tambahan yang Diperlukan |
|---|---|---|
| Akses data dari perangkat yang tidak terkunci | Tidak | PIN kuat, Perlindungan Perangkat Dicuri |
| Pelepasan dan penggunaan kartu SIM | Tidak | PIN SIM |
| Akses data iCloud melalui kredensial yang dicuri | Tidak | Kata sandi Apple ID kuat + 2FA |
| Gangguan fisik (serangan chips-off) | Tidak | Enkripsi disk penuh (AES-256 di iOS) |
| Menjual perangkat dengan harga lebih rendah | Tidak | Kunci Aktivasi tetap mengurangi nilai jual kembali |

---

## Daftar Periksa: Praktik Terbaik Kunci Aktivasi

- [ ] Find My diaktifkan di perangkat (otomatis mengaktifkan Kunci Aktivasi)
- [ ] Apple ID memiliki kata sandi yang kuat
- [ ] Apple ID memiliki autentikasi dua faktor yang diaktifkan
- [ ] Kata sandi Apple ID disimpan di pengelola kata sandi aman (bukan hanya di perangkat)
- [ ] Bukti pembelian asli disimpan dengan aman
- [ ] Saat menjual perangkat: Keluar dari Apple ID sebelum mentransfer

---

## Dokumen Terkait

- [Find My](find-my.md)
- [Mode Hilang](lost-mode.md)
- [Perlindungan Perangkat Dicuri](stolen-device-protection.md)
- [Pemulihan Apple ID](apple-id-recovery.md)
- [MDM Enterprise](../hardening/mdm-enterprise.md)

---

*Terakhir Diperbarui: 2026-06-01 | Sumber: https://support.apple.com/en-us/108794*
