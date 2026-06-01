# Keamanan SIM

> Terakhir Diperbarui: 2026-06-01

## Ikhtisar

Kartu SIM adalah titik lemah kritis yang sering diabaikan. Melalui serangan SIM swap atau pencurian SIM fisik, penyerang dapat mengambil alih nomor telepon Anda — dan karenanya semua 2FA berbasis SMS.

---

## PIN SIM

PIN SIM mengunci kartu SIM itu sendiri. Jika diaktifkan:
- SIM memerlukan PIN saat dimasukkan ke perangkat baru
- SIM memerlukan PIN setelah restart perangkat
- Tanpa PIN, pencuri tidak bisa menggunakan SIM di ponsel lain

**Cara mengaktifkan PIN SIM:**

**Android:**
1. Pengaturan > Keamanan > Kunci kartu SIM
2. Aktifkan "Kunci kartu SIM"
3. Masukkan PIN SIM default (biasanya 1234 atau 0000 — **segera ganti**)
4. Ganti ke PIN 6–8 digit unik

**iOS:**
1. Pengaturan > Seluler > PIN SIM
2. Aktifkan PIN SIM
3. Masukkan PIN default operator
4. Ubah ke PIN baru yang kuat

> **⚠️ PERINGATAN:** Jika PIN SIM dimasukkan salah 3 kali berturut-turut, SIM akan terkunci (PUK lock). Simpan kode PUK dari operator Anda di tempat yang aman.

---

## Serangan SIM Swap

SIM swap adalah serangan di mana penyerang meyakinkan operator untuk memindahkan nomor Anda ke SIM mereka.

**Tanda-tanda SIM swap berhasil:**
- Sinyal tiba-tiba hilang / "No Service"
- Tidak bisa melakukan panggilan atau menerima SMS
- SMS dari bank atau layanan lain berhenti masuk
- Mendapat notifikasi "SIM berubah" dari aplikasi

**Mitigasi berlapis:**

| Lapisan | Tindakan | Efektivitas |
|---|---|---|
| PIN akun operator | Wajibkan PIN untuk perubahan SIM | Tinggi |
| Kunci port-out | Blokir transfer nomor ke operator lain | Tinggi |
| eSIM | Tidak bisa dipindah secara fisik | Sangat Tinggi |
| 2FA non-SMS | Tidak bergantung pada nomor telepon | Kritis |

---

## PIN Akun Operator Indonesia

Aktifkan perlindungan tambahan di akun operator Anda:

| Operator | Cara Aktifkan | Keterangan |
|---|---|---|
| **Telkomsel** | Hubungi 188 atau MyTelkomsel app | Minta "PIN Akun" untuk perubahan layanan |
| **Indosat** | Hubungi 185 atau MyIM3 | Aktifkan verifikasi tambahan |
| **XL** | Hubungi 817 atau myXL app | Minta proteksi akun |
| **Smartfren** | Hubungi 881 | Minta PIN akun |
| **Tri (3)** | Hubungi 132 | Aktifkan verifikasi identitas |

---

## eSIM — Keunggulan Keamanan

eSIM tertanam dalam perangkat keras dan tidak bisa dilepas secara fisik:

**Keunggulan keamanan:**
- Tidak bisa dicuri secara fisik bersama perangkat
- Transfer eSIM memerlukan autentikasi yang lebih ketat
- Mendukung beberapa profil operator

**Perangkat yang mendukung eSIM di Indonesia:**
- iPhone XS dan lebih baru
- Samsung Galaxy S20 dan lebih baru (beberapa model)
- Google Pixel 4 dan lebih baru

**Operator Indonesia yang mendukung eSIM:**
- Telkomsel, Indosat, XL Axiata, Smartfren (per 2025)

---

## Yang Harus Dilakukan Segera Setelah Kehilangan Perangkat

1. Hubungi operator dan minta **suspend SIM segera**
2. Minta **pemblokiran IMEI** (agar tidak bisa digunakan dengan SIM lain)
3. Jika ada 2FA SMS di akun penting — beralih ke aplikasi autentikator segera
4. Ke gerai operator dengan KTP untuk aktivasi SIM pengganti dengan nomor yang sama

---

## Dokumen Terkait

- [Sebelum Kehilangan — Pencegahan](../checklists/before-loss-prevention.md)
- [30 Menit Pertama](../incident-response/first-30-minutes.md)
- [Skenario Serangan — SIM Swap](../threat-models/attack-scenarios.md)

---

*Terakhir Diperbarui: 2026-06-01 | Referensi: https://www.cisa.gov/sites/default/files/publications/CISA_MS-ISAC_Ransomware%20Guide_S508C.pdf*
