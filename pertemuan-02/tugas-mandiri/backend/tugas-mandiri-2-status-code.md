## Tugas Mandiri 2 - Memahami HTTP Status Code
### Tujuan:
untuk memahami arti berbagai HTTP status code serta mengetahui perbedaan respons berhasil, kesalahan dari client, dan
kesalahan dari server.

## Tabel Hasil Pengujian
| Status Code | Arti | Hasil Pengujian | Kapan Digunakan |
|---:|---|---:|---|
| 200 | OK / berhasil | Server mengembalikan status 200 OK dan tidak ada isi response body | Digunakan ketika request berhasil diproses, misalnya mengambil data berhasil |
| 201 | Created / berhasil dibuat | Server mengembalikan status 201 Created dan tidak ada isi response body | Digunakan ketika request berhasil membuat data baru, misalnya menambahkan pengguna baru |
| 400 | Bad Request / permintaan tidak valid | Server mengembalikan status 400 Bad Request dan tidak ada isi response body | Digunakan ketika request dari client memiliki data atau format yang salah |
| 401 | Unauthorized / belum terautentikasi | Server mengembalikan status 401 Unauthorized dan tidak ada isi response body | Digunakan ketika pengguna belum melakukan login atau kredensial yang diberikan tidak valid |
| 403 | Forbidden / akses ditolak | Server mengembalikan status 403 Forbidden dan tidak ada isi response body | Digunakan ketika pengguna sudah dikenali tetapi tidak memiliki izin untuk mengakses suatu sumber daya |
| 404 | Not Found / tidak ditemukan | Server mengembalikan status 404 Not Found dan tidak ada isi response body | Digunakan ketika URL atau data yang diminta tidak ditemukan |
| 500 | Internal Server Error / kesalahan server | Server mengembalikan status 500 Internal Server Error dan tidak ada isi response body | Digunakan ketika terjadi kesalahan internal pada proses server |
