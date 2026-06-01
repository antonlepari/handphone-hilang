# Perlindungan Reset Pabrik (FRP) — Android

> Terakhir Diperbarui: 2026-06-01

## Ikhtisar

**Perlindungan Reset Pabrik (Factory Reset Protection / FRP)** adalah fitur keamanan Android yang diperkenalkan pada Android 5.1 (Lollipop) yang mencegah perangkat yang telah direset pabrik diatur ulang tanpa kredensial Akun Google pemilik aslinya. Fitur ini dirancang khusus untuk mencegah pencurian perangkat dengan membuat ponsel yang dicuri tidak dapat digunakan kecuali pencuri dapat mengautentikasi dengan Akun Google asli.

*Referensi: https://support.google.com/android/answer/6088432*

---

## Cara Kerja FRP

### Mekanisme Perlindungan

FRP mengikat perangkat ke Akun Google yang aktif di dalamnya. Ketika reset pabrik dilakukan melalui **metode tidak sah** — seperti:

- Mode pemulihan (kombinasi tombol Volume + Daya)
- Perintah ADB
- Perintah Fastboot
- Kombinasi tombol perangkat keras

...perangkat akan memerlukan alamat email dan kata sandi Akun Google asli selama wizard penyiapan sebelum dapat digunakan.

### Reset Normal vs. Reset Tidak Sah

```
RESET YANG DISAHKAN (melalui menu Pengaturan):
  Pengaturan > Manajemen Umum > Reset > Reset Data Pabrik
  → Pengguna terautentikasi (masuk) saat memulai
  → Akun Google dihapus dengan benar selama reset
  → FRP TIDAK aktif
  → Perangkat dapat diatur dengan akun apa pun setelah reset

RESET TIDAK SAH (melalui mode pemulihan atau perangkat keras):
  → Perangkat direset tanpa sesi terautentikasi
  → Informasi Akun Google disimpan di partisi yang dilindungi
  → FRP AKTIF pada penyiapan berikutnya
  → Perangkat memerlukan kredensial Akun Google asli
```

### Implementasi Teknis

FRP menyimpan informasi Akun Google di partisi yang dilindungi yang bertahan dari reset pabrik yang dimulai melalui metode tidak sah. Partisi ini hanya dibersihkan ketika pengguna melakukan reset pabrik melalui menu Pengaturan yang terautentikasi (yang terlebih dahulu menghapus Akun Google terkait).

---

## Mengapa FRP Penting

Tanpa FRP:
1. Pencuri mencuri perangkat
2. Melakukan reset pabrik menggunakan tombol perangkat keras
3. Mengatur perangkat dengan akun mereka sendiri
4. Menjual atau menggunakan perangkat

Dengan FRP:
1. Pencuri mencuri perangkat
2. Mencoba reset pabrik menggunakan tombol perangkat keras
3. Perangkat mencapai layar verifikasi Akun Google
4. Pencuri tidak dapat melanjutkan tanpa kredensial asli
5. Perangkat tetap terkunci, secara signifikan mengurangi nilai jual kembali dan insentif pencurian

> **ℹ️ CATATAN:** FRP adalah salah satu fitur anti-pencurian paling efektif di Android. Ini secara langsung mengurangi insentif ekonomi pencurian perangkat dengan membuat perangkat yang dicuri sulit dijual kembali atau digunakan ulang.

---

## Konfigurasi

### Memverifikasi FRP Aktif

FRP **otomatis aktif** ketika:
- Akun Google masuk ke perangkat
- Versi Android adalah 5.1 atau lebih tinggi

Tidak diperlukan konfigurasi manual. Untuk memverifikasi:

1. Buka **Pengaturan > Akun > Google**
2. Jika Akun Google terdaftar, FRP aktif untuk akun tersebut

### Mengonfigurasi FRP Sebelum Menjual atau Memberikan Perangkat

> **⚠️ PERINGATAN:** Jika Anda melakukan reset pabrik melalui mode pemulihan tanpa terlebih dahulu menghapus Akun Google, FRP akan mengunci perangkat untuk pemilik baru. Selalu reset melalui menu Pengaturan.

**Proses yang benar sebelum mentransfer perangkat:**
1. Buka **Pengaturan > Akun > Google**
2. Ketuk Akun Google Anda
3. Ketuk **Hapus akun**
4. Kemudian lakukan reset pabrik melalui **Pengaturan > Manajemen Umum > Reset > Reset Data Pabrik**

Atau cukup:
1. Buka **Pengaturan > Manajemen Umum > Reset > Reset Data Pabrik**
2. Ini secara otomatis menangani penghapusan akun dalam sesi yang terautentikasi

---

## FRP yang Ditingkatkan: Aturan 72 Jam

Beberapa produsen Android (termasuk Samsung) menerapkan aturan FRP yang ditingkatkan: jika Akun Google ditambahkan ke perangkat dalam **72 jam terakhir** sebelum reset pabrik dimulai, perangkat dapat menerapkan pembatasan kunci tambahan. Ini mencegah pencuri:
1. Mencuri perangkat
2. Dengan cepat menambahkan Akun Google baru
3. Segera melakukan reset pabrik untuk "menghapus" FRP

---

## FRP Enterprise (eFRP)

Untuk penerapan enterprise, **Perlindungan Reset Pabrik Enterprise (eFRP)** memperluas FRP standar dengan kontrol organisasi:

- Administrator IT dapat menentukan **Akun Google mana** (atau tidak ada akun) yang dapat mengaktifkan ulang perangkat setelah reset
- Dalam lingkungan yang dikelola sepenuhnya (MDM), reset yang dilakukan melalui Pengaturan tetap dapat dilindungi
- Berguna untuk perangkat milik perusahaan untuk mencegah penggunaan ulang yang tidak sah setelah karyawan keluar

*Referensi: https://support.google.com/work/android/answer/7596562*

---

## Upaya Bypass FRP (Perspektif Penyerang)

Memahami upaya bypass membantu mengonfigurasi pertahanan:

### Metode Bypass Umum

| Metode | Deskripsi | Efektivitas |
|---|---|---|
| Social Engineering Google | Meyakinkan dukungan Google untuk menghapus FRP | Sangat Rendah — Google memerlukan verifikasi identitas |
| Flashing Firmware | Mem-flash firmware tidak ditandatangani untuk menghapus partisi FRP | Bervariasi per perangkat; sebagian besar perangkat saat ini memiliki Verified Boot |
| Alat Bypass ADB | Alat pihak ketiga yang mengklaim bypass FRP | Sering berupa malware; efektivitas aktual bervariasi dan berkurang dengan pembaruan |
| Alat Layanan Perangkat Keras | Alat komersial yang digunakan oleh toko reparasi | Efektivitas terbatas pada versi Android saat ini |

> **⚠️ PERINGATAN:** Sebagian besar "alat bypass FRP" yang ditemukan online adalah malware, adware, atau penipuan yang menargetkan pemilik perangkat yang terkunci sendiri. Jangan gunakan mereka.

### Ketahanan FRP pada Perangkat Modern

Perangkat dengan **Verified Boot** (Android 8+) dan **Google Titan M** (Pixel 3+) atau elemen aman yang setara membuat FRP jauh lebih tahan terhadap bypass:

- Elemen aman menyimpan informasi FRP di perangkat keras yang tahan gangguan
- Verified Boot mencegah firmware tidak ditandatangani berjalan yang dapat menghapus partisi FRP
- Upaya bypass yang gagal berulang kali dapat memicu kunci perangkat permanen

---

## FRP dan Samsung Knox

Perangkat Samsung Galaxy yang menjalankan **Samsung Knox** menerapkan FRP melalui sistem dua lapis:

1. **FRP Android Standar** — seperti yang dijelaskan di atas
2. **Kunci Reaktivasi Samsung** — lapisan tambahan yang terikat dengan Akun Samsung (terpisah dari Akun Google)

Untuk melindungi perangkat Samsung sepenuhnya:
- Aktifkan FRP melalui Akun Google (otomatis)
- Aktifkan Kunci Reaktivasi Samsung melalui **Pengaturan > Biometrik dan keamanan > Find My Mobile > Kunci reaktivasi**

*Referensi: https://www.samsungknox.com/en/blog/what-is-factory-reset-protection*

---

## Apa yang TIDAK Dilindungi FRP

FRP dirancang untuk mencegah **penggunaan ulang yang tidak sah** pada perangkat, bukan melindungi data. Pahami batasan ini:

| Ancaman | Perlindungan FRP? | Mitigasi Tambahan yang Dibutuhkan |
|---|---|---|
| Ekstraksi data sebelum reset | Tidak | Gunakan enkripsi perangkat kuat + PIN |
| Pelepasan dan penggunaan SIM | Tidak | Aktifkan PIN SIM |
| Membaca data kartu SD | Tidak | Enkripsi kartu SD; hindari menyimpan data sensitif di sana |
| Akses fisik ke perangkat yang terbuka | Tidak | PIN kuat, batas waktu layar, Pemeriksaan Identitas |
| Akses data cloud melalui kredensial yang dicuri | Tidak | 2FA pada Akun Google |

---

## Daftar Periksa: Praktik Terbaik FRP

- [ ] Akun Google masuk di perangkat (FRP otomatis aktif)
- [ ] Akun Google memiliki kata sandi kuat dan 2FA diaktifkan
- [ ] Jika menjual/memberikan perangkat: reset pabrik melalui menu Pengaturan, bukan mode pemulihan
- [ ] Untuk Samsung: aktifkan Kunci Reaktivasi Samsung sebagai lapisan tambahan
- [ ] Untuk enterprise: konfigurasikan kebijakan eFRP melalui MDM

---

## Dokumen Terkait

- [Keamanan Akun Google](google-account-security.md)
- [Panduan Penguatan Android](../hardening/android-hardening.md)
- [MDM Enterprise](../hardening/mdm-enterprise.md)

---

*Terakhir Diperbarui: 2026-06-01 | Sumber: https://support.google.com/android | https://www.samsungknox.com*
