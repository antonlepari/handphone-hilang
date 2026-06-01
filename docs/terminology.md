# Terminologi

> Terakhir Diperbarui: 2026-06-01

Glosarium ini mendefinisikan istilah-istilah kunci yang digunakan di seluruh Panduan Respons Kehilangan & Pencurian Perangkat Mobile. Istilah dicantumkan secara alfabetis.

---

## A

**Activation Lock (Kunci Aktivasi)**
Fitur keamanan Apple yang mengikat iPhone, iPad, atau Apple Watch ke Apple ID terkaitnya. Bahkan setelah reset pabrik, perangkat memerlukan kredensial Apple ID asli untuk diaktifkan kembali. Otomatis diaktifkan ketika Find My dihidupkan.
*Lihat: [Kunci Aktivasi](../ios/activation-lock.md)*

**ADB (Android Debug Bridge)**
Alat baris perintah yang memungkinkan komunikasi dengan perangkat Android. Digunakan dalam pengembangan dan forensik. Jika USB debugging diaktifkan pada perangkat yang dicuri, ADB dapat digunakan untuk mengekstrak data.
*Referensi: https://developer.android.com/tools/adb*

**Aplikasi Autentikator**
Aplikasi perangkat lunak yang menghasilkan kata sandi satu kali berbasis waktu (TOTP) untuk autentikasi dua faktor. Contoh: Google Authenticator, Microsoft Authenticator, Authy. Lebih aman dari 2FA berbasis SMS untuk pemulihan akun.

---

## B

**Autentikasi Biometrik**
Autentikasi menggunakan karakteristik fisik — sidik jari (Touch ID), geometri wajah (Face ID), atau pemindaian iris. Digunakan pada perangkat Android dan iOS untuk buka kunci perangkat dan otorisasi tindakan sensitif.

**BYOD (Bring Your Own Device)**
Kebijakan yang memungkinkan karyawan menggunakan smartphone pribadi mereka untuk keperluan kerja. Menciptakan tantangan keamanan seputar pemisahan data, otoritas penghapusan jarak jauh, dan pendaftaran MDM.

---

## C

**PIN Akun Operator**
PIN unik yang ditetapkan dengan operator seluler untuk mencegah perubahan akun yang tidak sah, penggantian SIM, atau port-out nomor. Berbeda dari PIN perangkat. Juga disebut "kode sandi akun."

**COPE (Corporate Owned, Personally Enabled)**
Model kepemilikan perangkat di mana organisasi memiliki perangkat tetapi mengizinkan penggunaan pribadi. Organisasi mempertahankan kontrol MDM penuh, termasuk penghapusan jarak jauh.

**CYOD (Choose Your Own Device)**
Model di mana karyawan memilih dari daftar perangkat yang telah disetujui yang dibeli oleh organisasi.

---

## D

**Data Saat Diam (Data at Rest)**
Data yang tersimpan di penyimpanan internal perangkat atau kartu SD. Perangkat Android modern (Android 10+) dan iOS (iOS 8+) mengenkripsi data saat diam secara default menggunakan AES-256 atau setara.

**Data Saat Transit (Data in Transit)**
Data yang dikirim melalui jaringan (Wi-Fi, seluler, Bluetooth). Harus dilindungi menggunakan TLS/HTTPS.

---

## E

**eSIM (Embedded SIM)**
Kartu SIM yang tertanam ke dalam perangkat keras dan tidak dapat dilepas secara fisik. Memberikan perlindungan yang ditingkatkan terhadap serangan berbasis pencurian SIM. Mendukung beberapa profil operator.

**Enkripsi**
Proses mengkodekan data sehingga hanya dapat dibaca dengan kunci dekripsi yang benar. Android dan iOS mengenkripsi penyimpanan perangkat secara default ketika kode sandi diatur.

---

## F

**Factory Reset Protection / FRP (Perlindungan Reset Pabrik)**
Fitur keamanan Android (Android 5.1+) yang memerlukan kredensial akun Google asli setelah reset pabrik yang dilakukan melalui mode pemulihan atau tombol perangkat keras. Mencegah pencuri menghapus dan menggunakan kembali perangkat.
*Lihat: [Perlindungan Reset Pabrik](../android/factory-reset-protection.md)*

**Find Hub**
Platform pelacakan perangkat Google, sebelumnya disebut "Find My Device." Diganti namanya pada Mei 2025. Menggunakan jaringan kerumunan dari lebih dari satu miliar perangkat Android untuk menemukan ponsel, tablet, earbud, dan tag yang hilang melalui Bluetooth bahkan saat offline.
*Lihat: [Find Hub](../android/find-my-device.md)*

**Find My**
Platform pelacakan perangkat dan item Apple untuk iPhone, iPad, Mac, Apple Watch, dan AirTag. Menggunakan sinyal Bluetooth berbasis kerumunan yang dienkripsi end-to-end untuk menemukan perangkat secara offline.
*Lihat: [Find My](../ios/find-my.md)*

**Ekstraksi Forensik**
Proses mengekstrak bukti digital dari perangkat menggunakan alat khusus. Relevan dalam konteks investigasi kriminal dan respons insiden.

---

## G

**Akun Google**
Mekanisme identitas dan autentikasi utama untuk perangkat Android. Mengontrol akses ke Gmail, Google Drive, Play Store, Find Hub, dan cadangan perangkat.

---

## I

**Pemeriksaan Identitas (Identity Check)**
Fitur keamanan Android yang diperkenalkan pada Januari 2025 (Android 15+, Pixel dan Samsung Galaxy). Memerlukan autentikasi biometrik (sidik jari atau wajah) — tanpa fallback kode sandi — untuk mengakses pengaturan sensitif ketika perangkat jauh dari lokasi tepercaya.
*Lihat: [Pemeriksaan Identitas](../android/identity-check.md)*

**IMEI (International Mobile Equipment Identity)**
Nomor 15 digit unik yang ditetapkan untuk setiap perangkat mobile. Digunakan untuk mengidentifikasi perangkat tertentu di jaringan seluler. Operator dapat memblokir perangkat yang dicuri menggunakan IMEI-nya. Temukan ini di Pengaturan > Tentang Ponsel, atau dengan menekan `*#06#`.

**IMSI (International Mobile Subscriber Identity)**
Pengenal unik yang tersimpan di kartu SIM yang mengidentifikasi pelanggan di jaringan seluler. Berbeda dari IMEI.

**Respons Insiden (Incident Response / IR)**
Metodologi terstruktur untuk mengelola dampak dari pelanggaran atau kompromi keamanan. Dalam konteks kehilangan perangkat, IR mencakup penahanan, pemberantasan, pemulihan, dan pelajaran yang dipetik.

**IOC (Indicator of Compromise)**
Artefak forensik — hash file, alamat IP, domain, pola perilaku — yang menunjukkan sistem telah disusupi. Digunakan oleh alat seperti MVT untuk mendeteksi spyware.

---

## K

**Kunci Pemulihan (Recovery Key)**
Kunci 28 karakter yang dibuat saat mengaktifkan Perlindungan Data Lanjutan atau autentikasi dua faktor untuk Apple ID. Digunakan untuk mendapatkan kembali akses akun jika terkunci. Harus disimpan secara aman secara offline.

**Kontak Pemulihan (Recovery Contact)**
Orang tepercaya yang dapat memberikan kode pemulihan untuk membantu mendapatkan kembali akses ke Apple ID. Kontak tidak mendapatkan akses ke data akun.

---

## L

**Lost Mode (Mode Hilang)**
Fitur iOS yang mengunci perangkat dan menampilkan pesan kustom (termasuk informasi kontak) di layar kunci. Mengaktifkan pelacakan lokasi untuk perangkat. Mencegah penggunaan Apple Pay. Tidak menghapus data.
*Lihat: [Mode Hilang](../ios/lost-mode.md)*

---

## M

**MDM (Mobile Device Management)**
Perangkat lunak yang digunakan oleh organisasi untuk mengelola, mengonfigurasi, memantau, dan mengendalikan perangkat mobile dari jarak jauh. Contoh: Microsoft Intune, Jamf, VMware Workspace ONE.
*Lihat: [MDM Enterprise](../hardening/mdm-enterprise.md)*

**MITRE ATT&CK Mobile Matrix**
Basis pengetahuan tentang taktik, teknik, dan prosedur (TTP) musuh khusus untuk platform mobile (Android dan iOS). Digunakan untuk memetakan skenario ancaman ke pola serangan yang diketahui.
*Referensi: https://attack.mitre.org/matrices/mobile/*

**MVT (Mobile Verification Toolkit)**
Alat forensik open-source yang dikembangkan oleh Amnesty International Security Lab untuk mendeteksi tanda-tanda kompromi perangkat, termasuk spyware seperti Pegasus.
*Lihat: [Alat yang Direkomendasikan](../tools/recommended-tools.md)*

---

## O

**OTP (One-Time Password)**
Kata sandi sementara dan sekali pakai yang digunakan untuk autentikasi. Dapat dikirim melalui SMS, email, atau dibuat oleh aplikasi autentikator. OTP berbasis SMS rentan terhadap serangan SIM swap.

---

## P

**Passkey**
Kredensial autentikasi yang sesuai dengan FIDO2 yang tersimpan di perangkat. Menggantikan kata sandi dengan pasangan kunci kriptografi. Tidak dapat di-phishing, digunakan ulang, atau dicuri melalui pelanggaran data. Didukung pada Android dan iOS.

**PIN (Personal Identification Number)**
Kode numerik yang digunakan untuk membuka kunci perangkat. Minimum 4 digit (tidak direkomendasikan), idealnya 6 digit atau lebih, atau diganti dengan frasa sandi alfanumerik.

**Play Protect**
Layanan pemindaian malware bawaan Google untuk Android. Memindai aplikasi saat instalasi dan terus-menerus setelah instalasi. Menganalisis lebih dari 200 miliar aplikasi setiap hari di seluruh Play Store dan aplikasi sideload.
*Lihat: [Play Protect](../android/play-protect.md)*

**Port Freeze / Port-Out Lock (Kunci Port)**
Fitur keamanan operator yang mencegah nomor telepon ditransfer (port) ke operator lain tanpa persetujuan eksplisit pemilik akun. Pertahanan kunci terhadap serangan SIM swap.

---

## R

**Remote Wipe (Penghapusan Jarak Jauh)**
Kemampuan untuk menghapus semua data di perangkat dari jarak jauh, biasanya melalui layanan cloud (Find Hub atau Find My) atau platform MDM. Digunakan sebagai upaya terakhir ketika pemulihan perangkat tidak mungkin dan perlindungan data menjadi prioritas.

---

## S

**Kartu SIM (Subscriber Identity Module)**
Kartu kecil yang menyimpan informasi identitas pelanggan dan menyediakan konektivitas seluler. SIM fisik dapat dilepas dari perangkat yang dicuri; eSIM tidak bisa.

**PIN SIM**
PIN terpisah yang digunakan untuk mengunci kartu SIM itu sendiri. Jika diaktifkan, PIN SIM diperlukan ketika SIM dimasukkan ke perangkat baru atau setelah restart perangkat. Berbeda dari PIN kunci perangkat.

**Serangan SIM Swap**
Serangan rekayasa sosial di mana penjahat meyakinkan operator untuk mentransfer nomor telepon korban ke kartu SIM yang dikendalikan oleh penyerang. Memungkinkan bypass 2FA berbasis SMS.
*Lihat: [Keamanan SIM](../hardening/sim-security.md)*

**Spyware**
Malware yang dirancang untuk memantau dan mengekstrak data dari perangkat tanpa sepengetahuan pemilik. Contoh lanjutan termasuk Pegasus (NSO Group), yang dirancang untuk menargetkan jurnalis dan aktivis.

**Stolen Device Protection (Perlindungan Perangkat Dicuri)**
Fitur keamanan iOS 17.3+ yang menambahkan persyaratan autentikasi biometrik (tanpa fallback kode sandi) untuk tindakan sensitif ketika iPhone berada di lokasi yang tidak familiar. Juga memberlakukan periode tunggu satu jam sebelum perubahan keamanan kritis tertentu.
*Lihat: [Perlindungan Perangkat Dicuri](../ios/stolen-device-protection.md)*

---

## T

**Theft Detection Lock (Kunci Deteksi Pencurian)**
Fitur keamanan Android 10+ yang menggunakan AI di perangkat (akselerometer, giroskop, Wi-Fi, Bluetooth) untuk mendeteksi pola gerakan yang konsisten dengan pencurian sambaran dan secara otomatis mengunci layar perangkat.

**TOTP (Time-Based One-Time Password)**
Mekanisme 2FA yang menghasilkan kode 6-8 digit baru setiap 30 detik menggunakan rahasia bersama dan waktu saat ini. Digunakan oleh aplikasi autentikator. Lebih aman dari OTP SMS.

**Lokasi Tepercaya (Trusted Location)**
Lokasi (rumah, kantor) yang terdaftar dalam Pemeriksaan Identitas Android atau Perlindungan Perangkat Dicuri iOS di mana persyaratan keamanan yang dilonggarkan berlaku. Di luar lokasi tepercaya, autentikasi yang lebih kuat diberlakukan.

---

## U

**USB Debugging (Penelusuran USB)**
Fitur pengembang Android yang memungkinkan komputer mengirim perintah ke perangkat Android melalui USB menggunakan ADB. Harus dinonaktifkan di perangkat non-pengembangan, karena memungkinkan ekstraksi data jika dibiarkan aktif.

**UWB (Ultra-Wideband)**
Teknologi nirkabel jarak pendek yang memberikan presisi lokasi tingkat sentimeter. Digunakan di Apple's Find My dengan AirTag dan di Android's Find Hub untuk lokasi item yang tepat. Tersedia di perangkat Pixel dan Samsung yang lebih baru.

---

## V

**VPN (Virtual Private Network)**
Terowongan terenkripsi antara perangkat dan server yang melindungi lalu lintas internet dari penyadapan. Direkomendasikan untuk digunakan di jaringan Wi-Fi publik.

---

*Terakhir Diperbarui: 2026-06-01*
