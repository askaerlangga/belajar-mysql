# Dokumentasi belajar Database MySQL

#### Membuat database baru
```sh
CREATE DATABASE nama_database;
```
#### Menampilkan semua databse
```sh
SHOW DATABASES;
```
#### Menghapus database beserta isinya
```sh
DROP DATABASE nama_database;
```
#### Memilih database yang akan digunakan
```sh
USE nama_database;
```
#### Melihat semua tabel
```sh
SHOW tables;
```
#### Menghapus tabel beserta isinya
```sh
DROP TABLE nama_tabel;
```
#### SELECT data di tabel
```sh
# Memilih semua data
SELECT * FROM nama_tabel;

# Memilih data bedasarkan kolom
SELECT nama_kolom1, nama_kolom2, nama_kolom3 FROM nama_tabel;

# Memilih data bedasarkan value menggunakan operator perbandingan (=, >=, <=, >, <, !=)
SELECT * FROM nama_tabel WHERE nama_kolom = value;
SELECT * FROM nama_tabel WHERE nama_kolom > value;

# Memilih data bedasarkan value menggunakan operator boolean (AND, OR, NOT)
SELECT * FROM nama_tabel WHERE nama_kolom = value AND nama_kolom >= value;
SELECT * FROM nama_tabel WHERE nama_kolom != value OR nama_kolom < value;
# Prioritas ()
SELECT * FROM nama_tabel WHERE (nama_kolom != value OR nama_kolom < value) AND nama_kolom = value;

# Memilih data menggunakan LIKE dan NOT LIKE operator
SELECT * FROM nama_tabel WHERE nama_kolom LIKE value%;
SELECT * FROM nama_tabel WHERE nama_kolom LIKE %value%;
SELECT * FROM nama_tabel WHERE nama_kolom LIKE %value;
SELECT * FROM nama_tabel WHERE nama_kolom NOT LIKE value%;

# Memilih data yang NULL dan NOT NULL
SELECT * FROM nama_tabel WHERE nama_kolom IS NULL;
SELECT * FROM nama_tabel WHERE nama_kolom IS NOT NULL;

# Memilih data menggunakan operator BETWEEN dan NOT BETWEEN
SELECT * FROM nama_tabel WHERE nama_kolom BETWEEN value AND value;
SELECT * FROM nama_tabel WHERE nama_kolom NOT BETWEEN value AND value;

# Memilih data menggunakan operator IN dan NOT IN
SELECT * FROM nama_tabel WHERE nama_kolom IN (value, value);
SELECT * FROM nama_tabel WHERE nama_kolom NOT IN (value, value);

# Mengurutkan data dari terkecil (ascending) atau terkecil (descending)
SELECT * FROM nama_tabel ORDER BY nama_kolom ASC;
SELECT * FROM nama_tabel ORDER BY nama_kolom DESC;
# Lebih dari 1 kolom
SELECT * FROM nama_tabel ORDER BY nama_kolom ASC, nama_kolom DESC;

# Membatasi jumlah data yang ditampilkan
SELECT * FROM nama_tabel LIMIT value1, value2;
# contoh :
SELECT * FROM produk LIMIT 5, 5; # value1 = lewati 5 data, value2 = tampilkan 5 data
```
#### Select AS Alias
```sh
SELECT nama_kolom AS 'Nama Alias',
nama_kolom2 AS 'Nama Alias 2',
FROM nama_tabel;
```
#### UPDATE data
```sh
# Update 1 data
UPDATE nama_tabel SET nama_kolom = value WHERE nama_kolom_primary = value;

# Update lebih dari 1 data
UPDATE nama_tabel SET nama_kolom1 = value, nama_kolom2 = value WHERE nama_kolom_primary = value;

# Update data value dengan operator matematika
UPDATE nama_tabel SET nama_kolom = value + value WHERE nama_kolom_primary = value;
UPDATE nama_tabel SET nama_kolom = nama_kolom + value WHERE nama_kolom_primary = value;
```
#### INSERT data di tabel
```sh
# Memasukan data ke tabel
INSERT INTO nama_tabel(nama_kolom1,nama_kolom2) VALUES (value1,value2);
```
#### DELETE data di tabel
```sh
DELETE FROM nama_tabel WHERE nama_kolom = value;
```
