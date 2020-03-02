Pada pertemuan 5, user menggunakan software sistem operasi linux.

# Latihan 1 (Hidupkan server Redis)
Pertama tama disini user membuat satu direktori dengan nama redis-demo kemudian user masuk atau mengakses direktori yang sudah dibuat. Lalu, user menginstal python dengan source codenya sudo apt install python-pip.

![Picture1](Picture1.png)

![Picture2](Picture2.png)

![Picture3](Picture3.png)

Selanjutnya untuk memulai redis-cli pada beberapa shell, yang mana dapat menghubungkan kembali perintah Python redis dan perintah redis biasa dengan menginstall redis-py.

![Picture4](Picture4.png)

Untuk mengatahui apakah python dengan redis sudah terhubung, maka user membuat satu dokumen dengan nama connect.py yang disimpan dalam directory redis-demo.

![Picture5](Picture5.png)

Didalam dokumen connect.py user menginputkan query seperti  pada gambar dibawah agar saat mengecek koneksi antara redis dan pyton dan terhubung maka akan menampilkan “Connection to redis jas beend established” jika tidak terhubung maka akan menampilkan “Cannot connection to redis”.

![Picture6](Picture6.png)

Dibawah ini user mencoba mengecek koneksi antara redis dan pyton. Hasil output menampilkan “Connection to redis jas beend established” maka artinya keduanya sudah terhubung. Kemudian user mengakses dan masuk pada python, python siap dijalankan.

![Picture7](Picture7.png)

Pada pertemuan sebelumnya user sudah menjelaskan dan melakukan penginstalan redis pada terminal linux, disini user langsung mengakses dan masuk pada redis pada terminal. Redis siap dijalankan.

![Picture8](Picture8.png)

# Latihan 2 (Kerjakan Materi dan Penjelasan 2, 3 dan 4)

-- Materi dan Penjelasan 2

STRING
Pada redis berikut ini untuk mengatur nilai string, user menggunakan yang berikut dari redis-cli.

![Picture9](Picture9.png)

Sekarang user ingin melakukan hal yang sama pada shell Python dimana membuat instance dari StrictRedis . Ini diperlukan untuk komunikasi dengan redis-server. Coba dapatkan "mykey", yang diset menggunakan redis-cli dari Python. Output menampilkan hasil yang sama pada redis dimana python dapat berkomunikasi dengan benar dengan redis-server. Hal-hal yang dimasukkan ke dalam redis menggunakan redis-cli dapat dibaca menggunakan Python.

![Picture10](Picture10.png)

Selanjutnya user mencoba mengatur nilai ke Redis dari Python shell.

![Picture11](Picture11.png)

Kemudian periksa dari redis-cli apakah kunci ini disetel dengan benar. 

![Picture12](Picture12.png)

Seperti pada hasil tampilan output pada gambar terminal dimana python dapat memasukkan nilai ke dalam Redis dengan benar. 

![Picture13](Picture13.png)

INCR dan INCRBY
Redis juga menyediakan incr dan incrby pada nilai integer. Disini user akan mencoba menetapkan nilai integer.

![Picture14](Picture14.png)

setara redis-py dari Redis 'incr adalah 

![Picture15](Picture15.png)

Menampilkan untuk memverifikasi bahwa num telah bertambah

![Picture16](Picture16.png)

User memastikan dengan mengecek menggunakan redis-cli juga.

![Picture17](Picture17.png)

Setara Python dengan incrby adalah

![Picture18](Picture18.png)

User memastikan dengan mengecek lagi menggunakan redis-cli juga.
![Picture19](Picture19.png)

EXISTS

![Picture20](Picture20.png)

DEL
Saat kunci ini dihapus pada python, maka kita akan mendapatkan "nihil" dan "Tidak Ada" jika Anda mencoba mengambilnya pada redis.

![Picture21](Picture21.png)

![Picture22](Picture22.png)

EXPIRE
Tandai key second_num untuk kedaluwarsa setelah 10 detik

![Picture23](Picture23.png)

Kemudian user memeriksa lagi setelah 10 detik, hasil yang ditampilkan yaitu kosong atau tidak menampilkan output dimana second_num sudah kadaluarsa

![Picture24](Picture24.png)

REDIS LISTS
Redis lpush setara dengan menggunakan Python

![Picture25](Picture25.png)

User memastikan dengan mengecek dan verifikasi bahwa list dibuat diredis.

![Picture26](Picture26.png)

Menambahkan beberapa nilai ke list

![Picture27](Picture27.png)

Periksa daftar baru dari redis-cli

![Picture28](Picture28.png)

Periksa daftar baru dari Python

![Picture29](Picture29.png)

rpush

![Picture30](Picture30.png)

Periksa elemen yang didorong ke kanan

![Picture31](Picture31.png)

REDIS HASHES
hmset memungkinkan penyimpanan kamus sebagai nilai. Ini sama seperti pada redis docs.

![Picture32](Picture32.png)

redis-py cara mencapai hal yang sama akan

![Picture33](Picture33.png)

Memastikan yang diinput pada python ini menggunakan redis-cli

![Picture34](Picture34.png)

Menampilkan ini menggunakan redis-py

![Picture35](Picture35.png)

-- Materi dan Penjelasan 3

-- Materi dan Penjelasan 4
Pada materi dan penjelasan dibagian 3 yaitu menulis program dengan python yang membutuhkan lima langkah dasar yaitu impor redis, tentukan informasi koneksi untuk redis, membuat objek koneksi redis, mengatur pesan ke redis, mengambil pesan redis dan menampilkan pesan tersebut. 
Pertama – tama pada shell unix python, disini user membuat dokumen baru dengan nama python3.py yang didalamnya akan berisi skrip untuk mengimplementasikan 5 langkah tersebut

![Picture36](Picture36.png)

![Picture37](Picture37.png)

Setelah user menyalin kode ke dokumen dan mengubah parameter koneksi di langkah 2 untuk terhubung ke instance Redis user sendiri, user dapat menjalankan skrip ini langsung dari shell Unix. Jika parameter koneksi ditentukan dengan benar, maka akan menampilkan output pesan Hello Redis!!! .
Dari kode ini, user dapat memodifikasi kode tersebut menggunakan metode set dan get untuk menggunggah data yang berbeda. Dari program ini kita dapat bereksperimen dengan beberapa tipe data redis lain yang ditautkan diatas.

![Picture38](Picture38.png)