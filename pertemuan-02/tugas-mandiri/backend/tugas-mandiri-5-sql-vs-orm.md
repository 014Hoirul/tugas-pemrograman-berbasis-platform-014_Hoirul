## Tugas Mandiri 5 — Membandingkan SQL Mentah dan ORM
### Tujuan:
untuk memahami perbedaan penggunaan SQL mentah dan ORM dalam melakukan operasi database, serta mengetahui kelebihan masing-masing pendekatan dan 
pentingnya penggunaan parameter query untuk mengurangi risiko SQL injection.

### Perbandingan SQL Mentah dan ORM
| Aspek | SQL Mentah | ORM Prisma |
|---|---|---|
| Bentuk kode | Menggunakan sintaks SQL | Menggunakan method dari prisma |
| Menambahkan data | Menggunakan INSERT INTO | Menggunakan create() |
| Pengaturan query | Query ditulis sendiri | Query dikelola oleh ORM |
| Fleksibilitas | Lebih leluasa dalam membuat query | Bergantung pada fitur ORM |
| Kemudahan Pengguna | Perlu memahami SQL | Lebih praktis untuk operasi umum |
| Interaksi database | Dilakukan melalui query yang ditulis programmer | Ditangani melalui model dan method ORM |

### 1. Apa perbedaan cara penulisan operasi database menggunakan SQL secara langsung dan ORM?
Pada SQL mentah, programmer menuliskan perintah database secara langsung sesuai dengan sintaks SQL. Contohnya menggunakan INSERT INTO untuk 
memasukkan data ke tabel jadwal. Sementara itu, ORM menyediakan fungsi tertentu untuk menjalankan operasi database. Pada contoh Prisma, proses 
tersebut dilakukan menggunakan prisma.jadwal.create(). Jadi, programmer lebih banyak bekerja dengan struktur object dan method daripada menulis 
query SQL secara langsung.
### 2. Apa kelebihan SQL mentah?
SQL mentah memberikan keleluasaan kepada programmer untuk mengatur query sesuai kebutuhan. Programmer juga dapat menggunakan berbagai fitur SQL 
dan membuat query yang lebih spesifik jika diperlukan.
### 3. Apa kelebihan ORM?
ORM membuat kode program untuk database menjadi lebih praktis. Programmer tidak perlu membuat query SQL satu per satu untuk operasi database yang 
umum. Dengan ORM seperti Prisma, operasi menambahkan, membaca, mengubah, dan menghapus data dapat dilakukan menggunakan method yang sudah 
tersedia. Struktur kode juga biasanya lebih mudah dipahami karena mengikuti bahasa pemrograman yang digunakan.
### 4. Apa yang dimaksud dengan SQL injection, dan apa dampaknya terhadap data aplikasi?
SQL injection merupakan teknik serangan dengan memasukkan input tertentu yang dapat memengaruhi query SQL yang dijalankan oleh aplikasi. Jika 
aplikasi tidak melakukan pengamanan input dengan baik, serangan ini dapat dimanfaatkan untuk memperoleh informasi yang seharusnya tidak bisa 
diakses. Dalam kondisi tertentu, data juga dapat diubah atau dihapus sehingga dapat merugikan aplikasi dan penggunanya.
###  5. Mengapa penggunaan parameter query dapat mengurangi risiko SQL injection?
Karena Penggunaan parameter query dapat mengurangi risiko SQL injection *karena* data yang dimasukkan oleh pengguna dipisahkan dari perintah SQL 
yang dijalankan. Dengan menggunakan parameter seperti tanda ?, input pengguna akan dianggap sebagai data dan bukan sebagai bagian dari perintah 
SQL. Jadi, apabila pengguna memasukkan karakter atau perintah SQL tertentu, input tersebut tidak langsung dijalankan sebagai query oleh database.
### 6. Bagaimana ORM membantu pengembang mengakses database?
ORM membantu pengembang mengakses database *karena* ORM menyediakan method yang dapat digunakan untuk melakukan operasi database tanpa harus 
menulis query SQL secara langsung. Pada contoh sebelumnya, penambahan data dilakukan menggunakan method create() pada Prisma. Dengan cara 
tersebut, pengembang cukup menentukan data yang ingin dimasukkan, sedangkan proses pembuatan query untuk database ditangani oleh ORM. Selain itu, 
SQL mentah cocok digunakan ketika query yang dibutuhkan cukup kompleks dan membutuhkan pengaturan langsung terhadap proses pengambilan atau 
pengolahan data.
