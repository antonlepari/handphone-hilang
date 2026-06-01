# Model Ancaman

> Terakhir Diperbarui: 2026-06-01

## Ikhtisar

Bagian ini menyediakan analisis ancaman terstruktur untuk skenario kehilangan dan pencurian perangkat mobile. Model ancaman membantu profesional keamanan, analis SOC, dan tim korporat memahami risiko secara sistematis dan memprioritaskan mitigasi.

---

## Dokumen dalam Bagian Ini

| Dokumen | Deskripsi |
|---|---|
| [Ikhtisar Model Ancaman](threat-model-overview.md) | Aset, pelaku ancaman, permukaan serangan, pemetaan mitigasi |
| [Skenario Serangan](attack-scenarios.md) | 8 skenario realistis dengan jalur serangan dan respons |
| [Matriks Risiko](risk-matrix.md) | Matriks 5x5 kemungkinan vs. dampak dengan mitigasi |

---

## Pendekatan Pemodelan Ancaman

Repositori ini menggunakan kerangka kerja **STRIDE** yang diadaptasi untuk konteks kehilangan perangkat mobile:

| Kategori STRIDE | Relevansi Kehilangan Perangkat |
|---|---|
| **Spoofing** | Pencuri berpura-pura sebagai pemilik ke operator/Apple Support |
| **Tampering** | Modifikasi data atau pengaturan perangkat |
| **Repudiation** | Transaksi yang dilakukan pencuri, korban tidak bisa buktikan |
| **Information Disclosure** | Akses data pribadi, kredensial, foto |
| **Denial of Service** | Pemblokiran akun, perubahan kata sandi mengunci korban |
| **Elevation of Privilege** | Pencuri mendapat akses admin melalui PIN yang diamati |

---

## Referensi

- [MITRE ATT&CK Mobile Matrix](https://attack.mitre.org/matrices/mobile/)
- [OWASP Mobile Security Testing Guide](https://owasp.org/www-project-mobile-app-security/)
- [Lanskap Ancaman](../docs/threat-landscape.md)

---

*Terakhir Diperbarui: 2026-06-01*
