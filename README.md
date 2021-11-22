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
#### Memilih data di tabel
```sh
# Memilih semua data
SELECT * FROM nama_tabel;

# Memilih data bedasarkan kolom
SELECT nama_kolom1, nama_kolom2, nama_kolom3 FROM nama_tabel;

# Memilih data bedasarkan value
SELECT * FROM nama_tabel WHERE nama_kolom = value;
```
#### Update data
```sh
# Update 1 data
UPDATE nama_tabel SET nama_kolom = value WHERE nama_kolom_primary = value;;

# Update lebih dari 1 data
UPDATE nama_tabel SET nama_kolom1 = value, nama_kolom2 = value WHERE nama_kolom_primary = value;

# Update data value dengan operator matematika
UPDATE nama_tabel SET nama_kolom = value + value WHERE nama_kolom_primary = value;
```
