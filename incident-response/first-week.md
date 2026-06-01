# Minggu Pertama — Respons Insiden

> Terakhir Diperbarui: 2026-06-01

## Tujuan Fase Ini

Pada minggu pertama, fokus adalah **pemulihan penuh dan pencegahan berulang**:
- Siapkan perangkat baru dengan konfigurasi aman
- Selesaikan klaim asuransi
- Lakukan evaluasi keamanan menyeluruh
- Terapkan pelajaran yang dipetik

---

## Langkah 1: Siapkan Perangkat Pengganti

### Membeli Perangkat Baru

**Pertimbangan keamanan saat membeli:**
- Pilih perangkat yang mendukung versi OS terbaru (Android 14+ atau iOS 17+)
- Verifikasi IMEI perangkat baru: tidak dalam daftar blokir
- Beli dari toko resmi atau distributor terpercaya
- Simpan bukti pembelian (nota/invoice) — diperlukan untuk klaim dan aktivasi garansi

**Verifikasi IMEI perangkat baru:**
- Android: Ketuk `*#06#`
- Cek di: https://imei.kemenperin.go.id (Indonesia)

### Pemulihan Data dari Cadangan

**Android:**
1. Nyalakan perangkat baru dan ikuti wizard penyiapan
2. Pilih **Pulihkan dari cadangan Google**
3. Masuk dengan Akun Google yang sama
4. Pilih cadangan terakhir yang valid
5. Tunggu proses pemulihan selesai

**iOS:**
1. Nyalakan iPhone baru dan mulai penyiapan
2. Pilih **Pulihkan dari Cadangan iCloud**
3. Masuk dengan Apple ID yang sama
4. Pilih cadangan terbaru
5. Tunggu pemulihan selesai

> **⚠️ PERINGATAN:** Verifikasi cadangan yang dipulihkan adalah dari **sebelum** perangkat hilang/dicuri. Jangan pulihkan cadangan yang dibuat setelah perangkat dicuri — bisa mengandung konfigurasi yang sudah disusupi.

---

## Langkah 2: Konfigurasi Keamanan Perangkat Baru

Sebelum menggunakan perangkat baru untuk aktivitas sensitif, konfigurasikan keamanan terlebih dahulu:

- [ ] Atur PIN/frasa sandi kuat (bukan 4 digit)
- [ ] Aktifkan biometrik (sidik jari / Face ID)
- [ ] Aktifkan Find My Device / Find My **segera**
- [ ] Aktifkan PIN SIM pada kartu SIM baru
- [ ] Aktifkan enkripsi perangkat (otomatis di Android 10+ dan iOS 8+ jika PIN diatur)
- [ ] Instal dan konfigurasikan pengelola kata sandi
- [ ] Aktifkan 2FA aplikasi autentikator untuk semua akun
- [ ] Aktifkan cadangan otomatis ke cloud

Untuk daftar periksa lengkap, lihat:
- [Daftar Periksa Penguatan Android](../checklists/android-hardening-checklist.md)
- [Daftar Periksa Penguatan iOS](../checklists/ios-hardening-checklist.md)

---

## Langkah 3: Aktifkan Kartu SIM Baru

Hubungi operator untuk mengaktifkan nomor lama di SIM baru:

1. Datang ke gerai operator dengan **KTP asli**
2. Minta **migrasi nomor** ke SIM baru
3. Tunjukkan nomor LP polisi sebagai bukti kehilangan
4. Operator akan menonaktifkan SIM lama dan mengaktifkan SIM baru dengan nomor yang sama

**Setelah SIM baru aktif:**
- Perbarui nomor telepon di akun-akun penting (bank, e-commerce, pemerintah)
- Beritahu kontak bahwa nomor sudah aktif kembali

---

## Langkah 4: Tindak Lanjut Klaim Asuransi

Jika perangkat diasuransikan, pantau proses klaim:

| Hari | Tindakan |
|---|---|
| Hari 1–2 | Kirim semua dokumen ke perusahaan asuransi |
| Hari 3–5 | Konfirmasi penerimaan dokumen |
| Hari 5–7 | Tindak lanjut status klaim |
| Minggu 2 | Eskalasi jika belum ada respons |

**Dokumen umum yang dibutuhkan:**
- Fotokopi KTP
- Nomor Laporan Polisi (LP)
- Nota/invoice pembelian perangkat
- Formulir klaim yang diisi
- Foto perangkat (jika ada)

---

## Langkah 5: Audit Keamanan Pasca-Insiden

Setelah situasi stabil, lakukan audit keamanan menyeluruh:

### Audit Akun (Hari 3–5)

- [ ] Periksa semua akun yang pernah login di perangkat lama
- [ ] Cabut sesi yang masih aktif di perangkat lama (jika belum dilakukan)
- [ ] Tinjau aplikasi pihak ketiga yang memiliki akses ke akun Google/Apple
- [ ] Hapus otorisasi aplikasi yang tidak dikenal atau tidak digunakan

### Audit Keamanan Email

- [ ] Periksa filter email yang mencurigakan (redirect, auto-forward)
- [ ] Periksa email tersimpan/draft yang tidak Anda buat
- [ ] Verifikasi opsi pemulihan (recovery email, nomor telepon)

### Audit Keuangan Lanjutan (Hari 5–7)

- [ ] Periksa laporan rekening bank penuh
- [ ] Verifikasi tidak ada pinjaman atau kredit baru atas nama Anda
- [ ] Pantau SLIK OJK untuk aktivitas kredit tidak sah

---

## Langkah 6: Pelajaran yang Dipetik

Dokumentasikan apa yang bisa diperbaiki untuk mencegah insiden serupa:

### Evaluasi Mandiri

Jawab pertanyaan berikut:

1. **Konfigurasi apa yang belum diaktifkan** sebelum kejadian? (Find My, PIN SIM, 2FA)
2. **Berapa lama waktu respons Anda?** Apa yang memperlambat?
3. **Data apa yang hilang** yang seharusnya ada di cadangan?
4. **Apakah PIN perangkat Anda cukup kuat?** Apakah pernah terlihat orang lain?
5. **Apakah ada akun yang belum diamankan** dalam 24 jam pertama?

### Tindakan Pencegahan untuk Masa Depan

Berdasarkan evaluasi, tambahkan ke daftar periksa pencegahan:
- [ ] Dokumentasikan IMEI perangkat baru segera
- [ ] Atur backup otomatis harian
- [ ] Aktifkan semua fitur anti-pencurian di perangkat baru
- [ ] Simpan kode IMEI dan nomor LP di tempat yang mudah diakses secara offline
- [ ] Pertimbangkan asuransi perangkat untuk perangkat baru

---

## Langkah 7: Perbarui Data di Instansi Resmi

Jika nomor telepon digunakan untuk keperluan resmi, perbarui data:

| Instansi | Cara Perbarui |
|---|---|
| **Bank** | Datang ke cabang atau update via aplikasi |
| **BPJS Kesehatan** | Aplikasi Mobile JKN atau kantor BPJS |
| **Dukcapil** (jika eSIM) | Lapor ke Dukcapil jika NIK terhubung ke eSIM |
| **Kantor pajak** | Perbarui nomor di akun DJP Online |
| **Tempat kerja** | Perbarui data kepegawaian |

---

## Ringkasan Minggu Pertama

| Hari | Prioritas |
|---|---|
| Hari 1–2 | Siapkan perangkat pengganti, aktifkan SIM baru |
| Hari 2–3 | Konfigurasi keamanan perangkat baru secara menyeluruh |
| Hari 3–5 | Tindak lanjut klaim asuransi, audit akun |
| Hari 5–7 | Audit keuangan lanjutan, pelajaran dipetik |
| Hari 7 | Perbarui data di instansi resmi |

---

## Dokumen Terkait

- [Sebelum Kehilangan — Pencegahan](../checklists/before-loss-prevention.md)
- [Daftar Periksa Penguatan Android](../checklists/android-hardening-checklist.md)
- [Daftar Periksa Penguatan iOS](../checklists/ios-hardening-checklist.md)

---

*Terakhir Diperbarui: 2026-06-01*
