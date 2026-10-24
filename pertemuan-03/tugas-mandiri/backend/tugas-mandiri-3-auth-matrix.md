# Tugas Mandiri 3 — Analisis Authentication dan Authorization

## 1. Peran Pengguna

Pada project Elibrary, terdapat tiga peran pengguna, yaitu:

1. **Anggota:** mencari buku, meminjam buku, mengembalikan buku, memperpanjang peminjaman, dan mengunduh e-book.
2. **Pustakawan:** mengelola katalog buku, mencatat peminjaman dan pengembalian, serta mengelola data koleksi perpustakaan.
3. **Pimpinan:** melihat laporan peminjaman, statistik buku populer, dan laporan aktivitas anggota.

## 2. Matriks Hak Akses

| Fitur | Anggota | Pustakawan | Pimpinan | Endpoint |
|---|:---:|:---:|:---:|---|
| Melihat katalog buku | ✅ | ✅ | ✅ | `GET /buku` |
| Meminjam buku | ✅ | ✅ | ❌ | `POST /peminjaman` |
| Memperpanjang peminjaman | ✅ | ✅ | ❌ | `PATCH /peminjaman/:id/perpanjang` |
| Mengembalikan buku | ❌ | ✅ | ❌ | `PATCH /peminjaman/:id/pengembalian` |
| Menambah katalog buku | ❌ | ✅ | ❌ | `POST /buku` |
| Mengubah data buku | ❌ | ✅ | ❌ | `PUT /buku/:id` |
| Menghapus data buku | ❌ | ✅ | ❌ | `DELETE /buku/:id` |
| Mengunduh e-book | ✅ | ❌ | ❌ | `GET /ebook/:id/download` |
| Melihat laporan peminjaman | ❌ | ✅ | ✅ | `GET /laporan/peminjaman` |
| Melihat statistik perpustakaan | ❌ | ❌ | ✅ | `GET /laporan/statistik` |

Keterangan: ✅ berarti peran tersebut diizinkan mengakses fitur, sedangkan ❌ berarti akses ditolak dengan kode `403` apabila pengguna sudah login dan tokennya valid. Matriks ini merupakan rancangan hak akses yang akan diterapkan pada sistem.

## 3. Perbedaan Authentication dan Authorization

**Authentication (autentikasi)** adalah proses memeriksa identitas pengguna, misalnya melalui login dan token. Sementara itu, **Authorization (otorisasi)** adalah proses memeriksa apakah pengguna yang identitasnya sudah terverifikasi memiliki izin untuk menggunakan fitur tertentu.

Kode `401 Unauthorized` digunakan ketika permintaan ke endpoint yang dilindungi tidak menyertakan token atau menggunakan token yang tidak valid. Contohnya, pengguna yang belum login mencoba mengakses `POST /buku`, sehingga sistem menolak permintaan karena identitasnya belum terverifikasi.

Kode `403 Forbidden` digunakan ketika pengguna memiliki token valid, tetapi tidak mempunyai hak akses yang diperlukan. Contohnya, anggota mencoba mengakses `POST /buku` untuk menambahkan katalog, padahal fitur tersebut hanya boleh digunakan oleh pustakawan. Sistem mengenali identitas anggota tersebut, tetapi menolak akses karena perannya tidak sesuai.

## 4. Risiko Jika Endpoint Hanya Menggunakan `requireAuth`

Jika endpoint `POST /buku` hanya menggunakan `requireAuth`, sistem hanya memastikan bahwa pengguna sudah login tanpa memeriksa perannya. Akibatnya, anggota yang sudah login dapat menambahkan katalog buku meskipun tidak memiliki izin. Untuk mencegah hal tersebut, endpoint harus menggunakan `requireAuth` dan `requireRole('pustakawan')` agar hanya pustakawan yang dapat menambahkan katalog.
