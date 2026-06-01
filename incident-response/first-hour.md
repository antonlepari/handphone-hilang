# Jam Pertama — Respons Insiden

> Terakhir Diperbarui: 2026-06-01

## Tujuan Fase Ini

Pada fase jam pertama, fokus adalah **pelaporan resmi dan keputusan strategis**:
- Membuat laporan polisi
- Pemblokiran IMEI di operator
- Keputusan hapus jarak jauh
- Notifikasi asuransi
- Respons perangkat korporat (jika berlaku)

---

## Langkah 1: Buat Laporan Polisi

Segera setelah menstabilkan akun keuangan, buat laporan polisi resmi.

### Di Indonesia

**Cara melapor:**
- Datang langsung ke **Kantor Polisi terdekat** (Polsek/Polres)
- Atau lapor online melalui: **https://www.polri.go.id** (layanan laporan online)
- Atau hubungi: **110** (darurat polisi)

**Dokumen yang dibawa:**
- KTP asli
- Data perangkat (IMEI, merek, model, foto perangkat jika ada)
- Bukti kepemilikan (nota pembelian, kotak perangkat)
- Kronologi kejadian tertulis

**Yang akan Anda terima:**
- **Nomor Laporan Polisi (LP)** — simpan ini, diperlukan untuk klaim asuransi dan pemblokiran IMEI resmi

Lihat: [Template Laporan Polisi](../templates/police-report-template.md)

---

## Langkah 2: Pemblokiran IMEI

Setelah memiliki nomor laporan polisi, hubungi operator untuk **pemblokiran IMEI permanen**:

- IMEI yang diblokir tidak dapat digunakan di jaringan operator mana pun di Indonesia
- Pemblokiran berlaku lintas operator (sejak regulasi IMEI Indonesia 2020)
- Diperlukan: Nomor LP, KTP, dan nomor IMEI

**Regulasi IMEI Indonesia:**
Berdasarkan Peraturan Menteri Kominfo No. 1/2020, perangkat dengan IMEI tidak terdaftar atau diblokir tidak dapat terhubung ke jaringan seluler di Indonesia.

*Referensi: https://imei.kemenperin.go.id*

---

## Langkah 3: Matriks Keputusan Hapus Jarak Jauh

Ini adalah keputusan paling kritis yang harus dibuat dengan cermat:

```
KEPUTUSAN HAPUS JARAK JAUH

1. Apakah pemulihan fisik masih mungkin dalam waktu dekat?
   ├── YA → Kunci saja, pantau lokasi, TUNDA penghapusan
   └── TIDAK → Lanjut ke pertanyaan 2

2. Apakah perangkat berisi data sangat sensitif?
   ├── YA (data korporat, kredensial, foto pribadi sensitif)
   │   └── HAPUS SEKARANG
   └── TIDAK (data umum, ada backup lengkap)
       └── Pertimbangkan menunggu 24-48 jam sambil melacak

3. Apakah ini perangkat korporat?
   ├── YA → JANGAN hapus tanpa otorisasi IT
   │         (bisa menghancurkan bukti forensik)
   └── TIDAK → Ikuti keputusan di atas
```

### Cara Hapus Jarak Jauh

**Android:**
1. Buka https://android.com/find
2. Pilih perangkat
3. Klik **Hapus Perangkat**
4. Konfirmasi tindakan

**iOS:**
1. Buka https://icloud.com/find
2. Pilih perangkat
3. Klik **Hapus Perangkat Ini**
4. Konfirmasi dengan Apple ID

> **⚠️ PERINGATAN:** Setelah penghapusan jarak jauh dilakukan, pelacakan lokasi tidak lagi tersedia. Pastikan Anda sudah:
> - Memiliki nomor LP polisi
> - Sudah backup data penting sebelumnya
> - Yakin perangkat tidak akan dapat dipulihkan

---

## Langkah 4: Hubungi Asuransi Perangkat

Jika perangkat diasuransikan, segera lapor:

| Jenis Asuransi | Cara Klaim |
|---|---|
| **AppleCare+** (dengan cakupan pencurian) | https://support.apple.com atau 1-800-APL-CARE |
| **Asuransi operator** | Hubungi operator dengan nomor LP |
| **Asuransi gadget swasta** | Hubungi perusahaan asuransi, siapkan LP + bukti kepemilikan |
| **Asuransi kartu kredit** (jika perangkat dibeli dengan kartu) | Hubungi bank penerbit kartu |

**Dokumen yang biasanya dibutuhkan untuk klaim:**
- Nomor laporan polisi (LP)
- Bukti kepemilikan (nota pembelian / e-receipt)
- Foto perangkat
- IMEI perangkat

---

## Langkah 5: Notifikasi Perangkat Korporat

Jika perangkat yang hilang adalah perangkat korporat atau menyimpan data kerja:

```
SEGERA (dalam jam pertama):
1. Hubungi IT Security / Help Desk perusahaan
2. Berikan: waktu kejadian, lokasi, data perangkat (IMEI, nomor aset)
3. IT akan melakukan: remote wipe via MDM, cabut akses VPN/email
4. Hubungi manajer langsung Anda
5. Dokumentasikan semua tindakan yang sudah diambil

JANGAN:
- Jangan hapus perangkat sendiri jika MDM aktif (bisa konflik)
- Jangan tunda laporan ke IT lebih dari 1 jam
- Jangan akses ulang data korporat dari perangkat pribadi tanpa izin
```

Lihat: [Respons Perangkat Korporat](corporate-device-response.md)

---

## Ringkasan Jam Pertama

| Waktu | Tindakan |
|---|---|
| Menit 30–40 | Buat laporan polisi (datang langsung atau online) |
| Menit 40–45 | Hubungi operator untuk pemblokiran IMEI |
| Menit 45–50 | Evaluasi dan jalankan hapus jarak jauh jika diperlukan |
| Menit 50–55 | Lapor ke asuransi perangkat |
| Menit 55–60 | Notifikasi IT korporat jika perangkat kerja |

---

## Langkah Berikutnya

- [24 Jam Pertama](first-24-hours.md) — Audit akun menyeluruh dan pemantauan penipuan

---

*Terakhir Diperbarui: 2026-06-01*
