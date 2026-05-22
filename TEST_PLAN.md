\# Test Plan - Aplikasi Toko Online



\*\*Versi:\*\* 1.0  

\*\*Tester:\*\* Balqis Naurah Hanifah  

\*\*Tanggal:\*\* 2026-05-10  



\---



\## 1. Pendahuluan



Dokumen ini menjelaskan strategi dan pendekatan pengujian untuk aplikasi web toko online sebelum dirilis ke production. Test plan ini disusun berdasarkan spesifikasi fitur dan kebutuhan bisnis.



\---



\## 2. Ruang Lingkup Pengujian



\### 2.1 In Scope



| Modul | Fitur yang Diuji |

|-------|------------------|

| Autentikasi | Login, Registrasi, Logout, Reset Password |

| Produk | Katalog, Detail Produk, Pencarian, Filter |

| Keranjang | Tambah, Ubah Quantity, Hapus, Subtotal |

| Checkout | Alamat Pengiriman, Metode Pembayaran, Kupon Diskon |

| Profil | Edit Profil, Histori Pesanan |



\### 2.2 Out of Scope



Pengujian payment gateway integration dilakukan terpisah oleh tim payment, pengujian performance dan load testing dilakukan setelah functional testing selesai, pengujian email notification dilakukan di lingkungan staging dengan mock email server.



\---



\## 3. Jenis Pengujian



| Jenis | Deskripsi | Tools |

|-------|-----------|-------|

| Functional Testing | Memastikan setiap fitur bekerja sesuai spesifikasi | Manual + Postman |

| UI Testing | Memvalidasi tampilan dan responsivitas | Manual (Browser DevTools) |

| API Testing | Memvalidasi response endpoint backend | Postman, pytest |

| Security Testing | Pengujian dasar terhadap SQL injection dan XSS | Manual |

| Compatibility Testing | Memastikan kompatibilitas multi-browser dan device | Manual |



\---



\## 4. Test Environment



| Komponen | Spesifikasi |

|----------|-------------|

| OS | Windows 11, Android 14, iOS 17 |

| Browser | Chrome 130, Firefox 131, Safari 17, Edge 130 |

| Resolusi Desktop | 1920x1080, 1366x768 |

| Resolusi Mobile | 360x800, 414x896 |

| Test Data | Database staging dengan 100 user dan 50 produk |



\---



\## 5. Kriteria Penerimaan



\### 5.1 Entry Criteria



Pengujian dimulai apabila build aplikasi sudah di-deploy ke staging environment, dokumen spesifikasi fitur sudah final dan disetujui, test environment sudah siap dengan test data yang sesuai, dan unit testing dari sisi development sudah selesai dengan minimal 80% coverage.



\### 5.2 Exit Criteria



Pengujian dianggap selesai apabila semua test case prioritas High dan Critical sudah dijalankan, tidak ada bug Critical atau High yang masih Open, minimal 95% test case berstatus Pass, semua bug yang ditemukan sudah didokumentasikan, dan UAT sudah disetujui oleh stakeholder.



\---



\## 6. Risiko dan Mitigasi



| Risiko | Dampak | Mitigasi |

|--------|--------|----------|

| Perubahan spesifikasi di tengah pengujian | Test case harus direvisi | Maintain komunikasi rutin dengan PM, gunakan tools tracking |

| Bug ditemukan di akhir pengujian | Delay rilis | Eksekusi test case High priority lebih awal |

| Test environment tidak stabil | Pengujian terganggu | Koordinasi dengan DevOps untuk monitoring environment |

| Test data tidak mencukupi | Tidak bisa cover semua skenario | Siapkan test data generator atau pengisian manual bertahap |



\---



\## 7. Skedul Pengujian



| Fase | Durasi | Aktivitas |

|------|--------|-----------|

| Persiapan | 2 hari | Setup environment, persiapan test data, review spec |

| Functional Testing | 5 hari | Eksekusi test case modul Autentikasi, Produk, Keranjang, Checkout |

| Bug Fixing \& Retest | 3 hari | Verifikasi bug yang sudah diperbaiki |

| UAT | 2 hari | Pengujian akhir dengan stakeholder |

| Sign-off | 1 hari | Persetujuan final dan dokumentasi hasil |



\---



\## 8. Tim dan Tanggung Jawab



| Role | Tanggung Jawab |

|------|----------------|

| QA Tester | Eksekusi test case, identifikasi bug, dokumentasi hasil |

| Developer | Memperbaiki bug yang dilaporkan, mendukung debugging |

| Product Manager | Memberikan klarifikasi requirement, review hasil UAT |

| Stakeholder | Memberikan approval UAT |



\---



\## 9. Deliverables



Output yang dihasilkan dari proses pengujian meliputi dokumen test case yang sudah dieksekusi dengan status pass/fail, bug report untuk setiap masalah yang ditemukan, UAT checklist dengan status final, dan summary report yang merangkum hasil keseluruhan pengujian.

