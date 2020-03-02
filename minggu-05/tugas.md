# Tugas (Kerjakan sesuai dengan artikel dari [RealPython.com](https://realpython.com/python-redis/#using-redis-py-redis-in-python))

Pada tugas dimulai dengan contoh database pemetaan negara dengan menggunakan set untuk mengatur pasangan nilai kunci dengan redis.

![Picture39](Picture39.png)

Urutan pernyataan yang sesuai dalam Python akan terlihat seperti ini :

![Picture40](Picture40.png)

Redis juga memungkinkan Anda untuk mengatur dan mendapatkan beberapa pasangan nilai kunci dalam satu perintah, MSET dan MGET:

![Picture41](Picture41.png)

Untuk menggunakan Python adalah dengan dict.update() :

![Picture42](Picture42.png)

Kami menggunakan .get () daripada .__ getitem __ () untuk meniru perilaku Redis untuk mengembalikan nilai seperti null ketika tidak ada kunci yang ditemukan. Sebagai contoh ketiga, perintah EXISTS yaitu memeriksa apakah ada kunci pada database:

![Picture43](Picture43.png)

Python memiliki kata kunci in untuk menguji hal yang sama, yang rute ke dict.__contains__(key):

![Picture44](Picture44.png)

Beberapa contoh ini dimaksudkan untuk menunjukkan, menggunakan Python asli, apa yang terjadi pada tingkat tinggi dengan beberapa perintah Redis yang umum. Tidak ada komponen client-server di sini untuk contoh Python, dan redis-py belum memasukkan gambar. Ini hanya dimaksudkan untuk menunjukkan fungsionalitas Redis dengan contoh.

