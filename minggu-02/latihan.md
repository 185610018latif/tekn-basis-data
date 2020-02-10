# Latihan 1 (Instalasi MonggoDB)

Latihan pada praktik 2 ini yaitu menginstal aplikasi MongoDB.
Setelah MongoDB berhasil download, silahkan jalankan file instalasinya. Tampilannya seperti pada gambar dan klik next untuk melanjutkan proses instalasi.
![Picture1](Picture1.png)
 
Dihalaman berikutnya ke jendela End-User Licence Agreement, silahkan check I accept the terms in the License Agreement setelah itu klik tombol Next
![Picture2](Picture2.png)
 
Di halaman Choose Setup Type, dimana jendela ini ada dua pilihan yang ingin diinstal yakni Complete dan Custom, disini user memilih Complete.
![Picture3](Picture3.png)
 
Di halaman Service Configuration check Install MongoD as a service kemudian tekan Next untuk melanjutkan.
![Picture4](Picture4.png)
![Picture5](Picture5.png) 
 
Selanjutnya akan muncul windows Ready to Install MongoDB 4.3.3, silahkan klik tombol install dan tunggu sampai proses instalasi selesai.
![Picture6](Picture6.png)
![Picture7](Picture7.png)
 
Klik tombol Finish jika proses instalasi telah selesai.
![Picture8](Picture8.png) 
 
# Latihan 2	(Jalankan MongoDB server dengan menggunakan mongo shell)
Jika Mongodb berhasil terinstall, maka langkah selanjutnya yaitu membuka cmd (Command Prompt). Kemudian kita akan masuk ke dalam direktori dimana file MongoDB tersimpan dengan cara cd C:\Program Files\MongoDB\Server\4.3\bin atau bisa juga dicopy pada alamat direktori pada file explorer. Apabila sudah masuk dalam direktori MongoDb ketik mongod lalu tekan enter, maka akan muncul proses seperti pada gambar dibawah.
![Picture9](Picture9.png)
 
Jika proses berhasil, user akan membuat folder baru di direktori C:\ dengan nama data. Kemudian didalam folder data tersebut, buatlah folder baru lagi dengan nama db.
![Picture10](Picture10.png) 
![Picture11](Picture11.png) 
 
Lalu kembali lagi di Command Prompt, kemudian ketik mongo dan tekan enter maka akan muncul proses lagi seperti gambar dibawah.
![Picture12](Picture12.png) 
 
Jika proses sudah berhasil, kembali dan masuk ke folder data -> db apabila muncul file-file seperti pada gambar dibawah maka file Mongodb berhasil dibuat.
![Picture13](Picture13.png) 
 
Kembali lagi ke Command Prompt kemudian ketik mongo dan tekan enter, jika hasil proses seperti dibawah maka Mongodb server berhasil dijalankan dengan menggunakan akases mongo shell.
![Picture14](Picture14.png)
 
 
# Latihan 3 (Kerjakan getting started)
Tab 0
1.	db menunjukkan bahwa merujuk ke database saat ini atau database yang sedang aktif.
![Picture15](Picture15.png)
 
2.	use examples menunjukkan bahwa berpindah database, dimana untuk beralih ke database examples
![Picture16](Picture16.png)
 
Tab 1
1.	Contoh berikut menggunakan metode db.collection.insertMany() menunjukkan untuk menyisipkan dokumen baru yang lebih dari satu atau lebih ke dalam collection inventory. 
![Picture17](Picture17.png)
 
Tab 2
1.	db.inventory.find merujuk untuk melihat semua dokumen pada collection inventory.
![Picture18](Picture18.png)
 
2.	db.inventory.find().pretty merujuk untuk melihat semua dokumen pada collection inventory dengan tampilan yang teratur atau tersusun rapih dalam arti dipercantik susunan dokumen.
![Picture19](Picture19.png)
![Picture20](Picture20.png)
![Picture21](Picture21.png)
 
Tab 3
1.	db.inventory.find merujuk untuk shell dokumen yang bidang isinya sama dengan huruf"D" :
![Picture22](Picture22.png)
 
2.	db.inventory.find merujuk untuk shell dokumen yang bidang isinya sama dengan angka "0" :
![Picture23](Picture23.png)
 
3.	db.inventory.find merujuk untuk shell dokumen yang bidang isinya sama dengan angka"0" dan huruf”d”:
![Picture24](Picture24.png)
 
4.	db.inventory.find merujuk untuk shell dokumen yang bidang isinya adalah size.oum sama dengan "in" :
![Picture25](Picture25.png)
 
5.	db.inventory.find merujuk untuk shell dokumen yang bidang isinya adalah size.oum sama dengan "cm", h sama dengan “14” dan w sama dengan “21” :
![Picture26](Picture26.png)
 
6.	db.inventory.find merujuk untuk shell dokumen yang bidang isinya adalah tags sama dengan "red" :
![Picture27](Picture27.png)
 
7.	db.inventory.find merujuk untuk shell dokumen yang bidang isinya adalah tags sama dengan "red" dan “blank” :
![Picture28](Picture28.png)
 
Tab 4
1.	db.inventory.find merujuk untuk shell dokumen yang bidang isinya adalah item sama dengan "1" dan status sama dengan “1” :
![Picture29](Picture29.png)
 
2.	db.inventory.find merujuk untuk shell dokumen yang bidang isinya adalah _id sama dengan "0", item sama dengan “1” dan status sama dengan “1” :
![Picture30](Picture30.png) 
 
# Latihan 4	(Kerjakan CRUD pada materi dan penjelasan nomor 2)
CREATE Diartikan yaitu MEMBUAT atau masukkan operasi, dimana menambahkan dokumen baru ke dalam collection. Jika collection saat ini tidak ada, operasi akan membuat collection. Didalam MongoDB terdapat dua method untuk menambahkan dokumen dalam collection yakni :
1.	insertOne() dimana menginsert atau menambahkan satu data kedalam collection.
Contoh menambahkan 1 dokumen baru ke dalam koleksi inventory . Jika dokumen tidak menentukan bidang _id , MongoDB menambahkan bidang _id dengan nilai ObjectId ke dokumen baru.
![Picture31](Picture31.png)
 
2.	insertMany() dimana menginsert atau menambahkan data yang lebih dari satu kedalam collection.
Contoh menambahkan beberapa dokumen baru ke dalam koleksi inventory . Jika dokumen tidak menentukan bidang _id , MongoDB menambahkan bidang _id dengan nilai ObjectId ke setiap dokumen. 
![Picture32](Picture32.png)
 
Contoh insertOne pada [Getting Started](https://docs.mongodb.com/manual/crud/)
![Picture33](Picture33.png) 

READ Diartikan yaitu MEMBACA atau mengambil dokumen dari collection. Berikut dalam MongoDB terdapat method untuk meminta collection untuk dokumen.
Query Document
1.	Menampilkan semua Dokumen, Gambar dibawah ini memberikan contoh operasi query menggunakan metode db.collection.find() di mongo shell. 
Contoh di halaman ini menggunakan collection inventory . Untuk mengisi koleksi inventory, jalankan yang berikut :
![Picture34](Picture34.png)
 
Untuk menampilkan semua dokumen dalam collection yaitu dengan query seperti pada contoh gambar dibawah bedanya dengan mysql yaitu menggunakan query select*from sedangkan nosql menggunakan sytak find().
![Picture35](Picture35.png)
 
2.	Menampilkan dokumen sesuai dengan kondisi yang spesifik, dalam nosql dapat menggunakan operator kueri untuk menentukan kondisi dalam formulir. 
Berikut contoh mengambil semua dokumen dari collection inventory mana status sama dengan "D" :
![Picture36](Picture36.png)
 
Contoh berikut mengambil semua dokumen dari collection inventory mana status sama dengan "A" atau "D" :
![Picture37](Picture37.png)
 
3.	Menampilkan dokumen sesuai dengan kondisi dan spesifikasi dimana query majemuk dapat menentukan kondisi untuk lebih dari satu bidang dalam dokumen koleksi. Secara implisit, logika AND konjungsi menghubungkan klausa dari query gabungan sehingga kueri memilih dokumen dalam collection yang cocok dengan semua kondisi. 
Contoh berikut mengambil semua dokumen dalam koleksi inventory mana status sama dengan "A" dan qty kurang dari ( $lt ) 30 :
![Picture38](Picture38.png)
 
4.	Menampilkan dokumen sesuai dengan kondisi dan spesifikasi dimana menggunakan $or operator, yang dapat menentukan query gabungan yang bergabung dengan setiap klausa dengan logika OR konjungsi sehingga kueri memilih salah satu dokumen dalam collection yang cocok dengan setidaknya satu kondisi.
Contoh berikut mengambil semua dokumen dalam collection di mana status sama dengan "A" atau qty kurang dari ( $lt ) 30 :
![Picture39](Picture39.png)
 
5.	Spesifikasi AND serta OR Kondisi
Dalam contoh berikut, dokumen query gabungan memilih semua dokumen dalam collection di mana status sama dengan "A" dan jumlah qty kurang dari ( $lt ) 30 atau item dimulai dengan karakter p :
![Picture40](Picture40.png)
 
UPDATE diartikan yaitu MEMPERBAHARUI dimana suatu dokumen dalam collection untuk memperbarui dan mengubah nilai-nilai dokumen. Untuk menggunakan operator pembaruan, terdapat 3 metode pembaruan dokumen pembaruan bentuk yaitu:
1.	Perbarui Satu Dokumen
Dalam contoh berikut menggunakan metode db.collection.updateOne() pada koleksi inventory untuk memperbarui dokumen pertama di mana item sama dengan "paper" :
![Picture41](Picture41.png)
 
2.	Perbarui beberapa dokumen
Contoh berikut menggunakan metode db.collection.updateMany() pada koleksi inventory untuk memperbarui semua dokumen dengan jumlah qty kurang dari 50 :
![Picture42](Picture42.png)
 
Operasi pembaruan :
-	menggunakan $set operator untuk memperbarui nilai bidang size.uom ke "in" dan nilai bidang status ke "P" ,
-	menggunakan operator $currentDate untuk memperbarui nilai bidang lastModified ke tanggal saat ini. Jika bidang lastModified tidak ada, $currentDate akan membuat bidang tersebut. Lihat $currentDate untuk detailnya.
3.	Ganti Dokumen
Untuk mengganti seluruh konten dokumen kecuali _idbidang, dokumen yang sama sekali baru sebagai argumen kedua db.collection.replaceOne().
Saat mengganti dokumen, dokumen pengganti harus terdiri dari hanya pasangan bidang atau nilai; yaitu tidak termasuk ekspresi operator pembaruan. Dokumen pengganti dapat memiliki bidang berbeda dari dokumen asli. Dalam dokumen pengganti, user dapat menghilangkan _idbidang karena _idbidang tidak dapat diubah; Namun, jika user menyertakan _idbidang, itu harus memiliki nilai yang sama dengan nilai saat ini.
Contoh berikut menggantikan dokumen pertama dari inventorykoleksi tempat :item: "paper"
![Picture43](Picture43.png)
 
DELETE diartikan yaitu MENGHAPUS dimana digunakan untuk menghapus dokumen pada collection. Untuk menggunakan operator hapus, terdapat 3 metode untuk menghapus dokumen yaitu:
1.	Menghapus semua dokumen
Untuk menghapus semua dokumen dari collection. Berikut menghapus semua dokumen dari collection :
![Picture44](Picture44.png)
 
2.	Hapus Hanya Satu Dokumen yang Sesuai dengan Suatu Kondisi
Untuk menghapus paling banyak dari satu dokumen yang cocok dengan cara memfilter yang ditentukan (meskipun beberapa dokumen mungkin cocok dengan dokumen yang ditentukan) gunakan metode db.collection.deleteOne ().
Contoh berikut menghapus dokumen pertama yang statusnya "D":
![Picture45](Picture45.png)
 
3.	Hapus Semua Dokumen yang Sesuai dengan Suatu Kondisi
Untuk dapat menentukan kriteria, atau memfilter, yang mengidentifikasi dokumen yang akan dihapus. Filter menggunakan sintaks yang sama dengan operasi baca. 
Contoh berikut menghapus semua dokumen dari koleksi inventaris di mana bidang status sama dengan "A":
![Picture46](Picture46.png)
 

