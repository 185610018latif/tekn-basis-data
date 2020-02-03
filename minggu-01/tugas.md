----- Membuat Database -----
MariaDB [(none)]> create database movie;
Query OK, 1 row affected (0.002 sec)

----- Memilih Database -----
MariaDB [(none)]> use movie;
Database changed

----- Membuat Tabel dengan field -----
MariaDB [movie]> create table member ( membership_id char(3) not null primary key,
    ->                                  full_names varchar(30) not null,
    ->                                  physical_address varchar(30) not null,
    ->                                  salutation_id char(3) not null);
Query OK, 0 rows affected (0.047 sec)

----- Menampilkan Tabel Member -----
MariaDB [movie]> desc member;
+------------------+-------------+------+-----+---------+-------+
| Field            | Type        | Null | Key | Default | Extra |
+------------------+-------------+------+-----+---------+-------+
| membership_id    | char(3)     | NO   | PRI | NULL    |       |
| full_names       | varchar(30) | NO   |     | NULL    |       |
| physical_address | varchar(30) | NO   |     | NULL    |       |
| salutation_id    | char(3)     | NO   |     | NULL    |       |
+------------------+-------------+------+-----+---------+-------+
4 rows in set (0.042 sec)

----- Membuat Tabel dengan field -----
MariaDB [movie]> create table movie (membership_id char(3) not null primary key,
    ->                                  movie_rented varchar(30) not null);
Query OK, 0 rows affected (0.043 sec)

----- Menampilkan Tabel Movie -----
MariaDB [movie]> desc movie;
+---------------+-------------+------+-----+---------+-------+
| Field         | Type        | Null | Key | Default | Extra |
+---------------+-------------+------+-----+---------+-------+
| membership_id | char(3)     | NO   | PRI | NULL    |       |
| movie_rented  | varchar(30) | NO   |     | NULL    |       |
+---------------+-------------+------+-----+---------+-------+
2 rows in set (0.046 sec)

----- Membuat Tabel Movie -----
MariaDB [movie]> create table title (salutation_id char(3) not null primary key,
    ->                                  salutation varchar(5));
Query OK, 0 rows affected (0.043 sec)

----- Menampilkan Tabel Title -----
MariaDB [movie]> desc title;
+---------------+------------+------+-----+---------+-------+
| Field         | Type       | Null | Key | Default | Extra |
+---------------+------------+------+-----+---------+-------+
| salutation_id | char(3)    | NO   | PRI | NULL    |       |
| salutation    | varchar(5) | YES  |     | NULL    |       |
+---------------+------------+------+-----+---------+-------+
2 rows in set (0.093 sec)

----- Mengisi Data pada Tabel -----
MariaDB [movie]> insert into member (membership_id, full_names, physical_address, salutation_id)
    -> values (1, 'Janet Jones', 'First Street Plot No 4', 2),
    ->          (2, 'Robert Phil', '3rd Street 34', 1),
    ->          (3, 'Robert Phil', '5th Avenue', 1);
Query OK, 3 rows affected (0.020 sec)
Records: 3  Duplicates: 0  Warnings: 0

----- Menampilkan Data pada Tabel -----
MariaDB [movie]> select * from member;
+---------------+-------------+------------------------+---------------+
| membership_id | full_names  | physical_address       | salutation_id |
+---------------+-------------+------------------------+---------------+
| 1             | Janet Jones | First Street Plot No 4 | 2             |
| 2             | Robert Phil | 3rd Street 34          | 1             |
| 3             | Robert Phil | 5th Avenue             | 1             |
+---------------+-------------+------------------------+---------------+
3 rows in set (0.000 sec)

