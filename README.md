# Tugas Praktikum SQL (Pertemuan 6)

| Variable | Isi |
| -------- | --- |
| Nama | RADITYA TANSY LIZARA  |
| NIM | 312310454 |
| Kelas | TI.23.A5 |
| Mata Kuliah | Basis Data |

# Soal Latihan Praktikum
## 1. Tulis semua perintah-perintah SQL percobaan di atas beserta outputnya!

**1. Buat sebuah database dengan nama latihan2**

Untuk membuat database gunakan perintah sebagai berikut :

`CREATE DATABASE [nama_database]`

`CREATE DATABASE latihan2;`

lalu, setelah kita membuat database. kita masuk kedalam database tersebut dengan perintah sebagai berikut :

`USE latihan2;`

![image](https://github.com/RadityaTansyLizara/praktikumsql/assets/147571863/0a28d560-2951-4356-9f7a-39817d6d7eae)

**2. Buat sebuah tabel dengan nama biodata (nama, alamat) didalam database latihan2!**

Untuk membuat Tabel gunakan perintah sebagai berikut :

`CREATE TABLE nama_tabel (
    nama_field1 tipe _data(ukuran), nama_field2 tipe_data(ukuran), ..., nama_fieldn tipe_data(ukuran)
    );`

`CREATE TABLE biodata (
    nama varchar (100),
    alamat text
    );`

    ![image](https://github.com/RadityaTansyLizara/praktikumsql/assets/147571863/91afe832-2aaa-466f-a519-995642051d38)

**3. Tambahkan sebuah kolom keterangan (varchar 15), sebagai kolom terakhir!**

Contoh :

`ALTER TABLE biodata ADD COLUMN keterangan VARCHAR (15);`

![image](https://github.com/RadityaTansyLizara/praktikumsql/assets/147571863/6d73b9ff-2ef7-4da2-8923-e7123028f7e9)

**4.Tambahkan kolom id(int 11) di awal (sebagai kolom pertama)!**

Untuk menambahkan kolom pertama yaitu dengan perintah sebagai berikut :

`ALTER TABLE biodata ADD COLUMN id int FIRST; `

![image](https://github.com/RadityaTansyLizara/praktikumsql/assets/147571863/a406141b-7963-45db-941b-6627b434c010)

**5. Sisipkan sebuah kolom dengan nama phone (varchar 15) setelah kolom alamat!**

Untuk menambahkan kolom setelah kolom lain yaitu dengan perintah `AFTER`

![image](https://github.com/RadityaTansyLizara/praktikumsql/assets/147571863/54de602a-0812-4703-80c4-983007e540fb)

**6. Ubah tipe data kolom id menjadi char(11)!**

Untuk mengubah type data yaitu dengan perintah sebagai berikut :

`ALTER TABLE [nama_tabel] MODIFY nama_field tipe_data_baru(ukuran);`

![image](https://github.com/RadityaTansyLizara/praktikumsql/assets/147571863/a11b6460-0d6b-4d84-a0ca-d26bcf37d483)

**7. Ubah nama kolom phone menjadi hp (char 20)!**

Untuk mengubah kolom yaitu dengan perintah sebgai berikut :

`ALTER TABLE [nama_tabel] CHANGE nama_field_lama nama_field_baru tipe_data(ukuran);`

![image](https://github.com/RadityaTansyLizara/praktikumsql/assets/147571863/55673499-cb5c-4bf8-9975-36c4be76144d)

**8. Tambahkan kolom email setelah kolom hp**

![image](https://github.com/RadityaTansyLizara/praktikumsql/assets/147571863/dc5f7a70-550d-46d9-884d-df0587777ca2)

**9. Hapus kolom keterangan dari tabel!**

Untuk menghapus kolom dari tabel yaitu dengan perintah sebagai berikut :

`ALTER TABLE [nama_tabel] DROP nama_field;`

![image](https://github.com/RadityaTansyLizara/praktikumsql/assets/147571863/cd431390-eac3-4b6c-8953-4a8a6ef1dbf5)

**10. Ganti nama tabel menjadi data_mahasiswa!**

Untuk mengganti nama tabel yaitu dengan perintah sebagai berikut :

`ALTER TABLE [nama_tabel] RENAME [nama_tabel_baru];`

![image](https://github.com/RadityaTansyLizara/praktikumsql/assets/147571863/8e64c811-28fd-4b42-99b9-ba96ac2417ac)

**11. Ganti nama field id menjadi nim!**

![image](https://github.com/RadityaTansyLizara/praktikumsql/assets/147571863/2e3f674b-7717-4156-b17f-19d4625a65d2)

**12. Jadikan nim sebagai PRIMARY KEY!**

Untuk menambahkan index atau key, gunakan perintah sebagai berikut :

tipe index :

- PRIMARY KEY
- UNIQUE KEY
- FULLTEXT

`ALTER TABLE [nama_tabel] ADD [INDEX|PRIMARY KEY] (nama_field);

![image](https://github.com/RadityaTansyLizara/praktikumsql/assets/147571863/2d5a7bcb-751c-476b-ba81-c94f65705890)

**13. Jadikan kolom email sebagai UNIQUE KEY!**

Perintah nya sama seperti diatas, hanya saja diganti menjadi `UNIQUE KEY`

![image](https://github.com/RadityaTansyLizara/praktikumsql/assets/147571863/1929625f-3905-42d8-9116-771afc418ee1)


## 2. Apa Maksud Dari INT(11) ?
Jawaban	: Maksud dari int (11) dalam SQL adalah tipe data yang berbentuk angka. Selain itu juga spesifikasi yang sering digunakan dalam bahasa SQL, terutama dalam konteks pembuatan tabel dan kolom pada database. Ini menandakan tipe data kolom sebagai bilangan bulat (integer) dengan lebar (width) maksimum 11 digit.

## 3. Ketika Kita Melihat Struktur Tabel Dengan Perintah DESC , Ada Kolom Null yang Berisi Yes dan No. Apa Maksudnya ?
Jawaban	: Jika kolom Null berisi YES, itu berarti kolom tersebut diperbolehkan untuk memiliki nilai NULL, yang berarti nilai di kolom tersebut dapat kosong atau tidak diisi. Ini berarti bahwa baris-baris dalam tabel dapat memiliki nilai NULL pada kolom tersebut.

Jika kolom Null berisi NO, itu berarti kolom tersebut tidak diperbolehkan untuk memiliki nilai NULL, yang berarti setiap baris dalam tabel harus memiliki nilai yang valid untuk kolom tersebut. Dalam hal ini, kolom tersebut diwajibkan memiliki nilai yang valid, dan tidak boleh kosong atau tidak diisi.
