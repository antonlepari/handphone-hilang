# Respons Perangkat Korporat

> Terakhir Diperbarui: 2026-06-01

## Ikhtisar

Kehilangan atau pencurian perangkat korporat (atau perangkat BYOD yang mengandung data kerja) memerlukan prosedur respons yang berbeda dari perangkat pribadi. Insiden ini dapat memicu kewajiban hukum, persyaratan notifikasi regulasi, dan investigasi forensik.

---

## Klasifikasi Perangkat

Tentukan jenis perangkat sebelum mengambil tindakan:

| Jenis | Deskripsi | Tindakan Utama |
|---|---|---|
| **Corporate-Owned** | Perangkat milik perusahaan, dikelola MDM | Ikuti kebijakan IR perusahaan; hapus via MDM |
| **BYOD dengan profil kerja** | Perangkat pribadi, ada profil kerja terdaftar | Hapus profil kerja saja via MDM jika memungkinkan |
| **BYOD tanpa MDM** | Perangkat pribadi, data kerja tanpa MDM | Lapor ke IT, ubah kredensial akses kerja |

---

## Prosedur Respons Segera (0–30 Menit)

### 1. Hubungi IT Security / Help Desk

**Segera hubungi** tim IT Security perusahaan — jangan tunda lebih dari 30 menit:

Informasi yang perlu disampaikan:
- Nama dan jabatan Anda
- Nomor aset perangkat (jika diketahui)
- IMEI / Nomor seri perangkat
- Waktu dan lokasi kejadian
- Data sensitif apa yang ada di perangkat
- Apakah perangkat terkunci saat hilang

### 2. Jangan Lakukan Remote Wipe Mandiri

> **⚠️ PERINGATAN:** Untuk perangkat korporat, **jangan** melakukan remote wipe tanpa otorisasi IT. Penghapusan data dapat:
> - Menghancurkan bukti forensik yang diperlukan untuk investigasi
> - Melanggar prosedur IR perusahaan
> - Menghambat klaim asuransi korporat

Tim IT akan memutuskan apakah wipe dilakukan melalui MDM, kapan waktunya, dan apakah forensik perlu dilakukan terlebih dahulu.

### 3. Cabut Akses Kerja

Koordinasikan dengan IT untuk mencabut akses:
- [ ] Email korporat (Exchange / Google Workspace)
- [ ] VPN korporat
- [ ] SSO / akun layanan internal
- [ ] Akses repositori kode (GitHub, GitLab, Bitbucket)
- [ ] Akun cloud korporat (AWS, GCP, Azure)
- [ ] Slack, Teams, dan alat kolaborasi
- [ ] Akses database atau server

---

## Eskalasi dan Pelaporan Internal

### Notifikasi yang Diperlukan

| Penerima | Waktu | Alasan |
|---|---|---|
| IT Security | 0–30 menit | Memulai respons teknis |
| Manajer langsung | 0–60 menit | Kesadaran manajemen |
| CISO / Kepala Keamanan | 1–4 jam | Jika data sensitif terlibat |
| Legal / Compliance | 4–24 jam | Jika kewajiban regulasi mungkin berlaku |
| HR | 24–48 jam | Dokumentasi kepegawaian |

### Kewajiban Notifikasi Regulasi

Evaluasi apakah insiden ini memerlukan notifikasi regulasi:

| Regulasi | Berlaku Jika | Tenggat Waktu |
|---|---|---|
| **UU PDP Indonesia (2022)** | Data pribadi warga Indonesia terpapar | 14 hari kalender sejak diketahui |
| **GDPR** | Data warga negara EU terpapar | 72 jam kepada otoritas pengawas |
| **PCI DSS** | Data kartu pembayaran mungkin terpapar | Segera; ikuti prosedur PCI IR |
| **HIPAA** | Data kesehatan pasien terpapar | 60 hari untuk entitas tercakup |
| **OJK** | Data nasabah lembaga keuangan terpapar | Ikuti POJK terkait pelaporan insiden |

---

## Penanganan Forensik

Jika perangkat korporat yang hilang mungkin menjadi subjek investigasi:

### Prinsip Chain of Custody

1. **Dokumentasikan semua tindakan** yang diambil setelah insiden diketahui
2. **Jangan ubah data** di akun yang terhubung perangkat tanpa dokumentasi
3. **Simpan semua log** akses dari periode sekitar waktu kejadian
4. **Arsipkan snapshot** log MDM, log akses VPN, dan aktivitas email

### Data yang Perlu Dipreservasi

- Log MDM sebelum dan sesudah insiden
- Log akses VPN (waktu koneksi, IP, data yang diakses)
- Log akses email — email yang dibuka, diunduh, atau diteruskan
- Log autentikasi SSO
- CCTV atau akses badge fisik di lokasi kejadian (jika relevan)

---

## Komunikasi Pasca-Insiden

### Notifikasi ke Karyawan/Tim

Jika ada risiko data karyawan lain terpapar, tim HR/Legal perlu menyiapkan komunikasi yang tepat.

### Notifikasi ke Pelanggan/Mitra

Jika data pelanggan atau mitra bisnis mungkin terpapar:
1. Konsultasikan dengan tim Legal
2. Siapkan pemberitahuan yang jelas dan faktual
3. Hindari spekulasi tentang data yang mungkin diakses
4. Sertakan langkah-langkah yang sudah diambil dan yang akan diambil

---

## Template Laporan Insiden Korporat

Lihat: [Template Laporan Insiden](../templates/incident-report-template.md)

---

## Dokumen Terkait

- [Respons Insiden — Ikhtisar](README.md)
- [Jam Pertama](first-hour.md)
- [Model Ancaman](../threat-models/threat-model-overview.md)
- [MDM & Enterprise](../hardening/mdm-enterprise.md)

---

*Terakhir Diperbarui: 2026-06-01 | Referensi: NIST SP 800-61r2, NIST SP 800-124r2*
