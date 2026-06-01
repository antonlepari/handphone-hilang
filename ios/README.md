# Keamanan iOS & Respons Kehilangan

> Terakhir Diperbarui: 2026-06-01

## Ikhtisar

Bagian ini mencakup fitur keamanan khusus iOS, konfigurasi, dan prosedur respons kehilangan untuk iPhone. Platform iOS Apple dirancang dengan privasi dan keamanan sebagai prinsip dasar, dan mencakup beberapa fitur anti-pencurian yang kuat yang, ketika dikonfigurasi dengan benar, membuat iPhone yang dicuri jauh kurang berguna bagi penyerang.

---

## Arsitektur Keamanan iOS

```
┌──────────────────────────────────────────────────────────────┐
│                    LAPISAN DATA PENGGUNA                      │
│          Aplikasi, Foto, Kesehatan, Pesan, Kontak            │
├──────────────────────────────────────────────────────────────┤
│                   LAPISAN APLIKASI                           │
│           App Store, iCloud, Aplikasi Pihak Ketiga           │
├──────────────────────────────────────────────────────────────┤
│                  LAPISAN LAYANAN APPLE                       │
│   Find My, Perlindungan Perangkat Dicuri, Apple ID, iCloud   │
├──────────────────────────────────────────────────────────────┤
│                      LAPISAN iOS                             │
│   Secure Enclave, Kelas Perlindungan Data, Gatekeeper        │
├──────────────────────────────────────────────────────────────┤
│                   LAPISAN PERANGKAT KERAS                    │
│   Prosesor Secure Enclave (SEP), Face ID / Touch ID         │
└──────────────────────────────────────────────────────────────┘
```

---

## Isi Bagian Ini

| Dokumen | Deskripsi |
|---|---|
| [Find My](find-my.md) | Platform pelacakan dan pemulihan perangkat Apple |
| [Mode Hilang](lost-mode.md) | Mengunci dan mengirim pesan ke iPhone yang hilang |
| [Kunci Aktivasi](activation-lock.md) | Mencegah penggunaan tidak sah setelah reset pabrik |
| [Perlindungan Perangkat Dicuri](stolen-device-protection.md) | Perlindungan iOS 17.3+ terhadap pencurian yang diamati kode sandinya |
| [Pemulihan Apple ID](apple-id-recovery.md) | Mendapatkan kembali akses akun setelah kehilangan |

---

## Fitur Anti-Pencurian iOS Sekilas

| Fitur | Versi iOS | Deskripsi |
|---|---|---|
| Kunci Aktivasi | iOS 7+ | Memerlukan Apple ID setelah reset pabrik ketika Find My aktif |
| Find My | iOS 8+ | Lacak, kunci, dan hapus perangkat dari jarak jauh |
| Mode Hilang | iOS 6+ | Kunci perangkat dan tampilkan info kontak |
| Perlindungan Perangkat Dicuri | iOS 17.3+ | Akses hanya biometrik; penundaan 1 jam untuk perubahan kritis di luar lokasi familiar |
| Mode Penguncian | iOS 16+ | Penguatan ekstrem untuk pengguna berisiko tinggi (jurnalis, aktivis) |

---

## Catatan Dukungan Versi

> **⚠️ PERINGATAN:** Perangkat yang tidak dapat diperbarui ke setidaknya iOS 16 tidak lagi menerima patch keamanan. Apple secara rutin menemukan dan menambal kerentanan kritis. Menjalankan versi iOS yang kedaluwarsa membuat Anda rentan terhadap eksploitasi yang diketahui.

| Perangkat | iOS Terbaru yang Didukung |
|---|---|
| iPhone 16 series | iOS 18+ |
| iPhone 15 series | iOS 18+ |
| iPhone 14 series | iOS 18+ |
| iPhone 13 series | iOS 18+ |
| iPhone 12 series | iOS 18+ |
| iPhone 11 series | iOS 18+ |
| iPhone XS / XS Max | iOS 18+ |
| iPhone XR | iOS 18+ |
| iPhone X | iOS 16 (akhir dukungan) |
| iPhone 8 / 8 Plus | iOS 16 (akhir dukungan) |
| iPhone 7 / 7 Plus | iOS 15 (akhir dukungan) |

---

## Tindakan Cepat untuk iPhone yang Hilang

1. Buka aplikasi **Find My** di perangkat Apple lain, atau buka **https://icloud.com/find**
2. Masuk dengan Apple ID Anda
3. Pilih iPhone yang hilang
4. Ketuk **Tandai sebagai Hilang** untuk mengaktifkan Mode Hilang
5. Tambahkan nomor telepon dan pesan untuk ditampilkan di layar kunci
6. Jika pemulihan tidak mungkin: ketuk **Hapus Perangkat Ini**

Untuk instruksi langkah demi langkah, lihat [5 Menit Pertama](../incident-response/first-5-minutes.md).

---

## Bagian Terkait

- [Panduan Penguatan iOS](../hardening/ios-hardening.md)
- [Daftar Periksa Penguatan iOS](../checklists/ios-hardening-checklist.md)
- [Keamanan SIM](../hardening/sim-security.md)

---

*Terakhir Diperbarui: 2026-06-01 | Referensi: https://support.apple.com | https://developer.apple.com/security*
