# REMEDIAL DATA WAREHOUSE UTDI
Tugas Remedial Data Warehouse UTDI

NAMA : FUKKAR AL WATHONI

NIM : 225611093

**MySQL**

MySQL adalah sistem manajemen basis data relasional (RDBMS) open-source yang paling populer di dunia. MySQL dikembangkan oleh perusahaan Swedia, MySQL AB, dan saat ini dimiliki oleh Oracle Corporation. RDBMS ini menggunakan Structured Query Language (SQL) sebagai antarmuka utama untuk mengelola dan mengakses data dalam basis data. MySQL banyak digunakan dalam berbagai aplikasi, mulai dari aplikasi web hingga sistem manajemen data perusahaan, karena kemampuannya yang handal, cepat, dan mudah diintegrasikan dengan berbagai platform.

**Arsitektur MySQL**

MySQL memiliki arsitektur client-server yang terdiri dari komponen utama seperti:

- Server MySQL: Ini adalah inti dari MySQL yang bertanggung jawab untuk menangani semua operasi basis data, seperti eksekusi query, penyimpanan data, dan manajemen transaksi.
- Client: Aplikasi yang terhubung ke server MySQL untuk mengirimkan query SQL. Ini bisa berupa command line interface (CLI), GUI tools, atau aplikasi berbasis web.
- Connectors: MySQL menyediakan berbagai konektor untuk berbagai bahasa pemrograman seperti PHP, Python, Java, dan lainnya yang memungkinkan aplikasi terhubung ke MySQL.

**Peran MySQL dalam Data Warehouse**

Dalam konteks Data Warehouse, MySQL bisa digunakan sebagai salah satu komponen utama untuk menyimpan, mengelola, dan memproses data yang berasal dari berbagai sumber data. Beberapa peran penting MySQL dalam Data Warehouse meliputi:

- Penyimpanan Data: MySQL digunakan untuk menyimpan data operasional yang akan dimuat ke dalam Data Warehouse. Dengan skema yang dirancang dengan baik, MySQL bisa mengelola tabel-tabel besar yang menyimpan data historis dan data agregat.
- ETL (Extract, Transform, Load): Proses ETL dalam Data Warehouse membutuhkan database yang handal untuk mengekstrak data dari berbagai sumber, melakukan transformasi sesuai kebutuhan bisnis, dan memuatnya ke dalam Data Warehouse. MySQL sering digunakan sebagai staging area dalam proses ini.
- Query dan Analisis Data: MySQL mendukung operasi query yang kompleks, termasuk agregasi, join, dan filter data, yang merupakan bagian penting dari analisis data dalam Data Warehouse.
- Replikasi dan Skalabilitas: MySQL mendukung replikasi basis data, yang memungkinkan Data Warehouse untuk didistribusikan ke beberapa server. Ini penting untuk meningkatkan performa dan skalabilitas, terutama ketika volume data yang dikelola sangat besar.

**Keunggulan dan Keterbatasan MySQL dalam Data Warehouse**

Keunggulan:

- Open Source: MySQL adalah solusi open-source yang dapat digunakan tanpa biaya lisensi.
- Kompatibilitas: MySQL mudah diintegrasikan dengan berbagai alat ETL, BI (Business Intelligence), dan platform data lainnya.
- Kinerja Tinggi: MySQL telah dioptimalkan untuk menangani beban kerja yang berat, terutama pada aplikasi web dan enterprise.

Keterbatasan:

- Skalabilitas Terbatas: Meskipun MySQL dapat direplikasi, untuk skala yang sangat besar, mungkin perlu menggunakan solusi lain seperti NoSQL databases atau RDBMS yang lebih canggih.
- Fitur Analitik Terbatas: MySQL lebih unggul sebagai RDBMS transaksional dibandingkan dengan sebagai alat analitik yang ekstensif seperti yang disediakan oleh Data Warehouse khusus.

**Kesimpulan**

MySQL adalah pilihan yang solid untuk menyimpan dan mengelola data dalam arsitektur Data Warehouse, terutama bagi organisasi yang membutuhkan solusi yang andal dan terjangkau. Meskipun memiliki beberapa keterbatasan dalam hal skalabilitas dan kemampuan analitik, dengan arsitektur yang tepat, MySQL dapat menjadi tulang punggung dari sistem Data Warehouse yang efisien dan efektif.

**INSTALASI MySQL**

![alt text](https://github.com/futhon/DWutdi/blob/main/public/Gambar%201.png?raw=true)
![alt text](https://github.com/futhon/DWutdi/blob/main/public/Gambar%202.png?raw=true)
![alt text](https://github.com/futhon/DWutdi/blob/main/public/Gambar%203.png?raw=true)
![alt text](https://github.com/futhon/DWutdi/blob/main/public/Gambar%204.png?raw=true)
![alt text](https://github.com/futhon/DWutdi/blob/main/public/Gambar%205.png?raw=true)
![alt text](https://github.com/futhon/DWutdi/blob/main/public/Gambar%206.png?raw=true)
![alt text](https://github.com/futhon/DWutdi/blob/main/public/Gambar%207.png?raw=true)
![alt text](https://github.com/futhon/DWutdi/blob/main/public/Gambar%208.png?raw=true)
![alt text](https://github.com/futhon/DWutdi/blob/main/public/Gambar%209.png?raw=true)


**PRAKTIKUM CRUD MENGGUNAKAN**

**MySQL COMMAND LINE CLIENT**

Tampilan awal MySQL Command Line Client

![alt text](https://github.com/futhon/DWutdi/blob/main/public/Picture%201.png?raw=true)

Proses yang dilakukan di MySQL Command Line melibatkan beberapa langkah penting dalam pengelolaan database dan tabel. Setelah login ke MySQL, perintah pertama yang dieksekusi adalah menampilkan daftar semua database yang ada di server MySQL dengan menggunakan show databases;. Hasilnya menampilkan empat database bawaan, yaitu information_schema, mysql, performance_schema, dan sys.

Selanjutnya, dilakukan upaya untuk membuat database baru dengan nama db_UTDI. Setelah database baru dibuat, perintah show databases; dijalankan kembali untuk memastikan bahwa database db_UTDI telah ditambahkan ke dalam daftar database. Langkah berikutnya adalah beralih ke database db_UTDI dengan menggunakan perintah use db_utdi;, yang mengubah fokus kerja ke database tersebut.

![alt text](https://github.com/futhon/DWutdi/blob/main/public/Picture%202.png?raw=true)

Dalam database db_UTDI, dibuat sebuah tabel baru bernama tb_mahasiswa dengan struktur yang terdiri dari lima kolom: id_mahasiswa, nama_mahasiswa, jenis_kelamin, no_telp, dan alamat. Kolom id_mahasiswa didefinisikan sebagai primary key dengan atribut auto_increment, yang berarti nilai kolom ini akan otomatis bertambah setiap kali data baru ditambahkan ke dalam tabel. Setelah tabel berhasil dibuat, perintah show tables; dijalankan untuk memastikan bahwa tabel tb_mahasiswa telah ada di dalam database.

Untuk melihat struktur tabel secara detail, perintah desc tb_mahasiswa; digunakan. Perintah ini menampilkan informasi mengenai tipe data, apakah kolom tersebut bisa bernilai NULL, serta atribut tambahan seperti auto_increment. Setelah itu, data mahasiswa dimasukkan ke dalam tabel tb_mahasiswa menggunakan perintah insert into tb_mahasiswa. Data yang dimasukkan adalah seorang mahasiswa bernama "Fukkar Al Wathoni" dengan ID 225611093.

Perintah select \* from tb_mahasiswa; kemudian dijalankan untuk menampilkan semua data yang ada dalam tabel, memastikan bahwa data mahasiswa yang baru saja ditambahkan telah berhasil masuk. Proses serupa dilakukan untuk menambahkan data mahasiswa kedua bernama "Erina Saraswati" dengan ID 225611094.

![alt text](https://github.com/futhon/DWutdi/blob/main/public/Picture%203.png?raw=true)
![alt text](https://github.com/futhon/DWutdi/blob/main/public/Picture%204.png?raw=true)

Langkah selanjutnya adalah memperbarui data pada tabel tb_mahasiswa, di mana nama mahasiswa dengan ID 225611094 diubah dari "Erina Saraswati" menjadi "Erina Gudono" menggunakan perintah update tb_mahasiswa. Setelah data diperbarui, perintah select \* from tb_mahasiswa; dijalankan kembali untuk memastikan perubahan telah diterapkan dengan benar.

![alt text](https://github.com/futhon/DWutdi/blob/main/public/Picture%205.png?raw=true)

Data mahasiswa dengan ID 225611094 dihapus dari tabel tb_mahasiswa menggunakan perintah delete from tb_mahasiswa. Setelah penghapusan, perintah select \* from tb_mahasiswa; kembali digunakan untuk memastikan bahwa data tersebut telah benar-benar dihapus dari tabel, menyisakan hanya satu data yaitu "Fukkar Al Wathoni".

![alt text](https://github.com/futhon/DWutdi/blob/main/public/Picture%206.png?raw=true)
