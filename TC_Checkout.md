\# Test Case: Fitur Checkout



\*\*Aplikasi:\*\* Toko Online  

\*\*Modul:\*\* Transaksi  

\*\*Tester:\*\* Balqis Naurah Hanifah  

\*\*Tanggal:\*\* 2026-05-10  



\---



| TC ID | Skenario | Langkah Pengujian | Test Data | Expected Result | Status |

|-------|----------|-------------------|-----------|-----------------|--------|

| TC-CO-001 | Checkout dengan keranjang berisi 1 produk | 1. Tambah 1 produk ke keranjang 2. Buka halaman checkout 3. Isi alamat pengiriman 4. Pilih metode pembayaran 5. Klik "Bayar Sekarang" | Produk: Kaos Polos (Rp 75.000), Qty: 1 | Pesanan berhasil dibuat, muncul halaman konfirmasi | PASS |

| TC-CO-002 | Checkout dengan keranjang berisi banyak produk | 1. Tambah 3 produk berbeda ke keranjang 2. Lakukan checkout | 3 produk berbeda | Total harga terhitung benar, pesanan berhasil | PASS |

| TC-CO-003 | Checkout dengan keranjang kosong | 1. Pastikan keranjang kosong 2. Coba akses halaman checkout | Keranjang kosong | Muncul pesan "Keranjang Anda kosong" atau diarahkan ke halaman produk | PASS |

| TC-CO-004 | Ubah quantity produk di keranjang | 1. Tambah produk ke keranjang 2. Ubah quantity menjadi 3 3. Cek total harga | Qty: 1 diubah ke 3 | Total harga diperbarui (harga x 3) | PASS |

| TC-CO-005 | Hapus produk dari keranjang | 1. Tambah 2 produk ke keranjang 2. Hapus 1 produk 3. Cek keranjang | 2 produk, hapus 1 | Hanya tersisa 1 produk, total diperbarui | PASS |

| TC-CO-006 | Checkout tanpa mengisi alamat pengiriman | 1. Tambah produk ke keranjang 2. Buka checkout 3. Biarkan alamat kosong 4. Klik "Bayar" | Alamat: (kosong) | Muncul validasi "Alamat wajib diisi" | PASS |

| TC-CO-007 | Checkout tanpa memilih metode pembayaran | 1. Tambah produk ke keranjang 2. Isi alamat 3. Tidak pilih metode pembayaran 4. Klik "Bayar" | Metode pembayaran: tidak dipilih | Muncul validasi "Pilih metode pembayaran" | PASS |

| TC-CO-008 | Checkout dengan kupon diskon valid | 1. Tambah produk ke keranjang 2. Masukkan kode kupon valid 3. Klik "Terapkan" | Kode: DISKON10 | Harga berkurang 10%, total diperbarui | PASS |

| TC-CO-009 | Checkout dengan kupon diskon tidak valid | 1. Tambah produk ke keranjang 2. Masukkan kode kupon yang salah 3. Klik "Terapkan" | Kode: SALAH123 | Muncul pesan "Kode kupon tidak valid" | PASS |

| TC-CO-010 | Checkout dengan quantity melebihi stok | 1. Tambah produk ke keranjang 2. Ubah quantity melebihi stok 3. Coba checkout | Qty: 999 (stok hanya 50) | Muncul pesan "Stok tidak mencukupi" | PASS |

