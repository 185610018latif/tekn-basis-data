# Latihan 1
---
Pada latihan pada praktikum 1 ini langkah awal yang dipelajari yaitu menginstall aplikasi mariaDB atau
MySQL shell, disini saya memilih MariaDB untuk mengaplikasikan suatu data dalam database dan sistem operasi
yang digunakan yakni windows 10. 

Setelah file instalasi MariaDB 10.5.0 berhasil download, silahkan jalankan file instalasinya. Tampilannya seperti pada gambar
(Picture1.PNG)

Selanjutnya klik tombol next untuk melanjutkan proses instalasi. Dihalaman berikutnya ke jendela End-User License Agreement, silahkan check A accept the terms in the License Agreement setelah itu klik tombol Next
![gambar2](Picture2.PNG)

Di halaman Custom Setup, dimana pada jendela ini kalian bisa memilih fitur mariaDB apa saja yang ingin diinstall, saya sarankan pilih saja semua lalu klik tombol Next.
(img src="Picture3.png")

Selanjutnya user akan diminta memasukan password yang nanti akan digunakan untuk membuka database MariaDB, checklist juga Enable access from remote machine for ‘root’ user agar kalian bisa melakukan remot terhadap database MariaDB dan check juga Use UTF8 as default server’s character set. Lalu klik tombol Next.
!(img src="Picture4.png")

Atur nama service dan port yang akan digunakan, disini user menggunakan settiingan default saja. Lalu klik tombol Next.
![gambar5](Picture5.PNG)

Selanjutnya akan muncul windows Ready to Install MariaDB 10.5, silahkan klik tombol install dan tunggu sampai proses instalasi selesai.
![gambar6](Picture6.PNG)

Klik tombol Finish jika proses instalasi telah selesai.
![gambar7](Picture7.PNG)
![gambar8](Picture8.PNG)

Berikut adalah tampilan dari database MariaDB saat pertama kali dibuka.
![gambar9](Picture9.PNG)


# Latihan 2
---
Untuk latihan yang kedua berisi penjelasan bagaimana langkah untuk membuat database, membuat tabel, menginsert data pada tabel, menghapus data, tabel dan database sesuai dengan tutorial yang ada pada [tutorialspoint](https://www.guru99.com/database-normalization.html). 

----- Membuat Database -----
MariaDB [movie]> create database testDB;
Query OK, 1 row affected (0.003 sec)

----- Menampilkan Database -----
MariaDB [movie]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| movie              |
| mysql              |
| performance_schema |
| test               |
+--------------------+
5 rows in set (0.002 sec)

----- Menghapus DataBase Baru -----
MariaDB [movie]> drop database testDB;
Query OK, 0 rows affected (0.005 sec)

----- Memilih Database -----
MariaDB [movie]> use testDB;
Database changed

----- Membuat Table -----
MariaDB [testDB]> create table customers (
    -> ID int not null,
    -> NAME varchar(20) not null,
    -> AGE int not null,
    -> ADDRESS char(25),
    -> SALARY decimal(18,2),
    -> primary key (ID));
Query OK, 0 rows affected (0.247 sec)

----- Menambahkan Data ke dalam Tabel -----
MariaDB [testDB]> insert into customers (ID, NAME, AGE, ADDRESS, SALARY)
    -> values (1, 'Ramesh', 32, 'Ahmedabad', 2000.00);
Query OK, 1 row affected (0.024 sec)

----- Menampilkan Semua Data pada Tabel Customer -----
MariaDB [testDB]> select * from customers;
+----+----------+-----+-----------+---------+
| ID | NAME     | AGE | ADDRESS   | SALARY  |
+----+----------+-----+-----------+---------+
|  1 | Ramesh   |  32 | Ahmedabad | 2000.00 |
|  2 | Khilan   |  25 | Delhi     | 1500.00 |
|  3 | Kaushik  |  23 | Kota      | 2000.00 |
|  4 | Chaitali |  25 | Mumbai    | 6500.00 |
|  5 | Hardik   |  27 | Bhopal    | 8500.00 |
|  6 | Komal    |  22 | MP        | 4500.00 |
+----+----------+-----+-----------+---------+
6 rows in set (0.001 sec)

----- Menampilkan Data Nama dan Gaji, berdasarkan Gaji lebih dari 2000 -----
MariaDB [testDB]> select ID, NAME, SALARY from customers
    -> where SALARY > 2000;
+----+----------+---------+
| ID | NAME     | SALARY  |
+----+----------+---------+
|  4 | Chaitali | 6500.00 |
|  5 | Hardik   | 8500.00 |
|  6 | Komal    | 4500.00 |
+----+----------+---------+
3 rows in set (0.001 sec)

----- Menampilkan Id, Nama dan Gaji berdasarkan Gaji lebih dari 2000 dengan umur dibawah 25 -----
MariaDB [testDB]> select ID, NAME, SALARY from customers
    -> where SALARY > 2000 AND AGE < 25;
+----+-------+---------+
| ID | NAME  | SALARY  |
+----+-------+---------+
|  6 | Komal | 4500.00 |
+----+-------+---------+
1 row in set (0.001 sec)

----- Memperbaharui Data Alamat pada Id 6 -----
MariaDB [testDB]> update customers
    -> set ADDRESS = 'Pune'
    -> where ID = 6;
Query OK, 1 row affected (0.010 sec)
Rows matched: 1  Changed: 1  Warnings: 0

----- Menghapus Data -----
MariaDB [testDB]> delete from customers
    -> where ID = 6;
Query OK, 1 row affected (0.015 sec)

----- Menampilkan semua Data Customers dimana Gaji mulai dari 2000 ----
MariaDB [testDB]> select * from customers
    -> where salary like '200%';
+----+---------+-----+-----------+---------+
| ID | NAME    | AGE | ADDRESS   | SALARY  |
+----+---------+-----+-----------+---------+
|  1 | Ramesh  |  32 | Ahmedabad | 2000.00 |
|  3 | Kaushik |  23 | Kota      | 2000.00 |
+----+---------+-----+-----------+---------+
2 rows in set (0.001 sec)

----- Menampilkan 3 Data Teratas -----
MariaDB [testDB]> select * from customers
    -> limit 3;
+----+---------+-----+-----------+---------+
| ID | NAME    | AGE | ADDRESS   | SALARY  |
+----+---------+-----+-----------+---------+
|  1 | Ramesh  |  32 | Ahmedabad | 2000.00 |
|  2 | Khilan  |  25 | Delhi     | 1500.00 |
|  3 | Kaushik |  23 | Kota      | 2000.00 |
+----+---------+-----+-----------+---------+
3 rows in set (0.001 sec)

----- Menampilkan urutan naik dari Gaji dan Nama -----
MariaDB [testDB]> select * from customers
    -> order by NAME, SALARY;
+----+----------+-----+-----------+---------+
| ID | NAME     | AGE | ADDRESS   | SALARY  |
+----+----------+-----+-----------+---------+
|  4 | Chaitali |  25 | Mumbai    | 6500.00 |
|  5 | Hardik   |  27 | Bhopal    | 8500.00 |
|  3 | Kaushik  |  23 | Kota      | 2000.00 |
|  2 | Khilan   |  25 | Delhi     | 1500.00 |
|  1 | Ramesh   |  32 | Ahmedabad | 2000.00 |
+----+----------+-----+-----------+---------+
5 rows in set (0.001 sec)

----- Menampilkan satu data pada GAJI atau tidak duplikat ----- 
MariaDB [testDB]> select distinct SALARY from customers
    -> order by SALARY;
+---------+
| SALARY  |
+---------+
| 1500.00 |
| 2000.00 |
| 6500.00 |
| 8500.00 |
+---------+
4 rows in set (0.001 sec)