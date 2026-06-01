# 30 Menit Pertama — Respons Insiden

> Terakhir Diperbarui: 2026-06-01

## Tujuan Fase Ini

Pada fase ini, fokus bergeser dari **penahanan perangkat** ke **perlindungan akun dan keuangan**:
- Ubah kata sandi akun kritis
- Hubungi operator untuk menangguhkan SIM
- Amankan akun perbankan dan keuangan
- Siapkan laporan polisi

---

## Prasyarat

Pastikan [5 Menit Pertama](first-5-minutes.md) sudah diselesaikan:
- [ ] Perangkat sudah dikunci (Mode Hilang / Amankan Perangkat aktif)
- [ ] Sesi perangkat hilang sudah dicabut dari Akun Google / Apple ID

---

## Langkah 1: Ubah Kata Sandi Akun Utama

Lakukan dari perangkat atau komputer **yang bukan perangkat yang hilang**.

### Google Account

1. Buka **https://myaccount.google.com/security**
2. Klik **Kata Sandi**
3. Masukkan kata sandi baru yang kuat dan unik
4. Gunakan pengelola kata sandi untuk membuat kata sandi acak

### Apple ID

1. Buka **https://appleid.apple.com**
2. Masuk ke akun Anda
3. Buka **Masuk & Keamanan > Kata Sandi**
4. Ubah kata sandi

### Email Utama (Gmail, Outlook, dll.)

Ubah kata sandi email utama Anda — ini adalah akun yang paling kritis karena dapat digunakan untuk mereset semua akun lainnya.

> **⚠️ PERINGATAN:** Jangan gunakan kata sandi yang sama untuk beberapa akun. Gunakan kata sandi unik untuk setiap akun.

---

## Langkah 2: Hubungi Operator Seluler

Segera tangguhkan SIM untuk mencegah:
- Penerimaan kode OTP/2FA oleh pencuri
- Penggunaan kuota data
- Panggilan dan SMS tidak sah
- Potensi serangan SIM swap

### Nomor Operator Indonesia

| Operator | Nomor Layanan | Cara Lapor |
|---|---|---|
| Telkomsel | 188 | Telepon langsung, laporkan SIM hilang/dicuri |
| Indosat Ooredoo | 185 | Telepon, minta suspend kartu |
| XL Axiata | 817 | Telepon, minta blokir kartu |
| Smartfren | 881 | Telepon, laporkan kehilangan |
| Tri (3) | 132 | Telepon, minta suspend |
| AXIS | 838 | Telepon, minta blokir SIM |

**Informasi yang perlu disiapkan saat menelepon operator:**
- Nama lengkap pemilik kartu
- Nomor KTP
- Nomor SIM yang hilang
- Nomor account/pelanggan (jika ada)
- Tanggal dan lokasi kehilangan

> **💡 TIPS:** Minta operator untuk melakukan **pemblokiran IMEI** sekaligus, bukan hanya suspend SIM. Ini mencegah perangkat yang dicuri digunakan dengan SIM lain.

---

## Langkah 3: Amankan Akun Keuangan

Ini adalah langkah yang paling mendesak untuk mencegah kerugian finansial.

### Aplikasi Perbankan

1. Masuk ke akun bank dari browser web atau aplikasi di perangkat lain
2. Ubah kata sandi internet banking
3. Ubah PIN aplikasi mobile banking (jika ada opsi di web)
4. Aktifkan notifikasi transaksi real-time
5. Periksa riwayat transaksi 24 jam terakhir untuk transaksi mencurigakan

### Dompet Digital (GoPay, OVO, Dana, ShopeePay, dll.)

Untuk setiap dompet digital:
1. Masuk dari browser web atau perangkat lain
2. Ubah kata sandi / PIN
3. Cabut sesi aktif jika ada opsi
4. Hubungi CS jika tidak bisa akses dari luar perangkat

| Platform | Layanan CS |
|---|---|
| GoPay | 1500696 atau aplikasi Gojek |
| OVO | 1500696 atau chat di aplikasi |
| Dana | 1500080 |
| ShopeePay | Help Center Shopee |

### Kartu Kredit / Debit

Hubungi bank penerbit dan:
- Laporkan kehilangan perangkat yang menyimpan data kartu
- Minta pemantauan transaksi ekstra
- Pertimbangkan memblokir sementara jika kartu tersimpan di dompet digital perangkat

---

## Langkah 4: Aktifkan 2FA yang Lebih Kuat

Jika Anda selama ini menggunakan 2FA berbasis SMS, **sekarang adalah waktu yang tepat untuk beralih** ke aplikasi autentikator, karena SIM Anda mungkin sudah tidak aman:

1. Instal aplikasi autentikator di perangkat pengganti
   - Google Authenticator, Microsoft Authenticator, atau Authy
2. Aktifkan TOTP untuk email, akun Google/Apple ID, dan perbankan
3. Hapus SMS sebagai metode 2FA setelah autentikator terdaftar

---

## Langkah 5: Persiapkan Laporan Polisi

Siapkan informasi berikut sebelum ke kantor polisi (atau laporan online):

```
INFORMASI YANG DIBUTUHKAN UNTUK LAPORAN POLISI:
├── Identitas Pemilik
│   ├── Nama lengkap
│   ├── Nomor KTP
│   └── Alamat
├── Data Perangkat
│   ├── Merek dan model
│   ├── Nomor IMEI (*#06# atau Settings > About)
│   ├── Nomor seri (jika ada)
│   └── Warna dan kondisi fisik
└── Detail Kejadian
    ├── Tanggal dan waktu kehilangan
    ├── Lokasi kejadian
    └── Deskripsi kejadian (hilang / dicuri)
```

Laporan polisi diperlukan untuk:
- Klaim asuransi perangkat
- Pemblokiran IMEI di operator
- Dokumentasi resmi jika ada penyalahgunaan identitas

---

## Ringkasan Timeline 30 Menit

```
MENIT 5-10:   Ubah kata sandi Google/Apple ID dan email utama
MENIT 10-15:  Hubungi operator, suspend SIM
MENIT 15-20:  Amankan akun perbankan dan dompet digital
MENIT 20-25:  Aktifkan 2FA aplikasi autentikator
MENIT 25-30:  Kumpulkan data untuk laporan polisi
```

---

## Langkah Berikutnya

Setelah 30 menit pertama selesai, lanjutkan ke:
- [Jam Pertama](first-hour.md) — Laporan resmi, keputusan hapus jarak jauh, IMEI blacklist

---

*Terakhir Diperbarui: 2026-06-01*
