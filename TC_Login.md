\# Test Case: Fitur Login



\*\*Aplikasi:\*\* Toko Online  

\*\*Modul:\*\* Autentikasi  

\*\*Tester:\*\* Balqis Naurah Hanifah  

\*\*Tanggal:\*\* 2026-05-10  



\---



| TC ID | Skenario | Langkah Pengujian | Test Data | Expected Result | Status |

|-------|----------|-------------------|-----------|-----------------|--------|

| TC-LG-001 | Login dengan kredensial valid | 1. Buka halaman login 2. Masukkan email dan password valid 3. Klik tombol Login | Email: user@test.com, Password: Test1234 | User berhasil masuk dan diarahkan ke halaman dashboard | PASS |

| TC-LG-002 | Login dengan password salah | 1. Buka halaman login 2. Masukkan email valid dan password salah 3. Klik tombol Login | Email: user@test.com, Password: salah123 | Muncul pesan error "Email atau password salah" | PASS |

| TC-LG-003 | Login dengan email tidak terdaftar | 1. Buka halaman login 2. Masukkan email yang belum terdaftar 3. Klik tombol Login | Email: tidakada@test.com, Password: Test1234 | Muncul pesan error "Email tidak terdaftar" | PASS |

| TC-LG-004 | Login dengan field email kosong | 1. Buka halaman login 2. Biarkan field email kosong 3. Klik tombol Login | Email: (kosong), Password: Test1234 | Muncul validasi "Email wajib diisi" | PASS |

| TC-LG-005 | Login dengan field password kosong | 1. Buka halaman login 2. Masukkan email valid 3. Biarkan field password kosong 4. Klik tombol Login | Email: user@test.com, Password: (kosong) | Muncul validasi "Password wajib diisi" | PASS |

| TC-LG-006 | Login dengan format email tidak valid | 1. Buka halaman login 2. Masukkan email tanpa @ 3. Klik tombol Login | Email: usertest.com, Password: Test1234 | Muncul validasi "Format email tidak valid" | PASS |

| TC-LG-007 | Login dengan kedua field kosong | 1. Buka halaman login 2. Biarkan semua field kosong 3. Klik tombol Login | Email: (kosong), Password: (kosong) | Muncul validasi untuk kedua field | PASS |

| TC-LG-008 | Login dengan SQL injection | 1. Buka halaman login 2. Masukkan SQL injection di field email 3. Klik tombol Login | Email: ' OR 1=1 --, Password: test | Muncul pesan error, bukan akses ke dashboard | PASS |

| TC-LG-009 | Fitur "Tampilkan Password" | 1. Buka halaman login 2. Masukkan password 3. Klik ikon mata di field password | Password: Test1234 | Password berubah dari tersembunyi menjadi terlihat | PASS |

| TC-LG-010 | Login lalu tekan tombol Back | 1. Login dengan kredensial valid 2. Setelah masuk dashboard, tekan tombol Back browser | - | User tidak kembali ke halaman login (session aktif) | PASS |

