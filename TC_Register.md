\# Test Case: Fitur Registrasi



\*\*Aplikasi:\*\* Toko Online  

\*\*Modul:\*\* Autentikasi  

\*\*Tester:\*\* Balqis Naurah Hanifah  

\*\*Tanggal:\*\* 2026-05-10  



\---



| TC ID | Skenario | Langkah Pengujian | Test Data | Expected Result | Status |

|-------|----------|-------------------|-----------|-----------------|--------|

| TC-RG-001 | Registrasi dengan data valid | 1. Buka halaman registrasi 2. Isi semua field dengan data valid 3. Klik tombol Daftar | Nama: Test User, Email: newuser@test.com, Password: Test1234, Konfirmasi: Test1234 | Akun berhasil dibuat, user diarahkan ke halaman login | PASS |

| TC-RG-002 | Registrasi dengan email yang sudah terdaftar | 1. Buka halaman registrasi 2. Isi email yang sudah terdaftar 3. Klik tombol Daftar | Email: user@test.com (sudah ada) | Muncul pesan "Email sudah terdaftar" | PASS |

| TC-RG-003 | Registrasi dengan password kurang dari 8 karakter | 1. Buka halaman registrasi 2. Isi password kurang dari 8 karakter 3. Klik tombol Daftar | Password: abc12 | Muncul validasi "Password minimal 8 karakter" | PASS |

| TC-RG-004 | Registrasi dengan password dan konfirmasi tidak sama | 1. Buka halaman registrasi 2. Isi password dan konfirmasi berbeda 3. Klik tombol Daftar | Password: Test1234, Konfirmasi: Test5678 | Muncul validasi "Password dan konfirmasi tidak cocok" | PASS |

| TC-RG-005 | Registrasi dengan nama kosong | 1. Buka halaman registrasi 2. Biarkan field nama kosong 3. Klik tombol Daftar | Nama: (kosong) | Muncul validasi "Nama wajib diisi" | PASS |

| TC-RG-006 | Registrasi dengan format email tidak valid | 1. Buka halaman registrasi 2. Masukkan email tanpa domain 3. Klik tombol Daftar | Email: newuser@ | Muncul validasi "Format email tidak valid" | PASS |

| TC-RG-007 | Registrasi dengan semua field kosong | 1. Buka halaman registrasi 2. Tidak mengisi apapun 3. Klik tombol Daftar | Semua field kosong | Muncul validasi untuk semua field wajib | PASS |

| TC-RG-008 | Registrasi dengan nama mengandung karakter spesial | 1. Buka halaman registrasi 2. Isi nama dengan karakter spesial 3. Klik tombol Daftar | Nama: <script>alert('xss')</script> | Input disanitasi, tidak terjadi XSS | PASS |

