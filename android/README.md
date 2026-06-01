# Keamanan Android & Respons Kehilangan

> Terakhir Diperbarui: 2026-06-01

## Ikhtisar

Bagian ini mencakup fitur keamanan khusus Android, konfigurasi, dan prosedur respons kehilangan. Android adalah sistem operasi mobile yang paling banyak digunakan di dunia, berjalan pada perangkat dari Google, Samsung, Motorola, OnePlus, dan ratusan produsen lainnya.

---

## Arsitektur Keamanan Android

Model keamanan Android dibangun di atas beberapa lapisan yang saling terhubung:

```
┌──────────────────────────────────────────────────────────┐
│                  LAPISAN DATA PENGGUNA                   │
│        Aplikasi, File, Kredensial, Cadangan              │
├──────────────────────────────────────────────────────────┤
│                  LAPISAN APLIKASI                        │
│       Play Store, Aplikasi Sideload, Aplikasi MDM        │
├──────────────────────────────────────────────────────────┤
│                LAPISAN LAYANAN GOOGLE                    │
│    Play Protect, Find Hub, Akun Google, Identity Check   │
├──────────────────────────────────────────────────────────┤
│               LAPISAN SISTEM OPERASI ANDROID             │
│   SELinux, Verified Boot, Enkripsi, Keystore             │
├──────────────────────────────────────────────────────────┤
│                LAPISAN PERANGKAT KERAS                   │
│   Titan M / StrongBox, Secure Enclave, TrustZone        │
└──────────────────────────────────────────────────────────┘
```

---

## Isi Bagian Ini

| Dokumen | Deskripsi |
|---|---|
| [Find Hub (sebelumnya Find My Device)](find-my-device.md) | Melacak, mengunci, dan menghapus perangkat Android dari jarak jauh |
| [Perlindungan Reset Pabrik (FRP)](factory-reset-protection.md) | Bagaimana FRP mencegah pencuri menghapus dan menggunakan kembali perangkat Anda |
| [Keamanan Akun Google](google-account-security.md) | Mengamankan Akun Google yang mengendalikan perangkat Anda |
| [Play Protect](play-protect.md) | Layanan pemindaian malware bawaan Google |
| [Pemeriksaan Identitas](identity-check.md) | Fitur Android 15+ berupa kunci biometrik untuk pengaturan sensitif di luar lokasi tepercaya |

---

## Fitur Anti-Pencurian Sekilas (Android 10–15+)

| Fitur | Versi Android | Deskripsi |
|---|---|---|
| Perlindungan Reset Pabrik | 5.1+ | Memerlukan akun Google setelah reset tidak sah |
| Find Hub (Find My Device) | Semua (melalui Play Services) | Pelacakan, kunci, dan hapus jarak jauh |
| Smart Lock | 5.0+ | Lokasi/perangkat tepercaya melonggarkan kunci layar |
| Kunci Deteksi Pencurian | 10+ | AI mendeteksi pencurian sambaran, layar otomatis terkunci |
| Kunci Perangkat Offline | 10+ | Otomatis mengunci jika perangkat offline setelah dicuri |
| Kunci Jarak Jauh (tanpa internet) | 10+ | Kunci melalui SMS atau kredensial tersimpan |
| Pemeriksaan Identitas | 15+ (Pixel, Samsung) | Akses hanya biometrik ke pengaturan di luar lokasi tepercaya |

---

## Catatan Dukungan Versi

> **⚠️ PERINGATAN:** Perangkat yang menjalankan Android 9 atau lebih lama tidak lagi menerima pembaruan keamanan dari Google. Jika perangkat Anda tidak dapat diperbarui ke setidaknya Android 12, pertimbangkan untuk menggantinya. Tanpa pembaruan keamanan, kerentanan tetap tidak ditambal selamanya.

- **Android 15+**: Pemeriksaan Identitas, perlindungan pencurian yang ditingkatkan
- **Android 12+**: Izin lokasi perkiraan, Dasbor Privasi
- **Android 10+**: Penyimpanan Terbatas, izin ditingkatkan, Kunci Deteksi Pencurian
- **Android 9 (Pie)**: Akhir dukungan keamanan Google

---

## Tindakan Cepat untuk Perangkat Android yang Hilang

1. Buka **https://myaccount.google.com/find-your-phone** atau gunakan aplikasi Find Hub di perangkat lain
2. Pilih perangkat Anda
3. Pilih **Amankan Perangkat** untuk mengunci dengan PIN dan menampilkan pesan
4. Jika pemulihan tidak mungkin: pilih **Hapus Perangkat**

Untuk instruksi langkah demi langkah, lihat [5 Menit Pertama](../incident-response/first-5-minutes.md).

---

## Bagian Terkait

- [Panduan Penguatan Android](../hardening/android-hardening.md)
- [Daftar Periksa Penguatan Android](../checklists/android-hardening-checklist.md)
- [Keamanan SIM](../hardening/sim-security.md)

---

*Terakhir Diperbarui: 2026-06-01 | Referensi: https://support.google.com/android, https://security.googleblog.com*
