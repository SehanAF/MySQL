# Agenda
1. Pengenalan MySQL.
2. Menginstall MySQL.
3. Tipe Data.
~ Database, Table.
~ Insert, Update, Delete, Select. 
~ Transaction.
~ Table Relationship.
~ Join
~ Dan lain-lain.

 # Perintah Dan Penjelasan
~ Jika ingin menghentikan atau menyalakan MySQL, cukup search di window (bar bagian bawah kiri)lalu ketik services -> lalu cari MySQL80 lalu tekan -> lalu tekan tombol stop atau sebaliknya yaitu start.
- jika ingin login ke MySQL, cukup search CMD di window, lalu masukan/ketik "mysql -uroot -p". Lalu jika ingin mengecek versi MySQL, cukup dengan perintah "select version(); " .
~ Setiap melakukan perintah di CMD MySQL, wajib menggunakan akhiran ; contoh nya jika ingin mengecek versi MySQL " select version(); ". Kalau tidak ada akhiran ; si perintah tersebut tidak akan dikirim.
~ Jika ingin melihat Database, cukup ke cmd lalu ketikan perintah " show databases; "
~ Cara membuat Database baru di CMD. Untuk membuat database caranya sangat sederhana yaitu perintah nya cukup menggunakan "create database nama_database; ". Untuk nama_database harus jangan ada spasi nya,harus menggunakan underscore " _ " dsb. Jadi biasanya di MySQL itu kebanyakan orang bikin nama database, nama table, nama kolom itu selalu memakai huruf kecil semua, jadi jarang menggunakan huruf besar. Walaupun tidak ada aturannya juga, jadi jika ingin menggunakan huruf besar juga tidak ada masalah. Tapi kebiasaan kebanyakan orang itu selalu menggunakan huruf kecil semua.
~ Jika ingin menghapus Database,cukup menggunakan perintah " drop database nama_database; ". Perlu diingat jika kita menghapus database maka tabel-tabel atau data di dalam nya akan terhapus semua. Jadi perlu diingat untuk membuat BackUp nya dulu sebelum menghapus database, untuk jaga jaga bila diperlukan.
~ Jika ingin memilih database yang akan digunakan cukup menggunakan perintah " use nama_database; ". Keuntungan nya dalah jika ingin memasukan table atau data kita harus memilih database terlebih dahulu agar table tersebut bisa disimpan di salah satu database. jika tidak akan terjadi error.
~ Jika ingin melihat table di database cukup masukan perintah " show tables; "

# Pengenalan Database Management System
~ DBMS adalah aplikasi yang digunakan untuk me-manage data.
~ Tanpa menggunakan DBMS, untuk me-manage data, seperti data produk, data customer, data penjualan, kita harus simpan dalam bentuk file( misal seperti kita menggunakan Excel. )
~ DBMS biasanya berjalan sebagai aplikasi server yang digunakan utuk me-manage data, kita hanya tinggal memberi perintah ke DBMS untuk melakukan proses manjemen datanya, seperti menambah, mengubah, menghapus atau mengambil data.
~ Contoh DBMS yang populer seperti MySQL, PostgreSQL, MongoDB, Oracle, dan lain-lain.

# Pengenalan Relational Database
~ Ada banyak sekali jenis-jenis DBMS, seperti Relational Database, Document Database, Key-Value Database, dan lain-lain.
~ Namun yang masih populer dan kebanyakan orang gunakan adalah relational database.
~ Relational database cukup mudah dimengerti dan dipelajari karena kita sudah terbiasa menyimpan data dalam bentuk tabular (tabel) seperti di Microsoft Excel atau di Google Doc Spreadsheet.
~ Selain itu relational database memiliki perintah standard menggunakan SQL, sehingga kita mudah ketika ingin berganti-ganti aplikasi database ( seperti MySQL, Oracle, PostgreSQL, dll. )

# Cara Kerja DBMS
~ Database Client dikirim ke -> Database Management System lalu dikirim lagi ke -> Database file. lebih jelasnya lihat saja di youtube pak eko.

# Databse Client
~ Database client adalah aplikasi yang digunakan untuk berkomunikasi dengan DBMS.
~ Biasanya DBMS sudah menyediakan database client sederhana yang bisa kita gunakan untuk berkomunikasi dengan DBMS agar lebih mudah.
~ Atau kita bisa membuat aplikasi untuk berkomunikasi dengan DBMS, misal membuat aplikasi database client menggunakan Java, PHP atau bahasa pemrograman lainnya.

# Database File 
~ Mayoritas DBMS menyimpan datanya di file, walaupun ada beberapa database yang hanya menyimpan datanya di memory (RAM).
~ Namun jangan berpikir file database yang disimpan berula file seperti Excel atau CSV ( Comma Separated Value ), tapi jauh lebih kompleks.
~ Database file akan dioptimasi oleh DBMS agar mempermudah DBMS dalam manajemen datanya, seperti insert, update, delete, dan select.
~ Tiap DBMS biasanya memiliki cara masing-masing mengelola Database File nya, dan kita tidak perlu harus tau, karena yang kita perlu hanya cara berkomunikasi ke DBMS.

# SQL
~ Structured Query Language.
~ Merupakan bahasa yang digunakan untuk mengirim perintah ke DBMS.
~ SQL adalah bahasa yang mudah karena hanya berisi instruksi untuk menyimpan, mengubah, menghapus atau mengambil data melalui DBMS.
~ Secara garis besar, semuah perintah SQL  di relational Database itu sama, namun biasanya tiap DBMS ada improvement yang membedakan hal-hal kecil dalam perintah SQL, namun secara garis besar perintahnya tetap sama.

# MySQL
~ MySQL adalah DBMS Relational OperSource yang paling populer didunia saat ini.
~ Tidak hanya OpenSource, MySQL juga gratis untuk digunakan.
~ MySQL pertama kali dibuat dan diperkenalkan tahun 1995 oleh David Axmark dan Michael Widenius.
~ MySQL sangat populer sekali terutama dikalangan programmer web PHP.
~ https://www.mysql.com/

# MySQL Community vs MySQL Enterprise
~ Saat kita membuka halaman website resmi MySQL, jangan sampai salah download aplikasi MySQL.
~ MySQL menawarkan pilihan versi MySQL Enterprise, yaitu DBMS MySQL yang berbayar.
~ MySQL yang versi gratis adalah MySQL Community.
~ MySQL Enterprise sendiri lebih ke versi improvement dari MySQL Community, biasanya menambahkan support dan monitoring.
~ Jika menggunakan MySQL Community, maka kita harus tangani semuanya sendiri, dari masalah dan monitorin MySQL nya.

# MySQL vs MariaDB
~ Tahun 2008 MySQL di akuisisi leh perusahaan Sun Microsystem.
~ Namun tahun 2009, Sun Microsystem diakuisisi oleh perusahaan Oracle (Pemiliki DBMS Oracle).
~ Hal ini menyebabkan 2 founder MySQL keluar dari MySQL dan membuat project baru bernama MariaDB.
~ MariaDB Sebenarnya fork dari MySQL, jadi apa yang bisa dilakukan di MySQL bisa dilakukan di MariaDB.
~ Sehingga sekarang jangan terlalu bingung jika ada MySQL dan MariaDB, karena sebenarnya itu dari source code yang sama, mungkin ada perbedaan kecil, namun secara garis besar sebenarnya tetap sama.
~ https://mariadb.org/

# Database
~ Database adalah tempak kita menyimpan table di MySQL.
~ Jika kita misalkan table di MySQL adalah sebuah file, maka database adalah folder nya, dimana kita bisa menyimpan banyak table di sebuah database.
~ Biasanya pembuatan kita akan membuat satu database untuk satu jenis aplikasi, walaupun satu aplikasi bisa menggunakan lebih dari satu database, namun lumrahnya, satu aplikasi akan menggunakan satu database.

# Tipe Data
~ Saat kita membuat table di Excel, kita bisa menentukan tipe data apa yang kita masukkan ke tiap kolom Excel. Jika di excel tipe data tiap kolom bisa di ubah ubah contoh nya ada sebuah kolom yang dulunya angka lalu saya ubah di baris keberapa menjadi text lalu dibaris ke berapa lagi menjadi tanggal. Nah kalau di MySQL tidak bisa seperti itu, jadi satu kolom itu harus 1 tipe data. 
~ Di MySQL, kita juga bisa menentukan tipe data tiap kolom yang kita buat di sebuah tabel. 
~ Ada banyak sekali tipe data yang tersedia di MySQL, dari yang sederhana, sampai yang kompleks.
~ Biasanya kita akan menggunakan tipe data sesuai dengan kebutuhan kolom yang perlu kita buat.

# Tipe Data per Kolom
~ Lihat contoh tabel nya di Buku kuning dengan judul Pelajaran Pemrograman pada tanggal 15-07-2022, halaman 42.

# Tipe Data Number
~ Secara garis besar, tipe data number di MySQL ada dua jenis yaitu :
~ Integer, atau tipe number bilangan bulat.
~ Floating Point, atau tipe data number pecahan.
~ Untuk lihat tabel nya tersedia di buku kuning dengan judul Pelajaran Pemrograman pada tanggal 15-07-2022, halaman 42-43. ]

#Gambar Integer

https://github.com/SehanAF/MySQL/issues/1#issue-1306678097
