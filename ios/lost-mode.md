# Mode Hilang — iOS

> Terakhir Diperbarui: 2026-06-01

## Ikhtisar

**Mode Hilang** adalah fitur iOS yang diaktifkan melalui Find My yang mengunci iPhone Anda dan menampilkan pesan kustom beserta informasi kontak Anda di layar kunci. Fitur ini dirancang untuk melindungi data perangkat sekaligus meningkatkan kemungkinan pemulihan dengan memungkinkan penemu menghubungi Anda tanpa membuka kunci ponsel.

Mode Hilang berbeda dari penghapusan jarak jauh — ini menjaga data Anda tetap aman sambil melindungi aksesnya.

*Referensi: https://support.apple.com/en-us/105072*

---

## Apa yang Dilakukan Mode Hilang

Ketika Anda mengaktifkan Mode Hilang pada iPhone yang hilang:

| Tindakan | Efek |
|---|---|
| **Kunci layar** | Perangkat segera dikunci dengan kode sandi yang ada |
| **Pesan kustom** | Pesan pilihan Anda muncul di layar kunci (mis., "iPhone ini hilang. Hubungi +62-XXX-XXXX") |
| **Telepon kontak** | Nomor telepon opsional ditampilkan yang dapat dihubungi siapa saja langsung dari layar kunci, tanpa membuka kunci |
| **Pelacakan lokasi** | Perangkat terus melaporkan lokasi GPS ke Find My |
| **Apple Pay / Dompet** | Dinonaktifkan — kartu, tiket transit, kunci mobil tidak dapat digunakan |
| **Pemasangan aksesori** | Aksesori baru (Bluetooth, USB) tidak dapat dipasangkan |
| **Notifikasi** | Notifikasi aplikasi yang ada tersembunyi dari layar kunci |
| **Perlindungan data** | Semua data tetap ada di perangkat dan dilindungi oleh kode sandi |

> **ℹ️ CATATAN:** Mode Hilang **tidak** menghapus data Anda. Ini mengunci perangkat. Data tetap utuh dan dapat diakses kembali ketika Anda memasukkan kode sandi yang benar setelah pemulihan.

---

## Apa yang Dilihat Penemu atau Pencuri

Ketika seseorang mengambil iPhone dalam Mode Hilang, mereka melihat:

```
┌─────────────────────────────────────────────┐
│                                             │
│               [Layar Kunci]                 │
│                                             │
│   ┌─────────────────────────────────────┐   │
│   │    iPhone ini telah hilang.         │   │
│   │    Hubungi +62-XXX-XXXX             │   │
│   │    jika ditemukan.                  │   │
│   └─────────────────────────────────────┘   │
│                                             │
│   Tombol [Hubungi] (menelepon tanpa         │
│   membuka kunci)                            │
│                                             │
│              Masukkan Kode Sandi            │
└─────────────────────────────────────────────┘
```

Mereka tidak dapat:
- Mengakses aplikasi atau data apa pun
- Menggunakan Apple Pay
- Memasangkan perangkat Bluetooth
- Menghapus pesan Mode Hilang tanpa Apple ID Anda

---

## Cara Mengaktifkan Mode Hilang

### Melalui iCloud.com

1. Buka **https://www.icloud.com/find**
2. Masuk dengan Apple ID Anda
3. Klik perangkat yang hilang pada peta atau daftar perangkat
4. Klik **Tandai sebagai Hilang** (atau **Aktifkan** di bawah bagian "Tandai sebagai Hilang")
5. Klik **Lanjutkan**
6. Masukkan nomor telepon tempat Anda dapat dihubungi
7. Masukkan pesan untuk ditampilkan (opsional — pesan default ditampilkan jika dibiarkan kosong)
8. Klik **Aktifkan**

### Melalui Aplikasi Find My (Perangkat Apple Lain)

1. Buka aplikasi **Find My**
2. Ketuk tab **Perangkat**
3. Ketuk perangkat yang hilang
4. Gulir ke bawah dan ketuk **Tandai sebagai Hilang**
5. Ketuk **Lanjutkan**
6. Masukkan nomor telepon dan pesan opsional
7. Ketuk **Aktifkan**

![Aktivasi Mode Hilang](../images/ios-lost-mode-activation.png)
*Gambar 1: Mengaktifkan Mode Hilang melalui iCloud.com — klik Tandai sebagai Hilang, masukkan informasi kontak*

---

## Mode Hilang dan Pelacakan Lokasi

Setelah Mode Hilang diaktifkan, Find My akan menampilkan:
- **Lokasi real-time** di peta (jika perangkat memiliki konektivitas internet)
- **Lokasi terakhir yang diketahui** dengan stempel waktu (jika perangkat offline)
- **Riwayat lokasi** yang menunjukkan pergerakan dari waktu ke waktu

Anda akan menerima notifikasi di perangkat Apple lain ketika iPhone yang hilang ditemukan.

---

## Mematikan Mode Hilang

Ketika Anda memulihkan perangkat:

1. Masukkan kode sandi perangkat Anda di iPhone — ini secara otomatis menonaktifkan Mode Hilang
2. Atau, buka aplikasi Find My / iCloud.com dan pilih **Matikan Tandai sebagai Hilang**

---

## Mode Hilang Setelah Baterai Habis

Jika baterai perangkat habis saat dalam Mode Hilang:
- Mode Hilang tetap aktif — perangkat tidak secara otomatis keluar dari Mode Hilang ketika baterai habis
- Ketika perangkat diisi daya dan dihidupkan, perangkat akan tetap dalam Mode Hilang
- "Kirim Lokasi Terakhir" (jika diaktifkan) akan merekam lokasi GPS terakhir sebelum mati

---

## Mode Hilang vs. Hapus Jarak Jauh

Gunakan matriks keputusan ini untuk memilih tindakan yang tepat:

```
PERANGKAT HILANG — TINDAKAN MANA?

Apakah pemulihan masih mungkin?
├── YA, perangkat ada di dekatnya → Putar Suara
├── MUNGKIN, perangkat berada di tempat yang dapat dilacak → Tandai sebagai Hilang
└── TIDAK, atau data sangat sensitif → Hapus Perangkat

Apakah ini perangkat korporat?
├── YA → Konsultasikan dengan IT / kebijakan MDM sebelum menghapus
└── TIDAK → Gunakan penilaian pribadi

Apakah perangkat berisi data yang tidak tergantikan?
├── YA (tidak ada cadangan) → Tandai sebagai Hilang terlebih dahulu; beli waktu
└── TIDAK (cadangan terkini ada) → Penghapusan adalah pilihan yang aman
```

> **⚠️ PERINGATAN:** Setelah Anda menghapus perangkat, Anda tidak dapat lagi melacaknya melalui Find My. Gunakan "Tandai sebagai Hilang" terlebih dahulu untuk memantau lokasi, kemudian hapus jika pemulihan menjadi tidak mungkin.

---

## Notifikasi Mode Hilang

Anda dapat mengonfigurasi notifikasi untuk:
- Perangkat ditemukan
- Baterai perangkat lemah
- Perangkat terhubung ke jaringan

Notifikasi ini membantu Anda memantau status perangkat tanpa harus berulang kali memeriksa Find My.

---

## Dokumen Terkait

- [Find My](find-my.md)
- [Kunci Aktivasi](activation-lock.md)
- [Perlindungan Perangkat Dicuri](stolen-device-protection.md)
- [5 Menit Pertama](../incident-response/first-5-minutes.md)
- [Daftar Periksa Darurat](../checklists/emergency-checklist.md)

---

*Terakhir Diperbarui: 2026-06-01 | Sumber: https://support.apple.com/en-us/105072*
