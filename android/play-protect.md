# Google Play Protect

> Terakhir Diperbarui: 2026-06-01

## Ikhtisar

**Google Play Protect** adalah layanan perlindungan malware bawaan Android. Ini disertakan dengan Google Play Services dan beroperasi secara terus-menerus di setiap perangkat Android yang memiliki Google Play Store terinstal. Play Protect memindai aplikasi yang diinstal dari Play Store dan dari sumber pihak ketiga (aplikasi sideload), memantau perilaku perangkat untuk aktivitas berbahaya, dan menyediakan perlindungan Penjelajahan Aman di Chrome dan aplikasi lainnya.

*Referensi: https://support.google.com/googleplay/answer/2812853*

---

## Apa yang Dilakukan Play Protect

### Pemindaian Aplikasi

Play Protect menganalisis aplikasi sebelum dan setelah instalasi:

- **Pemindaian pra-instalasi**: Aplikasi yang dikirimkan ke Google Play Store dipindai oleh sistem otomatis dan peninjau manusia sebelum tersedia untuk diunduh
- **Pemindaian di perangkat**: Aplikasi dipindai saat diinstal dari sumber mana pun (Play Store, sideload APK, toko pihak ketiga)
- **Pemindaian latar belakang berkelanjutan**: Aplikasi yang sudah terinstal dipindai ulang secara berkala untuk mendeteksi ancaman yang baru diidentifikasi

Play Protect menganalisis lebih dari **200 miliar aplikasi** setiap hari di seluruh ekosistem Android.

### Kategori Deteksi Aplikasi Berbahaya

Play Protect mendeteksi dan bertindak pada aplikasi dalam kategori ancaman berikut:

| Kategori | Deskripsi |
|---|---|
| **Stalkerware** | Aplikasi yang secara diam-diam melacak lokasi, panggilan, pesan tanpa persetujuan |
| **Trojan Perbankan** | Aplikasi yang melapisi layar aplikasi perbankan untuk mencuri kredensial |
| **Spyware** | Aplikasi yang mengekstrak data pribadi, kontak, pesan |
| **Ransomware** | Aplikasi yang mengunci perangkat atau mengenkripsi file dan meminta pembayaran |
| **Aplikasi Berpotensi Berbahaya (PHA)** | Aplikasi dengan izin atau perilaku mencurigakan |
| **Perangkat Lunak Tidak Diinginkan** | Adware, aplikasi yang mengumpulkan data berlebihan |

### Pemantauan Perilaku Perangkat

Play Protect memantau perilaku tingkat perangkat di luar aplikasi individual:
- Aktivitas jaringan yang tidak biasa
- Pengeringan baterai yang tidak normal dari proses yang tidak dikenal
- Pola penggunaan izin yang mencurigakan

### Penjelajahan Aman

Play Protect terintegrasi dengan Google Safe Browsing untuk memperingatkan pengguna saat mereka mencoba mengunjungi situs web berbahaya yang dikenal di Chrome dan aplikasi lain yang menggunakan Safe Browsing API.

---

## Cara Memeriksa Status Play Protect

### Di Android (Versi Apa Pun)

1. Buka aplikasi **Play Store**
2. Ketuk **ikon profil** (kanan atas)
3. Ketuk **Play Protect**
4. Tinjau status:
   - "Tidak ada aplikasi berbahaya yang ditemukan" — perangkat bersih (pemindaian terakhir)
   - Waktu dan tanggal pemindaian terakhir
   - Opsi untuk menjalankan pemindaian manual

### Melalui Pengaturan

Beberapa versi Android: **Pengaturan > Keamanan > Google Play Protect**

---

## Menjalankan Pemindaian Manual

1. Buka **Play Store** > Profil > **Play Protect**
2. Ketuk **Pindai**
3. Tunggu pemindaian selesai
4. Tinjau item yang ditandai

> **💡 TIPS:** Jalankan pemindaian Play Protect manual segera setelah menginstal aplikasi apa pun dari luar Google Play Store.

---

## Play Protect dan Perangkat Hilang/Dicuri

### Relevansi dengan Skenario Pencurian

Play Protect paling relevan untuk kehilangan/pencurian perangkat dalam skenario berikut:

**Skenario 1: Perangkat Dipulihkan Setelah Ditinggalkan Tanpa Pengawasan**
Jika perangkat dapat diakses oleh penyerang yang menginstal malware atau spyware, pemindaian Play Protect harus segera dijalankan saat pemulihan untuk mendeteksi ancaman yang terinstal.

**Skenario 2: Malware yang Ada Sebelum Pencurian**
Jika spyware diinstal sebelum pencurian (mis., stalkerware yang diinstal oleh seseorang dengan akses fisik sebelumnya), mungkin telah menyampaikan lokasi atau data komunikasi ke penyerang. Play Protect akan mendeteksi tanda tangan stalkerware yang dikenal.

**Skenario 3: Verifikasi Pasca-Pemulihan**
Setelah memulihkan perangkat yang hilang/dicuri atau menyiapkan perangkat baru, menjalankan Play Protect memastikan tidak ada aplikasi berbahaya yang ada.

### Yang Harus Diperiksa Setelah Pemulihan

```
Setelah memulihkan perangkat yang hilang/dicuri:

1. Play Store > Profil > Play Protect > Pindai
2. Tinjau aplikasi yang ditandai
3. Jika stalkerware atau spyware terdeteksi:
   - JANGAN langsung uninstal — penyerang mungkin mendapat peringatan
   - Lakukan reset pabrik penuh sebagai gantinya
   - Ubah semua kata sandi dari perangkat yang bersih
4. Periksa aplikasi yang terinstal: Pengaturan > Aplikasi > Lihat semua aplikasi
   - Cari aplikasi yang tidak Anda instal
   - Cari aplikasi dengan pemberian izin tidak biasa (lokasi, mikrofon, kontak)
```

---

## Mengaktifkan Pemindaian yang Ditingkatkan

### Untuk Aplikasi Sideload (APK)

Secara default, Play Protect mungkin tidak memindai sepenuhnya aplikasi yang diinstal dari luar Play Store. Aktifkan pemindaian yang ditingkatkan:

1. Buka **Pengaturan > Keamanan** (atau **Keamanan & Privasi**)
2. Ketuk **Pengaturan keamanan lainnya** (atau serupa, bervariasi per produsen)
3. Aktifkan **Pindai aplikasi dengan Play Protect**
4. Aktifkan **Tingkatkan deteksi aplikasi berbahaya** untuk mengizinkan aplikasi yang tidak dikenal dikirim ke Google untuk ditinjau

> **⚠️ PERINGATAN:** Menginstal APK dari sumber tidak resmi (bukan Google Play Store) secara dramatis meningkatkan risiko. Hanya instal aplikasi dari Play Store atau dari sumber yang Anda percayai secara eksplisit (mis., F-Droid untuk aplikasi open-source). Jika Anda harus menginstal APK, verifikasi hash SHA256 terhadap situs web resmi penerbit.

---

## Keterbatasan Play Protect

Play Protect adalah landasan yang kuat tetapi tidak sempurna:

| Keterbatasan | Detail |
|---|---|
| **Ancaman zero-day** | Malware baru yang tidak dikenal oleh basis data Google mungkin tidak langsung terdeteksi |
| **Spyware tingkat lanjut** | Spyware negara-bangsa (mis., Pegasus) mungkin lolos dari deteksi Play Protect; gunakan MVT untuk analisis forensik |
| **Aplikasi sistem** | Bloatware yang sudah terinstal atau aplikasi produsen tidak dipindai dengan cara yang sama seperti aplikasi yang diunduh |
| **Operasi offline** | Akurasi pemindaian berkurang tanpa konektivitas internet untuk pembaruan tanda tangan |

Untuk analisis forensik lanjutan dari potensi spyware, lihat [Mobile Verification Toolkit (MVT)](../tools/recommended-tools.md).

---

## Play Protect dan Profil Kerja

Di perangkat dengan **profil kerja** yang dikelola oleh MDM (mis., Android Enterprise), Play Protect beroperasi di dalam kontainer profil pribadi dan kerja. Administrator MDM mungkin memiliki kebijakan pemindaian malware terpisah yang dikonfigurasi.

---

## Dokumen Terkait

- [Panduan Penguatan Android](../hardening/android-hardening.md)
- [Pemeriksaan Identitas](identity-check.md)
- [Alat yang Direkomendasikan — MVT](../tools/recommended-tools.md)

---

*Terakhir Diperbarui: 2026-06-01 | Sumber: https://support.google.com/googleplay/answer/2812853*
