# Skenario Serangan

> Terakhir Diperbarui: 2026-06-01

---

## Skenario 1: Ponsel Tertinggal di Tempat Umum

**Deskripsi:** Perangkat tertinggal di kafe, transportasi umum, atau tempat umum lainnya dan ditemukan oleh orang yang tidak bertanggung jawab.

**Jalur Risiko:**
```
Perangkat tertinggal → Ditemukan orang lain → Mencoba akses → Data terpapar / dijual
```

**Risiko Utama:**
- Akses ke aplikasi yang masih terbuka jika layar tidak terkunci
- Pencurian perangkat keras untuk dijual kembali

**Deteksi:** Tidak ada sinyal aktif; lokasi terakhir terlihat di Find Hub/Find My

**Respons:**
1. Segera aktifkan Mode Hilang / Amankan Perangkat
2. Hubungi tempat kejadian (lost & found)
3. Pantau lokasi via Find Hub/Find My

**Mitigasi Pencegahan:**
- Batas waktu layar 30 detik
- PIN kuat
- Find My/Find Hub aktif

---

## Skenario 2: Copet (Perangkat Terkunci)

**Deskripsi:** Perangkat dicuri oleh copet saat terkunci, misalnya di keramaian atau transportasi umum.

**Jalur Serangan (MITRE ATT&CK):**
```
T1476 - Deliver Malicious App (fase sebelumnya, opsional)
→ Pencurian fisik
→ Upaya bypass PIN [T1411]
→ FRP bypass attempt
→ Penjualan perangkat
```

**Risiko Utama:**
- Brute force PIN jika 4 digit
- Upaya bypass FRP/Activation Lock
- Penjualan perangkat

**Deteksi:** Tidak ada aktivitas online dari perangkat; lokasi bergerak jauh

**Respons:**
1. Aktifkan Mode Hilang/Amankan Perangkat dalam 5 menit pertama
2. Laporkan ke polisi dan operator untuk pemblokiran IMEI
3. Pertimbangkan hapus jarak jauh jika tidak bisa dipulihkan

**Mitigasi Pencegahan:**
- PIN 6+ digit atau alfanumerik
- Hapus data setelah 10 upaya gagal
- FRP/Activation Lock aktif

---

## Skenario 3: Sambaran (Perangkat Tidak Terkunci / Sedang Digunakan)

**Deskripsi:** Perangkat dirampas saat sedang digunakan aktif — layar menyala, aplikasi terbuka.

**Jalur Serangan:**
```
Observasi target → Sambaran fisik → Akses langsung ke aplikasi terbuka [T1516]
→ Transfer dana perbankan → Ubah kata sandi email → Nonaktifkan Find My
```

**Risiko Utama:**
- Akses langsung ke semua aplikasi terbuka
- Transfer dana sebelum layar terkunci
- Pengambilalihan akun dalam hitungan menit

**Deteksi:**
- Kunci Deteksi Pencurian Android (AI) — otomatis kunci layar saat gerakan sambaran
- Notifikasi transaksi real-time dari bank

**Respons:**
1. Segera cabut sesi dari perangkat lain
2. Hubungi bank untuk memblokir kartu sementara
3. Ubah semua kata sandi segera

**Mitigasi Pencegahan:**
- Aktifkan Kunci Deteksi Pencurian (Android 10+)
- Batas waktu kunci layar pendek (15–30 detik)
- Notifikasi transaksi real-time aktif

---

## Skenario 4: Penyitaan di Perbatasan / Pemeriksaan

**Deskripsi:** Perangkat disita oleh otoritas (imigrasi, bea cukai, kepolisian) atau pihak tidak berwenang yang mengaku sebagai otoritas.

**Risiko Utama:**
- Ekstraksi data forensik tanpa izin
- Akses ke data korporat / komunikasi sensitif
- Instalasi spyware sebelum dikembalikan

**Deteksi:** Sulit dideteksi secara real-time

**Respons:**
1. Jangan berikan PIN atau kata sandi tanpa proses hukum yang jelas
2. Setelah perangkat dikembalikan: scan dengan MVT untuk deteksi spyware
3. Jika perangkat korporat: segera laporkan ke IT Security

**Mitigasi Pencegahan:**
- Aktifkan Mode Penguncian iOS (Lockdown Mode) sebelum perjalanan berisiko tinggi
- Gunakan perangkat sementara (burner device) untuk perjalanan ke negara berisiko tinggi
- Enkripsi penuh aktif
- Backup data sebelum perjalanan

---

## Skenario 5: Serangan SIM Swap

**Deskripsi:** Penyerang meyakinkan operator untuk memindahkan nomor telepon korban ke SIM mereka, mendapatkan akses ke semua 2FA berbasis SMS.

**Jalur Serangan:**
```
Kumpulkan data pribadi korban (OSINT/phishing) [T1593]
→ Hubungi operator dengan data palsu
→ Operator transfer nomor ke SIM penyerang
→ Penyerang menerima semua OTP SMS
→ Reset kata sandi akun → Pengambilalihan akun
```

**Teknik MITRE ATT&CK:** T1449 (Exploit SS7 to Redirect Phone Calls/SMS)

**Risiko Utama:**
- Bypass 2FA SMS untuk semua akun
- Pengambilalihan akun email, perbankan, kripto
- Tidak memerlukan pencurian perangkat fisik

**Deteksi:**
- SMS tiba-tiba berhenti (SIM tidak aktif)
- Notifikasi "No Service" pada perangkat
- Email notifikasi perubahan akun

**Respons:**
1. Segera hubungi operator untuk konfirmasi dan batalkan SIM swap
2. Periksa akun yang menggunakan 2FA SMS — ganti ke autentikator
3. Hubungi bank jika 2FA perbankan berbasis SMS

**Mitigasi Pencegahan:**
- Gunakan aplikasi autentikator TOTP, bukan SMS untuk 2FA
- Aktifkan PIN akun operator dan kunci port-out
- Gunakan eSIM (tidak bisa dicuri secara fisik)

---

## Skenario 6: Pencurian Kredensial dari Perangkat Tidak Terkunci

**Deskripsi:** Penyerang mendapat akses singkat ke perangkat yang tidak terkunci (misalnya ditinggal di meja, dipinjam) dan mengekstrak kredensial.

**Jalur Serangan:**
```
Akses fisik singkat ke perangkat tidak terkunci
→ Buka pengelola kata sandi / browser
→ Ekspor / foto kata sandi [T1414]
→ Akses akun dari perangkat lain
```

**Risiko Utama:**
- Pencurian kredensial tanpa jejak jelas
- Korban tidak sadar sampai akun disusupi

**Deteksi:**
- Login akun dari lokasi/perangkat tidak dikenal
- Email verifikasi login mencurigakan

**Respons:**
1. Jika dicurigai: ubah semua kata sandi segera
2. Aktifkan Pemeriksaan Identitas / Stolen Device Protection
3. Audit akses akun kritis

**Mitigasi Pencegahan:**
- Aktifkan Identity Check (Android 15+) — memblokir akses pengelola kata sandi tanpa biometrik
- Aktifkan Stolen Device Protection (iOS 17.3+)
- Jangan pernah tinggalkan perangkat tidak terkunci tanpa pengawasan

---

## Skenario 7: Kompromi Aplikasi Perbankan

**Deskripsi:** Setelah mendapat akses ke perangkat, penyerang menargetkan aplikasi perbankan mobile untuk melakukan transfer tidak sah.

**Jalur Serangan:**
```
Akses perangkat (terkunci/tidak terkunci)
→ Bypass kunci layar atau gunakan PIN yang diketahui
→ Buka aplikasi bank yang sudah login
→ Transfer dana ke rekening pencuci [T1516]
→ Cabut akses notifikasi untuk menyembunyikan aktivitas
```

**Teknik MITRE ATT&CK:** T1516 (Input Injection), T1429 (Capture Audio — untuk OTP verbal)

**Risiko Utama:**
- Kerugian finansial langsung
- Sulit dibatalkan jika sudah diproses

**Deteksi:**
- Notifikasi transaksi real-time (jika aktif)
- Peringatan dari bank

**Respons:**
1. **Segera** hubungi bank — minta pembekuan akun dan pembatalan transaksi
2. Ubah PIN dan kata sandi internet banking dari perangkat aman
3. Ajukan laporan ke bank dan OJK jika diperlukan

**Mitigasi Pencegahan:**
- Aktifkan notifikasi real-time untuk semua transaksi
- Pasang PIN tambahan di aplikasi banking (beda dari PIN perangkat)
- Batasi limit transfer harian

---

## Skenario 8: Pencurian Perangkat Korporat

**Deskripsi:** Perangkat korporat atau BYOD dengan data kerja dicuri, berpotensi memaparkan data bisnis sensitif.

**Jalur Serangan:**
```
Pencurian fisik / insider threat
→ Akses email korporat, dokumen, VPN credentials
→ Ekstraksi data pelanggan / IP perusahaan [T1533]
→ Penjualan ke kompetitor atau penggunaan untuk pemerasan
```

**Risiko Utama:**
- Pelanggaran data dan kewajiban regulasi
- Espionase industri
- Kerusakan reputasi

**Respons:**
1. Segera hubungi IT Security perusahaan
2. Cabut semua akses korporat via MDM
3. Dokumentasikan untuk investigasi forensik
4. Evaluasi kewajiban notifikasi regulasi (UU PDP, GDPR)

**Mitigasi Pencegahan:**
- MDM dengan kemampuan remote wipe
- Profil kerja terpisah (Android Enterprise / iOS MDM)
- Zero-trust akses — verifikasi perangkat sebelum akses sumber daya korporat

---

*Terakhir Diperbarui: 2026-06-01 | Referensi: MITRE ATT&CK Mobile — https://attack.mitre.org/matrices/mobile/*
