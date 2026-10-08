# Tugas Mandiri 1 — Mengenal HTTP Method dan Endpoint
### Tujuan:
untuk memahami penggunaan HTTP method dan endpoint serta mengetahui hubungan antara request, data yang dikirim, status HTTP,
dan response yang diberikan oleh server.

## Tabel Hasil Pengujian 
| No. | Method | Endppoint | Data yang dikirim | Status | Hasil |
|---:|---|---|---|---:|---|
| 1. | GET | '/get' | URL : 'https://httpbin.org/get?nama=Hoirul&nim=2024520014' | 200 | Request berhasil dan parameter dikembalikan pada response |
| 2. | POST | '/post' | URL : 'https://httpbin.org/post' JSON : '{"nama":"Hoirul","nim":"2024520014"}' | 200 | Request berhasil dan data JSON ditampilkan kembali |
| 3. | PUT | '/put' | URL : 'https://httpbin.org/put' JSON : '{"nama":"Hoirul","nim":"2024520014"}' | 200 | Request berhasil dan data JSON ditampilkan kembali |
| 4. | PATCH | '/patch' | URL : 'https://httpbin.org/patch' JSON : '{"nama":"Hoirul","nim":"2024520014"}' | 200 | Request berhasil dan data JSON ditampilkan kembali |
| 5. | DELETE | '/delete' | URL : 'https://httpbin.org/delete' | 200 | Request DELETE berhasil dan informasi request ditampilkan kembali |

## Screenshot Pengujian 
![Hasil Pengujian](./screenshot/TAHAP-9-1.png)
