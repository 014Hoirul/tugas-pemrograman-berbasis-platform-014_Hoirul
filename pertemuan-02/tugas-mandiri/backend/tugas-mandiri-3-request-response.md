## Tugas Mandiri 3 — Memahami Request dan Response
### Tujuan:
untuk memahami proses request dan response antara client dan server serta mengetahui fungsi query parameter dan HTTP header dalam sebuah permintaan HTTP.

### 1. Apa yang dimaksud dengan permintaan (request), dan pihak mana yang mengirimkannya?
Request adalah permintaan yang dikirimkan oleh client kepada server untuk meminta suatu data atau melakukan suatu proses. Contohnya ketika browser
atau Thunder Client mengirim GET https://httpbin.org/get kepada server HTTPBin.
### 2. Apa yang dimaksud dengan respons (response), dan pihak mana yang mengirimkannya?
Response adalah jawaban yang dikirimkan oleh server kepada client setelah server menerima dan memproses request. Response dapat berisi status code, 
header, dan data yang diminta.
### 3. Apa fungsi query parameter?
Query parameter digunakan untuk mengirimkan informasi tambahan kepada server melalui URL.
Pada pengujian: https://httpbin.org/get?nama=Hoirul&kelas=TI 
terdapat dua query parameter:
- nama=Hoirul → mengirimkan nama pengguna.
- kelas=TI → mengirimkan informasi kelas.
Server kemudian menampilkan kembali kedua data tersebut pada bagian args dalam response.
### 4. Apa fungsi HTTP header?
HTTP header berfungsi untuk memberikan informasi tambahan mengenai request atau response, seperti jenis data, informasi client, dan jenis browser 
atau aplikasi yang digunakan. Salah satu header yang dapat terlihat adalah: User-Agent. Header tersebut memberikan informasi mengenai client atau 
aplikasi yang digunakan untuk mengirim request.
### 5. Apa perbedaan penempatan data pada query parameter di URL dan pada body permintaan?
Query parameter ditempatkan langsung pada URL setelah tanda ?, contohnya: https://httpbin.org/get?nama=Hoirul&kelas=TI.
Sedangkan body digunakan untuk menempatkan data di dalam isi request, biasanya digunakan pada method seperti POST, PUT, atau PATCH. Contohnya:
{
  "nama": "Hoirul",
  "kelas": "TI"
}
Jadi, perbedaannya adalah query parameter terlihat pada URL, sedangkan data body dikirim di dalam isi request.


## Screenshot Pengujian
### 1. GET


### 2. HEADER
