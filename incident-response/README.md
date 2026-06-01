# Respons Insiden

> Terakhir Diperbarui: 2026-06-01

## Ikhtisar

Bagian ini menyediakan prosedur respons insiden terstruktur untuk perangkat mobile yang hilang atau dicuri. Prosedur diorganisir berdasarkan fase waktu, memungkinkan responden untuk mengidentifikasi tindakan yang tepat untuk tahap insiden mereka saat ini.

---

## Struktur Respons Insiden

```mermaid
flowchart LR
    A[Perangkat Hilang] --> B[5 Menit Pertama]
    B --> C[30 Menit Pertama]
    C --> D[Jam Pertama]
    D --> E[24 Jam Pertama]
    E --> F[Minggu Pertama]
    F --> G[Tinjauan Pasca-Insiden]
```

---

## Dokumen dalam Bagian Ini

| Dokumen | Fase Waktu | Tindakan Kunci |
|---|---|---|
| [Ikhtisar Playbook](playbook-overview.md) | Alur penuh | Diagram alur IR lengkap, pohon keputusan |
| [5 Menit Pertama](first-5-minutes.md) | 0–5 mnt | Lacak, kunci, keluar, beritahu |
| [30 Menit Pertama](first-30-minutes.md) | 5–30 mnt | Amankan akun, hubungi operator, buat laporan |
| [Jam Pertama](first-hour.md) | 30–60 mnt | Pelaporan IMEI, keputusan hapus jarak jauh, asuransi |
| [24 Jam Pertama](first-24-hours.md) | 1–24 jam | Audit akun penuh, pemantauan kredit |
| [Minggu Pertama](first-week.md) | 1–7 hari | Penyiapan perangkat baru, klaim asuransi, pelajaran dipetik |
| [Respons Perangkat Korporat](corporate-device-response.md) | Semua fase | Prosedur khusus enterprise |

---

## Keputusan Kritis: Hapus atau Tidak Hapus?

Salah satu keputusan terpenting dalam insiden kehilangan perangkat adalah apakah akan melakukan penghapusan jarak jauh. Gunakan kerangka kerja ini:

```
KEPUTUSAN HAPUS JARAK JAUH:

Apakah perangkat berisi data sensitif?
├── YA: Email kerja, data klien, kredensial, keuangan pribadi?
│   └── Apakah pemulihan perangkat masih mungkin?
│       ├── YA: Kunci terlebih dahulu, pantau lokasi, tunda penghapusan
│       └── TIDAK: Hapus segera
└── TIDAK: Hanya konten pribadi standar
    └── Apakah perangkat diasuransikan atau dapat diganti?
        ├── YA: Hapus dan klaim
        └── TIDAK: Kunci dan coba pemulihan

Perangkat korporat:
└── Ikuti kebijakan MDM/IT — JANGAN hapus tanpa otorisasi IT
    (Penghapusan dapat menghancurkan bukti forensik yang diperlukan untuk investigasi)
```

Untuk panduan keputusan terperinci, lihat [Jam Pertama — Matriks Keputusan Hapus Jarak Jauh](first-hour.md).

---

## Terminologi

| Istilah | Definisi |
|---|---|
| **Penahanan** | Membatasi kerusakan dari insiden (kunci jarak jauh, pencabutan sesi) |
| **Pemberantasan** | Menghilangkan ancaman (hapus jarak jauh, pemblokiran IMEI) |
| **Pemulihan** | Memulihkan operasi normal (perangkat baru, verifikasi akun) |
| **Pelajaran yang Dipetik** | Tinjauan pasca-insiden untuk mencegah pengulangan |

---

## Persyaratan Pelaporan

| Skenario | Notifikasi yang Diperlukan |
|---|---|
| Perangkat pribadi | Tidak diwajibkan secara hukum, tetapi beritahu bank, operator, dan asuransi |
| BYOD dengan data kerja | Segera beritahu IT/Keamanan pemberi kerja |
| Perangkat milik korporat | Beritahu IT Security, manajer, dan ikuti rencana IR organisasi |
| Pelanggaran data (data pribadi orang lain) | Mungkin memerlukan notifikasi regulasi (GDPR, UU PDP Indonesia) |
| Data layanan kesehatan | Notifikasi pelanggaran mungkin berlaku |

---

*Terakhir Diperbarui: 2026-06-01*
