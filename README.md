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

# Memilih data bedasarkan value
SELECT * FROM nama_tabel WHERE nama_kolom = value;

# Mengurutkan data dari terkecil (ascending) atau terkecil (descending)
SELECT * FROM nama_tabel ORDER BY nama_kolom ASC;
SELECT * FROM nama_tabel ORDER BY nama_kolom DESC;

# Membatasi jumlah data yang ditampilkan
SELECT * FROM nama_tabel LIMIT value1, value2;
# contoh :
SELECT * FROM produk LIMIT 5,5; # value1 = lewati 5 data, value2 = tampilkan 5 data

```
#### UPDATE data
```sh
# Update 1 data
UPDATE nama_tabel SET nama_kolom = value WHERE nama_kolom_primary = value;

# Update lebih dari 1 data
UPDATE nama_tabel SET nama_kolom1 = value, nama_kolom2 = value WHERE nama_kolom_primary = value;

# Update data value dengan operator matematika
UPDATE nama_tabel SET nama_kolom = value + value WHERE nama_kolom_primary = value;
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
