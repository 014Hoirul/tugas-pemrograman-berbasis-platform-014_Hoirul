# Laporan Tugas Mandiri 2
## Menyusun Tata Letak dengan Class Utility

### 1. Tujuan
Memahami penggunaan class utility Tailwind CSS untuk menyusun halaman web yang responsif, meliputi navbar, hero, kartu konten, dan footer.

### 2. Hasil Pengerjaan
Saya membuat halaman Profil Mahasiswa dengan tema biru yang terdiri dari navbar, bagian pembuka (hero), tiga kartu konten yaitu Biodata, Jadwal Kuliah, dan Kegiatan, serta footer. Halaman menggunakan Tailwind CSS melalui CDN tanpa menambahkan CSS buatan sendiri.

### 3. Class Utility dan Fungsinya

| Bagian | Class Utility | Fungsi |
|---|---|---|
| Navbar | `flex`, `flex-wrap`, `justify-between`, `gap-3` | Menyusun logo dan menu navigasi serta memberikan jarak. |
| Navbar | `bg-blue-700`, `text-white` | Memberikan latar biru dan teks putih. |
| Hero | `grid`, `grid-cols-1`, `md:grid-cols-2`, `gap-8` | Menyusun hero dalam satu kolom pada layar kecil dan dua kolom pada layar menengah ke atas. |
| Hero | `text-3xl`, `md:text-5xl` | Menyesuaikan ukuran judul berdasarkan ukuran layar. |
| Hero | `bg-gradient-to-br`, `from-blue-700`, `to-blue-500` | Membuat latar belakang dengan gradasi biru. |
| Kartu konten | `grid`, `grid-cols-1`, `sm:grid-cols-2`, `md:grid-cols-3` | Mengatur jumlah kolom kartu sesuai ukuran layar. |
| Kartu konten | `gap-5`, `md:gap-6` | Mengatur jarak antarkartu. |
| Kartu konten | `rounded-2xl`, `bg-white`, `shadow-sm` | Membuat sudut membulat, latar putih, dan bayangan ringan. |
| Efek hover | `transition`, `hover:-translate-y-1`, `hover:shadow-xl` | Memberikan animasi, mengangkat kartu sedikit, dan memperbesar bayangan ketika kursor diarahkan ke kartu. |
| Tombol | `bg-blue-600`, `hover:bg-blue-800` | Mengubah warna tombol dari biru menjadi biru lebih gelap ketika kursor berada di atasnya. |
| Footer | `bg-blue-950`, `text-white`, `text-center` | Membuat footer berwarna biru gelap dengan teks putih yang rata tengah. |

### 4. Pengujian Responsivitas
Saya menguji halaman pada tampilan laptop dan viewport dengan lebar 360 px. Pada layar kecil, navbar dapat membungkus elemen jika ruang tidak cukup, bagian hero tersusun dalam satu kolom, dan kartu konten ditampilkan dalam satu kolom. Pada layar yang lebih lebar, hero berubah menjadi dua kolom dan kartu konten menjadi tiga kolom mulai breakpoint `md`.

### 5. Bagian yang Mudah dan Sulit Disusun
Menurut saya, bagian yang paling mudah disusun menggunakan class utility adalah kartu konten karena jarak, warna, sudut, bayangan, dan efek hover dapat diatur langsung melalui class Tailwind. Bagian yang lebih sulit dibaca adalah elemen hero karena memiliki banyak class untuk mengatur grid, ukuran teks, warna, jarak, dan responsivitas. Meskipun demikian, pendekatan utility-first memudahkan perubahan tampilan tanpa perlu membuat aturan CSS sendiri.

### 6. Kesimpulan
Tailwind CSS memudahkan penyusunan halaman web responsif melalui class utility. Class seperti `grid-cols-1`, `md:grid-cols-3`, dan `gap-5` membantu mengatur susunan serta jarak elemen. Sementara itu, prefiks `hover:` memberikan perubahan tampilan saat kursor diarahkan ke elemen. Penggunaan prefiks responsif seperti `md:` memungkinkan tata letak menyesuaikan ukuran layar.
